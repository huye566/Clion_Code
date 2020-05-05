cmake_minimum_required(VERSION 3.15)
project(c00_helloworld)

set(CMAKE_CXX_STANDARD 14)

#设置可执行文件输出位置
set(dir ${CMAKE_CURRENT_SOURCE_DIR})
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${dir}/lib")
#set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${dir}/lib")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${dir}/bin")

add_executable(c00_helloworld
        helloworld.cpp)
