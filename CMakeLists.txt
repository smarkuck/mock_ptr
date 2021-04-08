cmake_minimum_required(VERSION 3.16.3)

project(mock_ptr)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

if (MSVC)
    add_compile_options(/permissive-)
endif ()

add_library(mock_ptr INTERFACE)
target_include_directories(mock_ptr INTERFACE headers)

add_subdirectory(unitTests)
