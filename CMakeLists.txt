cmake_minimum_required(VERSION 3.13)
set(CMAKE_VERBOSE_MAKEFILE OFF)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
include(FetchContent)
FetchContent_Declare(
	pico-sdk
	GIT_REPOSITORY https://github.com/raspberrypi/pico-sdk.git
	GIT_SUBMODULES_RECURSE OFF)
FetchContent_MakeAvailable(pico-sdk)

include(${pico-sdk_SOURCE_DIR}/external/pico_sdk_import.cmake)
pico_sdk_init()

project(com LANGUAGES C CXX ASM)
add_subdirectory(src)
add_subdirectory(lib)





