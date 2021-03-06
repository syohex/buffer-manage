# Manager Emacs Buffers [![MELPA badge][melpa-badge]][melpa-link] [![MELPA stable badge][melpa-stable-badge]][melpa-stable-link] [![Travis CI Build Status][travis-badge]][travis-link]

  [melpa-link]: https://melpa.org/#/buffer-manage
  [melpa-stable-link]: https://stable.melpa.org/#/buffer-manage
  [melpa-badge]: https://melpa.org/packages/buffer-manage-badge.svg
  [melpa-stable-badge]: https://stable.melpa.org/packages/buffer-manage-badge.svg
  [travis-link]: https://travis-ci.org/plandes/buffer-manage
  [travis-badge]: https://travis-ci.org/plandes/buffer-manage.svg?branch=master

Provides support to multiple managed buffers of any kind.  This is helpful for
using multiple inferior shells, multiple SQL session buffers or any other piped
process that requires multiple buffers.

The library includes support for:
* A major mode and buffer for listing, switching, and organizing multiple emacs
  buffers.
* Fast switching with customized key bindings through the customize framework.
* Switch between managers providing the same key bindings for buffer entries
  with the same key bindings for creation, switching and managing.
* Create your own trivial implementations in minimal set of Emacs Lisp code.
* Interact with buffer entries and manager as objects with a straight forward
  API.


## Usage

This isn't useful by itself, you need to extend but subclassing eieio (Emacs
Lisp) objects.  See the [buffer shell](https://github.com/plandes/bshell)
project for an example.  This is doen by extending Emacs `eieio` objects and
can be done in ~90 lines of code
(example: [buffer shell](https://github.com/plandes/bshell)).

To create your own managed buffer set you must extend `buffer-entry` that
defines behavior for each created managed buffer.  You must also extend the
manager itself `buffer-manager`.


## License

Copyright © 2017 Paul Landes

GNU Lesser General Public License, Version 2.0
