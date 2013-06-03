File Encoding
=============

This VIM plugin provides a function to return information on the buffer and
file encoding being used for a buffer.
The output can be used in a statusline, for example:

    set statusline=%f\ %{StatusFileEncoding('%')}

The function retuns a string as follows:

- `""` if the buffer name is `[File List]` or `[Buf List]` (not interested in
these buffers normally),
- `"[binary]"` if the buffer has the `binary` option set, else
- `"[<encoding>/<fileencoding>]"` based on the buffer's settings.

If the `fileencoding` is for a Unicode encoding (starts with `ucs` or `utf`)
then it will be prefixed with `bomb:` or `nobomb:` depending on whether the
`bomb` option is set or not.

Installation
============

The recommended approach is use
[Pathogen](https://github.com/tpope/vim-pathogen) and to clone this plugin into
your bundle directory.

License
=======

Copyright (c) 2004-2013 Mike Williams <mrmrdubya@gmail.com>

Permission to use, copy, modify, and distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
