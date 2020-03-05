# chromium-base

from the Google Chromium. That code include:
1. Base component and cross platform wrap, like file\process\thread\path...
2. Some high-performance container.
3. Lightweight smart pointer.
4. Callback and Bind.
5. Message loop and task.
6. Characters and timer.
7. ...

## build
### Windows
1. VS 2017 15.9
2. open chromium-base\src\base.sln 
### Linux
1. CMake 3.6 or higher，GCC 7.3 of higher。  
1. 需要依赖glib，有些Linux发行版不带glib，需要自行安装，安装之后需要修改CMakeLists.txt中BASE\_INCLUDE\_PLATFORM\_DIRECTORIES这个变量所定义的glib头文件目录。
2. 进入scm目录，运行build\_base\_linux.sh脚本编译即可。
### macOS
要求: Xcode 10.1或更高版本  
1. 需要依赖libevent，推荐使用这个版本:https://chromium.googlesource.com/chromium/+/trunk/third_party/libevent  
2. 编译安装完成之后，Xcode打开 chromium-base\src\xcode\base.xcodeproj编译即可。  
3. 如果出现找不到libevent相关头文件或库的编译、链接错误，需要改下Build Setting中头文件和库文件搜索路径。  

## usage
1. include `base\base_export.h`
2. link base.dll/libbase.so/libbase.dylib 

## documents
[https://dev.chromium.org/Home](https://dev.chromium.org/Home)