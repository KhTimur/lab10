cmake_minimum_required(VERSION 3.0)

set(CMAKE_CXX_STANDARD 11)

include(cmake/HunterGate.cmake)

HunterGate(
    URL "https://github.com/KhTimur/lab09/releases/download/v0.1.0.1/insert-Linux-x86_64.tar.gz"
    SHA1 "2edb426b09a0d774a5507f5803db86d7148cdcce"
)

project(insert-demo)

hunter_add_package(insert)
find_package(insert CONFIG REQUIRED)

include_directories(${INSERT_ROOT}/include)

add_executable(demo ${CMAKE_CURRENT_SOURCE_DIR}/sources/demo.cpp)
target_link_libraries(demo insert)

install(TARGETS demo RUNTIME DESTINATION bin)
