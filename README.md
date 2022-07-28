# avr-toolchain.cmake
Modern CMake (3.21+) toolchain file for AVR microcontroller. This toolchain file make use of GNU and open source AVR project i.e. avr-gcc, avr-libc and avrdude

# Usage

A simple project is provided in [example](./example) directory. Do the following to compile and upload to the target microcontroller.

```console
cd example
cmake -S . -B build --toolchain ../avr-toolchain.cmake
cmake --build build
```

Project configuration settings include the target microcontroller type (-mmcu), frequency (-DF_CPU) and avrdude arguments. Edit the ```CMakeCache.txt``` file or use any CMake project configuration tool. 

```console
ccmake build
```

Useful commands has been added as custom target. These includes dumping EEPROM content, programming AVR fuse and bitlock. The list of target provides all available commands.

```console
cmake --build build --target help
```

# To Do
1. Add wrapper function for add_library()

# Alternatives
1. [mkleemann/cmake-avr](https://github.com/mkleemann/cmake-avr)
2. [Using CMake to deploy to avr microcontrollers](https://www.kuon.ch/post/2018-07-11-avr-cmake/)
3. [AVR CMake Toolchain](https://nnarain.github.io/2016/03/29/AVR-CMake-Toolchain.html)
