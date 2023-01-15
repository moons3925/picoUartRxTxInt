# Generated Cmake Pico project file

cmake_minimum_required(VERSION 3.13)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

# Initialise pico_sdk from installed location
# (note this can come from environment, CMake cache etc)
set(PICO_SDK_PATH "C:/Users/m3925/Documents/Pico/pico-sdk")

# Pull in Raspberry Pi Pico SDK (must be before project)
include(pico_sdk_import.cmake)

project(picoUartRxTxInt C CXX ASM)

# Initialise the Raspberry Pi Pico SDK
pico_sdk_init()

# Add executable. Default name is the project name, version 0.1

add_executable(picoUartRxTxInt picoUartRxTxInt.c uart_ex.c)

add_compile_options(-std=c11 -O0 -g -Wall)
add_compile_options(-std=c++17 -O0 -g -Wall)

pico_set_program_name(picoUartRxTxInt "picoUartRxTxInt")
pico_set_program_version(picoUartRxTxInt "0.1")

pico_enable_stdio_uart(picoUartRxTxInt 0)
pico_enable_stdio_usb(picoUartRxTxInt 0)

# Add the standard library to the build
target_link_libraries(picoUartRxTxInt pico_stdlib)

pico_add_extra_outputs(picoUartRxTxInt)

