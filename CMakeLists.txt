cmake_minimum_required(VERSION 3.15)
project(test)

set(CMAKE_CXX_STANDARD 11)

set(OpenGlLinkers -lglut -lGLU -lGL -lglfw -lGLEW -lSOIL)

add_executable(test main.cpp Shader.h)

target_link_libraries(test ${OpenGlLinkers})