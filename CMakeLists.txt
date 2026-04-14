cmake_minimum_required(VERSION 3.14)
project(lsem_log LANGUAGES CXX)


set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(lsem_log)
target_sources(lsem_log PRIVATE src/log.hpp src/log.cpp PUBLIC include/lsem/log/log.hpp)
add_library(lsem::log ALIAS lsem_log)

target_include_directories(lsem_log PUBLIC include/)
target_link_libraries(lsem_log PUBLIC fmt::fmt)
