# Introduction #

Building FoFLyricConverter from source requires some of the same tools needed for building EOF:
  1. A GCC style compiler.  For Windows, use MinGW (http://sourceforge.net/projects/mingw/).  Make sure that it installs properly so that gcc can be called from any directory.
  1. Optionally, you can use CMake to build the converter if you like (http://www.cmake.org/)
  1. A make system.  This usually comes with your Linux OS or compiler

The converter's source code is available with EOF's source code, so use your favorite SVN client to download the source code for EOF.  In Windows, I find that TortoiseSVN (http://tortoisesvn.net/) works very well.

# Building with make #

Change to the foflc directory from within EOF's source folder, ie:
```
cd c:\eof\src\foflc
```
For Windows, use MinGW's make program:
```
mingw32-make -f makefile.mingw
```
For Mac, I assume it's just called make, in which case use:
```
make -f makefile.mingw
```
For Linux, use:
```
make -f makefile.linux
```

If all goes well, you should have an executable file ready to use!

# Building with cmake #

Cmake is a little more complex, but if you build EOF, you already have it anyway.  Ensure that cmake is in your PATH environment variable so you can call it from any directory.  Change to foflc's build directory and delete its contents if it is not already empty, ie:
```
cd c:\eof\src\foflc\build
del *.*
```
For Mac or Windows, use this command:
```
cmake -G "MinGW Makefiles" ..
```
For Linux, use:
```
cmake -G "Unix Makefiles" ..
```
Then, regardless of which OS you have, this is the last command you need:
```
make
```

If it works, you'll have the executable file.