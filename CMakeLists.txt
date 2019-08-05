cmake_minimum_required(VERSION 3.2)

include("cmake/HunterGate.cmake")
HunterGate(
    URL "https://github.com/ruslo/hunter/archive/v0.23.205.tar.gz"
    SHA1 "eba80d3028c856c6bedb5d8d9627b1b3bba19634"
)

project(convenience-demo)

add_subdirectory(convenience)

add_executable(demo demo.cpp)

target_link_libraries(demo PRIVATE convenience)
