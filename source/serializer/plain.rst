=====
Plain
=====

The plain text serializer converts chat components to their plain-text representation
and back. It is thus the simplest text serializer in Adventure. This serializer is
useful for supporting legacy clients, logging, clearing formatting from a component that
originates from external source, and provides a small, self-contained example of a
text serializer.

The plain text serializer, by its nature, does not support any advanced features, including
color, hover and click events, URL linking, or insertions. If advanced features are desired,
consider using :doc:`/minimessage`.

Usage
-----

The plain serializer is accessed using the ``PlainComponentSerializer``. You can
use ``PlainComponentSerializer.plain()`` for a default instance that silently ignores
keybind and translatable components, or construct your own ``PlainComponentSerializer``
that maps the components to some plain-text representation.

The deserialization of plain text is equivalent to ``Component.text(string)``. No
preprocessing is done on the input. The deserialization is implemented in order to provide
API consistency.
