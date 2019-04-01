# libxplanemp

### Multiplayer library for X-Plane

This is libxplanemp, the multiplayer client code for X-Plane.

See README.MULTIPLAYER for the original README file.

To clone this repository to your local drive, use:
git clone https://github.com/kuroneko/libxplanemp

### Additional Notes

* Included CMakeFiles can be integrated into your project directly

* Make sure you define `XPMP_CLIENT_NAME` and `XPMP_CLIENT_LONGNAME` to
  reflect your client/plugin.
  
### Building

The library needs libpng as an external dependency. This can be easily installed by
using vcpkg. For that, call .\vcpkg install libpng on the command line.
If you want to compile the 64bit version, don't forget to specify the x64-windows triplet.

There is also a problem with the glext.h header file, which cannot be found. This can be downloaded
from https://www.khronos.org/registry/OpenGL/index_gl.php
glext.h needs also the KHR/khrplatform.h header file. Find out in the properties page of the 
libxplanemp project under VC++ directories / Include directories, to which Windows Kits path is pointing,
and copy these two files into this directory.

## License
```
Copyright (c) 2006-2013, Ben Supnik and Chris Serio
Copyright (c) 2015-2017, Christopher Collins
Copyright (c) 2016-2017, Roland Winklmeier & Matthew Sutcliffe

Permission is hereby granted, free of charge, to any person obtaining a
copy of this software and associated documentation files (the "Software"),
to deal in the Software without restriction, including without limitation
the rights to use, copy, modify, merge, publish, distribute, sublicense,
and/or sell copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following conditions:

The above copyright notices and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```
