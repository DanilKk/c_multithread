cmake_minimum_required(VERSION 2.8)

include(ExternalProject)

project(final)
set(SOURCE_FILES
    src/main.cpp
)

## Flags
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -DUNIX -Werror -ggdb")

file(MAKE_DIRECTORY /home/box/final)
set( CMAKE_RUNTIME_OUTPUT_DIRECTORY /home/box/final )

add_executable(final ${SOURCE_FILES})
target_link_libraries(final m pthread)
