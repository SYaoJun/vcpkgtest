cmake_minimum_required(VERSION 3.10)
project(abc)

add_executable(main src/main.cpp)

find_package(ZLIB REQUIRED)
find_package(fmt CONFIG REQUIRED)
target_link_libraries(main PRIVATE ZLIB::ZLIB fmt::fmt-header-only)
