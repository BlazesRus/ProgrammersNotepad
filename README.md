# Programmer's Notepad

[Programmer's Notepad](http://www.pnotepad.org/) is a text editor for Windows.

![Screenshot](http://www.pnotepad.org/images/home1.png)

It is primarily written in C++ and extensible using Python, and is built on the following technologies:
  - [Scintilla](https://www.scintilla.org/)
  - [WTL](http://sourceforge.net/projects/wtl/)
  - [Boost](http://www.boost.org/)

## Getting Started

Clone the tree, then see the [Build Instructions](http://pnotepad.org/docs/dev/how_to_compile_pn/)

## Build in VS 2019

- download and install VS 2019, following [this link](https://visualstudio.microsoft.com/downloads/)
- download / install [git](https://git-scm.com/) and install `vcpkg` on `D` disk
```
d:
cd /
git clone https://github.com/microsoft/vcpkg.git
cd d:/vcpkg
./bootstrap-vcpkg.bat

./vcpkg integrate install

./vcpkg install wtl:x86-windows wtl:x64-windows
./vcpkg install expat:x86-windows expat:x64-windows
./vcpkg install python3:x86-windows python3:x64-windows
./vcpkg install boost-config[core]:x86-windows boost-config[core]:x64-windows
./vcpkg install boost-foreach[core]:x86-windows boost-foreach[core]:x64-windows
./vcpkg install boost-function[core]:x86-windows boost-function[core]:x64-windows
./vcpkg install boost-xpressive[core]:x86-windows boost-xpressive[core]:x64-windows
./vcpkg install boost-phoenix[core]:x86-windows boost-phoenix[core]:x64-windows
./vcpkg install boost-python:x86-windows boost-python:x64-windows
./vcpkg install boost-test[core]:x86-windows boost-test[core]:x64-windows
```
- clone `pn` source code
```
d:
cd /
git clone https://github.com/ssrlive/pn.git
```
- open `pnwtl/pn.sln` with `VS 2019` to make a `Release` build.
- Done
