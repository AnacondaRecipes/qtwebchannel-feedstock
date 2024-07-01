cmake_minimum_required (VERSION 3.0)

set (CMAKE_BUILD_TYPE "Release" CACHE STRING "build type")

project (qtwebchannel-test CXX)

find_package (Qt6 CONFIG REQUIRED COMPONENTS WebChannel)

add_executable (test_qtwebchannel test_qtwebchannel.cpp)
target_link_libraries (test_qtwebchannel Qt6::WebChannel)

enable_testing ()
add_test (NAME test_qtwebchannel COMMAND test_qtwebchannel)
