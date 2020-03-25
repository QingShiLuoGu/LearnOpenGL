cmake_minimum_required(VERSION 3.15)
project(test)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_CURRENT_SOURCE_DIR}/cmake)

find_package(glm REQUIRED)
include_directories( ${GLM_INCLUDE_DIRS} )

set(OpenGlLinkers -lglut -lGLU -lGL -lglfw -lGLEW -lSOIL)

add_executable(test main.cpp Shader.h)

target_link_libraries(test ${OpenGlLinkers})