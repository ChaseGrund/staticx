StaticX
=======
Bundle dynamic executables with their library dependencies so they can be run
anywhere, just like a static executable.

## Requirements
The following external tools need to be installed to run StaticX:
- `ldd` - Part of GNU C Library
- `readelf` - Part of binutils
- `objcopy` - Part of binutils
- [`patchelf`](patchelf)
   - Packages available for Debian 8+, Fedora 14+, others

The following additional tools must be installed to build StaticX from source:
- `scons`
- [`musl-libc`](musl-libc) *(optional)*


## Installation

*StaticX is not yet available on PyPi.*

You can install using Pip.
StaticX is compatible with Python 2 (`pip`) or Python 3 (`pip3`):
```
sudo pip3 install https://github.com/JonathonReinhart/staticx/archive/master.zip
```

If you have musl libc installed, you can use it to build the staticx
bootloader, resulting in smaller, better binaries. Simply set the `CC`
environment variable to your `musl-gcc` wrapper path:
```
sudo CC=/usr/local/musl/bin/musl-gcc pip3 install https://github.com/JonathonReinhart/staticx/archive/master.zip
```


[patchelf]: https://nixos.org/patchelf.html
[musl-libc]: https://www.musl-libc.org/
