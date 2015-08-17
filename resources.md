---
layout: default
title: "Resources"
---

This page contains links to useful resources.

-   [Visual Studio 2013](http://e5.onthehub.com/WebStore/ProductsByMajorVersionList.aspx?ws=5d805b88-ce9b-e011-969d-0030487d8897&vsro=8&JSEnabled=1) is available through MSDNAA.
-   [FreeGLUT](http://freeglut.sourceforge.net/) the OpenGL window management package we will be using. The package is targetted to Linux, but you can get a distribution for [Windows](http://www.transmissionzero.co.uk/software/freeglut-devel/) (this package will also work on VS 2013).
-   [SOIL](http://www.lonesock.net/soil.html) the Simple OpenGL Image Library package we will be using. I have precompiled libraries for Windows and Mac OSX that can be downloaded in the corresponding installation section below.
-   [GLEW](http://glew.sourceforge.net/) the OpenGL Extension Wrangler Library package we will be using for shaders (since Windows contains an old version of OpenGL). NOTE: OSX contains a current version of OpenGL and thus does not require GLEW.

FreeGLUT Installation Instructions
----------------------------------

**Windows 7 (Visual Studio 2013)**

1.  Download and extract [freeglut 2.8.1-1 for MSVC](http://www.transmissionzero.co.uk/software/freeglut-devel/).

2.  Copy the contents of the **include\\GL** directory to:
> -   (32-bit) C:\\Program Files\\Windows Kits\\8.1\\Include\\um\\gl
> -   (64-bit) C:\\Program Files (x86)\\Windows Kits\\8.1\\Include\\um\\gl

3.  Copy **freeglut.lib** from the **lib** directory (**NOT** the x64 subdirectory) to:
> -   (32-bit) C:\\Program Files\\Windows Kits\\8.1\\Lib\\win8\\um\\x86
> -   (64-bit) C:\\Program Files (x86)\\Windows Kits\\8.1\\Lib\\win8\\um\\x86

4.  Copy **freeglut.dll** from the **bin** directory (**NOT** the x64 subdirectory) to:
> -   (32-bit) C:\\Windows\\System32
> -   (64-bit) C:\\Windows\\SysWOW64

**Windows 8.1 (Visual Studio 2013)**

1.  Download and extract [freeglut 2.8.1-1 for MSVC](http://www.transmissionzero.co.uk/software/freeglut-devel/).

2.  Copy the contents of the **include\\GL** directory to:
> -   C:\\Program Files (x86)\\Windows Kits\\8.1\\Include\\um\\gl

3.  Copy **freeglut.lib** from the **lib** directory (**NOT** the x64 subdirectory) to:
> -   C:\\Program Files (x86)\\Windows Kits\\8.1\\Lib\\winv6.3\\um\\x86

4.  Copy **freeglut.dll** from the **bin** directory (**NOT** the x64 subdirectory) to:
> -   C:\\Windows\\SysWOW64

**Linux (ubuntu)**

From a terminal window

```cpp
$ sudo apt-get install freeglut3-dev
```

**Mac OSX**

Install [XCode](https://developer.apple.com/xcode/downloads/) which includes OSX GLUT libraries.

SOIL Installation Instructions
------------------------------

**Windows 7 (Visual Studio 2013)**

1.  Copy the header file in the links to (you will need to make a new **SOIL** directory):
> -   [(32-bit header)](soil/win32/SOIL.h) C:\\Program Files\\Windows Kits\\8.1\\Include\\um\\SOIL
> -   [(64-bit header)](soil/win64/SOIL.h) C:\\Program Files (x86)\\Windows Kits\\8.1\\Include\\um\\SOIL

2.  Copy the library in the links to:
> -   [(32-bit library)](soil/win32/SOIL.lib) C:\\Program Files\\Windows Kits\\8.1\\Lib\\win8\\um\\x86
> -   [(64-bit library)](soil/win64/SOIL.lib) C:\\Program Files (x86)\\Windows Kits\\8.1\\Lib\\win8\\um\\x86

**Windows 8.1 (Visual Studio 2013)**

1.  Copy the header file in the links to (you will need to make a new **SOIL** directory):
> -   [SOIL.h](soil/win64/SOIL.h) C:\\Program Files (x86)\\Windows Kits\\8.1\\Include\\um\\SOIL

2.  Copy the library in the links to:
> -   [SOIL.lib](soil/win64/SOIL.lib) C:\\Program Files (x86)\\Windows Kits\\8.1\\Lib\\winv6.3\\um\\x86

**Linux (ubuntu)**

From a terminal window

```cpp
$ sudo apt-get install libsoil-dev
```
	
**Mac OSX**

1.  Download the [mac header](soil/mac/SOIL.h).

2.  In a terminal window, from the directory where you downloaded the header file:

	```cpp
	$ sudo mkdir /usr/local/include/SOIL
	
	$ sudo cp SOIL.h /usr/local/include/SOIL/
	```

3.  Download [libSOIL.a](soil/mac/libSOIL.a).

4.  In a terminal window, from the directory where you downloaded the library:

	```cpp
	$ sudo cp libSOIL.a /usr/local/lib/
	```
	
GLEW Installation Instructions
------------------------------

**Windows 7 (Visual Studio 2013)**

1.  Download and extract (be sure to get the Windows 32-bit version even if you are running a 64-bit OS) [precompiled binaries](https://sourceforge.net/projects/glew/files/glew/1.9.0/glew-1.9.0-win32.zip/download).

2.  Copy the contents of the **include\\GL** directory to:
> -   (32-bit) C:\\Program Files\\Windows Kits\\8.1\\Include\\um\\gl
> -   (64-bit) C:\\Program Files (x86)\\Windows Kits\\8.1\\Include\\um\\gl

3.  Copy **glew32.lib** in the **lib** directory to:
> -   (32-bit) C:\\Program Files\\Windows Kits\\8.1\\Lib\\win8\\um\\x86
> -   (64-bit) C:\\Program Files (x86)\\Windows Kits\\8.1\\Lib\\win8\\um\\x86

4.  Copy **glew32.dll** in the **bin** directory to:
> -   (32-bit) C:\\Windows\\System32
> -   (64-bit) C:\\Windows\\SysWOW64

**Windows 8.1 (Visual Studio 2013)**

1.  Download and extract (be sure to get the Windows 32-bit version even if you are running a 64-bit OS) [precompiled binaries](https://sourceforge.net/projects/glew/files/glew/1.9.0/glew-1.9.0-win32.zip/download).

2.  Copy the contents of the **include\\GL** directory to:
> -   C:\\Program Files (x86)\\Windows Kits\\8.1\\Include\\um\\gl

3.  Copy **glew32.lib** in the **lib** directory to:
> -   C:\\Program Files (x86)\\Windows Kits\\8.1\\Lib\\winv6.3\\um\\x86

4.  Copy **glew32.dll** in the **bin** directory to:
> -   C:\\Windows\\SysWOW64

**Linux (ubuntu)**

From a terminal window

```cpp
$ **sudo apt-get install libglew-dev**
```

**Mac OSX**

GLEW is not needed for OSX.



