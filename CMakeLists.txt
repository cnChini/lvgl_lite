cmake_minimum_required(VERSION 3.12.4)

project(lvgl_lite VERSION 8.3.1)

file(GLOB_RECURSE all_source_file src/*.c)

add_library(lvgl_lite STATIC ${all_source_file})

target_include_directories(lvgl_lite PUBLIC ${CMAKE_SOURCE_DIR})
target_compile_definitions(lvgl_lite PUBLIC LV_CONF_INCLUDE_SIMPLE)

