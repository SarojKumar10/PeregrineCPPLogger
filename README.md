# PeregrineCPPLogger

A simple logging library written in C++17.

# Building

Make sure you have [CMake 3.14+](https://cmake.org) installed on your system.

**Note**: The instructions here use CMake command line interface. The project can also be built using [CMake GUI](https://cmake.org/cmake/help/latest/manual/cmake-gui.1.html).

## Windows

**Note**: The instructions here are for Visual Studio 2017+. You can use any other [CMake Generator](https://cmake.org/cmake/help/latest/manual/cmake-generators.7.html).

Make sure `cmake` is in your `PATH`.

Open command prompt in the root project directory and execute the following commands:
1. `mkdir build && cd build`
2. `cmake .. -G "Visual Studio <vs_version>"` or `cmake .. -G "Visual Studio <vs_version>" -DCMAKE_BUILD_TYPE=<config>`. See below for which one to use.

The solution file is generated. Open it with Visual Studio and build it.
`<vs_version>` must be `15 2017` or higher as this project uses C++17.

## Linux

**Note**: The instructions here are for GNU Make. You can use any other [CMake Generator](https://cmake.org/cmake/help/latest/manual/cmake-generators.7.html).

[GNU Make](https://www.gnu.org/software/make/) is required. It is usually preinstalled on most linux systems.  
Run `make -v` in terminal to check if it is installed.

Open terminal in the root project directory and execute the following commands:
1. `mkdir build && cd build`
2. `cmake ..` or `cmake .. -DCMAKE_BUILD_TYPE=<config>`. See below for which one to use.
3. `make all`

**Note for Mac users**: The library "should" work fine on MacOS. Currently, I have no way to test the building process or the project on MacOS
because I do not have a Mac. So, any help on that is welcome.

The libraries should be inside `lib/<config>/<os_name>/<architecture>/` where  
* `<config>` is Release by default. Refer to [this](https://cmake.org/cmake/help/latest/variable/CMAKE_BUILD_TYPE.html) for possible values for `<config>`.
* `<os_name>` is the name of your Operating System. Example - `Windows`, `Linux` etc.
* `<architecture>` is the architecture of your CPU. Example - `x86`,`x86_64` etc.