# MinGW_12.2.0
MinGW将经典的开源 C语言 编译器 GCC 移植到了 Windows 平台下，并且包含了 Win32API ，因此可以将源代码编译为可在 Windows 中运行的可执行程序。而且还可以使用一些 Windows 不具备的，Linux平台下的开发工具。一句话来概括：MinGW 就是 GCC 的 Windows 版本 。MinGW-w64 与 MinGW 的区别在于 MinGW 只能编译生成32位可执行程序，而 MinGW-w64 则可以编译生成 64位 或 32位 可执行程序。正因为如此，MinGW 现已被 MinGW-w64 所取代，且 MinGW 也早已停止了更新，内置的 GCC 停滞在了 4.8.1 版本，而 MinGW-w64 内置的 GCC 则更新到了12.2.0 版本现在的MinGW-w64分支很多 ，简要了解一下各版本之间的区别。
+ "I686"意指适用于32位操作系统的的程序包。

+ "12.2.0"意指当前程序包版本位12.2.0。

+ "posix"适用于基于Linux kernel 开发而来的操作系统，如linux，macos。
    + posix: 启用 c++11/c11多线程功能。 依赖于 libwinpthreads，即使你不直接调用 API，也将分发给 winpthreads 。 使用应用程序分发一个DLL没有什么问题。

+ "win32"适用于基于windows开发而来的操作系统，如windows。
    + win32: 没有C++11多线程功能。对任何调用 Win32 api或者 pthreads api的代码都不影响。 你可以同时使用。
+ "dwarf,seh,sjlj"这些都是异常处理模型，其中dwarf仅支持32的操作系统，性能较强；seh仅支持64位的操作系统，性能较强；sjlj同时支持32位和64位操作系统，但性能较差。

+ "msvcrt" 在较老的windows操作系统（win10之前），较低版本的visual studio（2017之前）上使用。

+ "ucrt"在较新的操作系统和visual studio上使用。

下载好对应的MinGW-W64后解压到目标文件夹下（这个由自己定），然后将mingw下的bin文件夹所在的位置添加到系统环境变量中并在终端中通过 gcc -v 检查是否配置成功。

[参考网站](https://www.cnblogs.com/duruofei/p/15674502.html)
[文件源网站](https://github.com/niXman/mingw-builds-binaries/releases)
