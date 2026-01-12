cmake_minimum_required(VERSION 3.10)

project(data_structures_and_algorithms C)

set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED ON)

include_directories(${CMAKE_SOURCE_DIR}/include)

file(GLOB_RECURSE ALGO_SOURCES "src/*.c")

add_library(algo_core ${ALGO_SOURCES})

add_executable(run_test test/vector_main.c)

target_link_libraries(run_test algo_core)