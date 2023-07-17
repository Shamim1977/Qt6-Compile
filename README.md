![Build Qt6](/qt.png)

## Build Qt6 from Source

[Original Documentation](https://wiki.qt.io/Building_Qt_6_from_Git)

<br>

## 1. Install NodeJS 18.16.1 with Chocolatey

[https://nodejs.org/en/download](https://nodejs.org/en/download)
	

<br>

## 2. Install Git

[https://git-scm.com/downloads](https://git-scm.com/downloads)

<br>


### 3. Install Visual Studio 2022 with C/C++ capabilities


[https://visualstudio.microsoft.com/downloads/](https://visualstudio.microsoft.com/downloads/)

<br>

### 4. Install Python 3.1

[https://www.python.org/downloads/](https://www.python.org/downloads/)

<br>

```
pip install html5lib
```

<br>

### 5. Install C++ compiler supporting C++ 17

[https://github.com/llvm/llvm-project/releases/tag/llvmorg-16.0.0](https://github.com/llvm/llvm-project/releases/tag/llvmorg-16.0.0)

<br>

### 6. Install CMake

[https://cmake.org/download/](https://cmake.org/download/)

<br>

### 7. Other dependencies
	
```
	choco install mingw --version=11.2.0
	choco install ninja
	choco install strawberryperl
	choco install winflexbison
	choco install openssl (optional)
```

<br>

<div>Test GCC, CLang and Perl:</div>

```
	g++ --version	
	gcc --version
	ninja --version
	clang++ --version
	perl --version
```

<div>Microsoft Visual C++ (MSVC):</div>

	check if listed in appwiz.cpl

<br>


### 8. Install GNU GPerf

[https://gnuwin32.sourceforge.net/downlinks/gperf.php](https://gnuwin32.sourceforge.net/downlinks/gperf.php)

Add "GnuWin32\bin" path to system environment variables.

<br>

### 9. Build QT

Windwows:<br>
(Customize paths accordingly.)

```
	git clone git://code.qt.io/qt/qt5.git qt6
	cd qt6

	perl init-repository

	mkdir qt6-build
	cd qt6-build
	"..\qt6\configure.bat" -prefix "D:\Qt-Dev\qt6\qt6-build"
	cmake --build .
	cmake --install .

```

Linux:

```
	mkdir qt6-build
	cd qt6-build
	../qt6/configure -prefix /path/to/install
	cmake --build . --parallel 4
	cmake --install .
```

<br>

### 10. Test:
	
```
	ctest -V -R qlocale
```

<br>

### Special Note

Windows-Specific: Visual Studio 2022, Visual Studio 2019, MinGW 11.2
<br><br>
Linux-Specific: OpenGL developing library (libgl-dev, libegl-dev), libfontconfig1-dev (for fonts to be rendered correctly), libinput-dev (for the XCB platform plugin), and the XCB libraries mentioned in https://doc.qt.io/qt-6/linux-requirements.html


<br><br>

### Developer

Shamim Hossain<br>
sparrowmtm@gmail.com<br>
[https://sparrowtech.org](https://sparrowtech.org)<br>
+880 1758900389