cmake_minimum_required(VERSION 3.16.3)
project(cpp-particle-system)
set(CMAKE_CXX_STANDARD 17)

add_subdirectory(src)

option(BUILD_EXAMPLES "Build examples" ON)

if (BUILD_EXAMPLES)
    MESSAGE(STATUS "Building examples is enabled")
    add_subdirectory(examples)
endif()