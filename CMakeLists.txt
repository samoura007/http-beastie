cmake_minimum_required(VERSION 3.10)
project(MyProject)

set(CMAKE_CXX_STANDARD 17)

find_package(Boost REQUIRED COMPONENTS system)

file(GLOB SOURCES "src/*.cpp")
add_executable(a ${SOURCES})

target_include_directories(a PRIVATE include)

target_link_libraries(a PRIVATE Boost::system)
