cmake_minimum_required(VERSION 3.10)

find_package(GTest REQUIRED)

include(GoogleTest)

add_executable(
  gtest_version
  gtest_version.cpp
)

#include_directories(${CMAKE_SOURCE_DIR}../)
target_include_directories(gtest_version
    PRIVATE "${CMAKE_SOURCE_DIR}"
)

target_link_libraries(
  gtest_version
  GTest::GTest
  helloworld

)




