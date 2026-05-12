cmake_minimum_required(VERSION 3.22.1)

project(sbagen)

add_library(sbagen SHARED sbagen.c)

target_compile_definitions(sbagen PRIVATE BUILD_JNI=1)

find_library(log-lib log)

target_link_libraries(sbagen ${log-lib} m)