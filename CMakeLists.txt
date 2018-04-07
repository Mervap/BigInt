cmake_minimum_required(VERSION 2.8.4)

project(BIGINT)

include_directories(${BIGINT_SOURCE_DIR})

add_executable(myBigInt
        big_integer.h
        big_integer.cpp
        big_integer_testing.cpp
        gtest/gtest-all.cc
        gtest/gtest.h
        gtest/gtest_main.cc)

if (CMAKE_COMPILER_IS_GNUCC OR CMAKE_COMPILER_IS_GNUCXX)
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -std=gnu++0x -O2")
    set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -D_GLIBCXX_DEBUG")
endif ()

