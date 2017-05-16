# PartA.ssr-server for Windows

## Compiling environment:Windows OS

#### 1.Download and install python2.7 and set up the environment PATH.

<https://www.python.org/downloads/release/python-2713/>

#### 2.Download pyinstaller and install by python command.

<https://github.com/pyinstaller/pyinstaller/releases/download/v3.2.1/PyInstaller-3.2.1.zip>

     python setup.py install

#### 3.Compile the ssr-server.exe.(the target file is "dist") 

    pyinstaller ssr_server.spec


# PartB.ssr-client for Windows

## Compiling environment:Windows OS

#### 1.Download and install msys2 for windows.

<https://sourceforge.net/projects/msys2/>

#### 2.Update your packages to the latest version and install the dependencies

    pacman -Syu
    pacman -S git base-devel mingw-w64-i686-headers mingw-w64-i686-winpthreads mingw-w64-i686-gcc mingw-w64-i686-binutils mingw-w64-i686-pcre mingw-w64-i686-readline mingw-w64-i686-openssl-devel

#### 3.git clone the latest version and prepare to compile. (use --prefix to specify the installing path)

    git clone https://github.com/shadowsocksr/shadowsocksr.git
    cd shadowsocksr
    ./configure --prefix=/root
    make
    make install

#### 4.Copy the dll file into the ssr-local folder. (find them from C:\msys64\ )

    libeay32.dll
    libgcc_s_dw2-1.dll
    libpcre-1.dll
    libssp-0.dll
    libwinpthread-1.dll


### **Old driver will take you go!!** 
    you may download ssr-server & ssr-local binary files from here!
<https://github.com/letssudormrf/ssr-exe/releases>
