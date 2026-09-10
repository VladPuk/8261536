cmake_minimum_required(VERSION 3.10)
project(MyCMakeProject)

add_library(print SHARED util/print.cpp)

target_include_directories(print PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/util)

add_executable(main main.cpp)

target_link_libraries(main PRIVATE print)