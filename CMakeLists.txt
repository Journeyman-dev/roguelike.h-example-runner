cmake_minimum_required(VERSION 3.19)

project(rlh_example_runner)

add_subdirectory(extern)
set(RLH_BUILD_EXAMPLE ON)
add_subdirectory(roguelike.h)
