cmake_minimum_required(VERSION 3.10)
project(my_project)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(GTest REQUIRED)

enable_testing()

add_executable(test_prime test_prime.cpp)
target_link_libraries(test_prime GTest::gtest_main)

include(GoogleTest)
gtest_discover_tests(test_prime)
