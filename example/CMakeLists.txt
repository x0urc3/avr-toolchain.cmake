cmake_minimum_required(VERSION 3.21)

project("example")
add_library(led led.c)
setup_avr_target(led)

add_executable(firmware main.c led)
setup_avr_target(firmware)
