# Pointer Events Polyfill for JSDOM

This is a polyfill explicitly designed for use in JSDOM to solve the issue of
unimplemented pointer event functionality.

## Scope

Unlike other pointer event polyfills, such as the popular [jQuery PEP]() library,
this polyfill is _not_ intended to provide a complete implementation of pointer
events for production use. Instead, the scope of this polyfill is to only
provide the subset of behavior for pointer events that is missing from JSDOM.

At the time of writing, the missing behaviors are:
 -  A complete, conformant implementation of the `PointerEvent` interface.
 -  An implementation of `Element.setPointerCapture()` and `Element.releasePointerCapture()`.

This polyfill is not intended to provide any utilities for performing testing
of pointer events. Instead it is recommended to use [`@testing-library/dom`]()
and its associated wrappers.