# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.13.1)


set(ZEPHYR_TOOLCHAIN_VARIANT "espressif")
#export ESPRESSIF_TOOLCHAIN_PATH="/path/to/xtensa-esp32-elf/"

list(APPEND BOARD_ROOT ${CMAKE_CURRENT_SOURCE_DIR})


find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(nodemcu-esp32-blinky)

target_sources(app PRIVATE src/main.c)
