cmake_minimum_required(VERSION 3.10)
project(cpp-base64 VERSION 1.0.0 LANGUAGES CXX)

# Add library
add_library(cpp-base64 STATIC
    base64.cpp
)

# Set include directories - use relative path
target_include_directories(cpp-base64
    PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
        $<INSTALL_INTERFACE:include>
)

# Set C++ standard
set_target_properties(cpp-base64 PROPERTIES
    CXX_STANDARD 11
    CXX_STANDARD_REQUIRED ON
)
