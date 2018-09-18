cmake_minimum_required(VERSION 3.0)

set(CMAKE_CXX_STANDARD 11)

include(cmake/HunterGate.cmake)

HunterGate(
    URL "https://github.com/KhTimur/hunter/archive/0.23.27.1.tar.gz"
    SHA1 "66cc630b8e2584cb68146ee1e27125fec956d9d7"
)
