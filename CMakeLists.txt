cmake_minimum_required(VERSION 3.20)
project(OpenGL VERSION 0.1.0 DESCRIPTION "My app")

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_BINARY_DIR ${CMAKE_SOURCE_DIR}/bin)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR})
set(SOURCE_FILES src/main.cpp src/gl.c)

add_executable(opengl ${SOURCE_FILES})
target_include_directories(opengl PRIVATE include)
target_link_directories(opengl PRIVATE lib)
target_link_libraries(opengl glfw3 GL X11 pthread dl)
