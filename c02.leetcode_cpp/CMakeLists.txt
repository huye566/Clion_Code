cmake_minimum_required(VERSION 3.15)
project(c02_leetcode_cpp)

set(CMAKE_CXX_STANDARD 14)
set(GOOGLETEST_VERSION 1.10.0)

#设置可执行文件输出位置
set(dir ${CMAKE_CURRENT_SOURCE_DIR})
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${dir}/lib")
#set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${dir}/lib")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${dir}/bin")

# Set Compiler，指定编译为32位程序
#SET(CMAKE_C_FLAGS "-m32")
#SET(CMAKE_CXX_FLAGS "-m32")

#外部头文件引用
include_directories(${PROJECT_SOURCE_DIR}/../trilib/inc)
#外部源码引用
aux_source_directory(${PROJECT_SOURCE_DIR}/../trilib/src TRILIB_SOURCE)

# 编译google test，会在当前目录生成libtest.a动态库,非子目录需要缓存目录gtest.out
add_subdirectory(../googletest-master/googletest gtest.out)
# 将用于google test的头文件gtest.h添加到include路径中,
include_directories(${CMAKE_CURRENT_LIST_DIR}/../googletest-master/googletest/include)

set(LIBRARIES gtest pthread)

add_subdirectory(ut00.test00)

