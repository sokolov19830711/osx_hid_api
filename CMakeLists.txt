cmake_minimum_required(VERSION 3.0.0)

project(osx_hid_api VERSION 0.1.0)

find_library(CoreFoundationLib CoreFoundation)
find_library(IOKitLib IOKit)

add_executable(osx_hid_api main.c hidapi.c rs_hid.c)
target_link_libraries(osx_hid_api ${CoreFoundationLib} ${IOKitLib})
