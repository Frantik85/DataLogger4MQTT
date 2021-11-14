cmake_minimum_required(VERSION 3.10)

project(DataLogger4MQTT)
#
# CMake Toolchain file for crosscompiling on ARM.
#
# Target operating system name.
set(CMAKE_SYSTEM_NAME Linux)
set(CMAKE_SYSTEM_PROCESSOR arm)

# Name of C compiler.
set(CMAKE_C_COMPILER "/usr/bin/arm-linux-gnueabihf-gcc")
set(CMAKE_CXX_COMPILER "/usr/bin/arm-linux-gnueabihf-g++")
#set(CMAKE_C_COMPILER "/usr/bin/aarch64-linux-gnu-gcc-9")
#set(CMAKE_CXX_COMPILER "/usr/bin/aarch64-linux-gnu-g++-9")
# Where to look for the target environment. (More paths can be added here)
#set(CMAKE_FIND_ROOT_PATH /usr/aarch64-linux-gnu)
#set(CMAKE_SYSROOT /usr/aarch64-linux-gnu)

# Adjust the default behavior of the FIND_XXX() commands:
# search programs in the host environment only.
set(CMAKE_FIND_ROOT_PATH_MODE_PROGRAM NEVER)

# Search headers and libraries in the target environment only.
#set(CMAKE_FIND_ROOT_PATH_MODE_LIBRARY ONLY)
#set(CMAKE_FIND_ROOT_PATH_MODE_INCLUDE ONLY)
#set(CMAKE_FIND_ROOT_PATH_MODE_PACKAGE ONLY)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_executable(DataLogger4MQTT main.cpp)

