cmake_minimum_required(VERSION 3.15)
project(c01_leetcode_c C)

set(CMAKE_C_STANDARD 99)

#设置可执行文件输出位置
set(dir ${CMAKE_CURRENT_SOURCE_DIR})
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${dir}/lib")
#set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${dir}/lib")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${dir}/bin")

include_directories(${PROJECT_SOURCE_DIR}/../trilib/inc)
#include_directories(.)

add_subdirectory(l0000.helloworld)
add_subdirectory(l0000.test)
#aux_source_directory(trilib/src DIR_SRC)

#add_executable(c01_leetcode_c main.c ${DIR_SRC})