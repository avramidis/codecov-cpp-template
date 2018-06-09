#---------------------------------------------------------------------------//
# Copyright (c) 2018 Eleftherios Avramidis <el.avramidis@gmail.com>
#
# Distributed under The MIT License (MIT)
# See accompanying file LICENSE.txt
#---------------------------------------------------------------------------//

cmake_minimum_required (VERSION 3.2.2)

set(default_build_type "Debug")

# if(NOT CMAKE_BUILD_TYPE AND NOT CMAKE_CONFIGURATION_TYPES)
#   message(STATUS "Setting build type to '${default_build_type}' as none was specified.")
#   set(CMAKE_BUILD_TYPE "${default_build_type}" CACHE
#       STRING "Choose the type of build." FORCE)
#   # Set the possible values of build type for cmake-gui
#   set_property(CACHE CMAKE_BUILD_TYPE PROPERTY STRINGS
#     "Debug" "Release" "MinSizeRel" "RelWithDebInfo")
# endif()

# Select flags.
# SET(CMAKE_CXX_FLAGS_RELWITHDEBINFO "-O2 -g")
# SET(CMAKE_CXX_FLAGS_RELEASE "-O2")
# SET(CMAKE_CXX_FLAGS_DEBUG  "-O0 -g")

project(codecovexample LANGUAGES CXX)
set(CMAKE_CXX_FLAGS "-Wall -pedantic -pthread -g -O0 -fprofile-arcs -ftest-coverage")
set(CMAKE_CXX_STANDARD 14)
add_executable(codecovexample "${CMAKE_CURRENT_SOURCE_DIR}/codecovexample.cpp")

# Add all warnings compile options
# if (MSVC)
# 	add_compile_options(/W4)
# else()
# 	add_compile_options(-Wall -Wextra -Wpedantic --coverage)
# endif()



#TARGET_LINK_LIBRARIES(codecovexample "-lgcov")

# MESSAGE(STATUS "CMAKE_CURRENT_BINARY_DIR: " ${CMAKE_CURRENT_BINARY_DIR})
# MESSAGE(STATUS "CMAKE_CURRENT_SOURCE_DIR : " ${CMAKE_CURRENT_SOURCE_DIR})
# MESSAGE(STATUS "PROJECT_NAME  : " ${PROJECT_NAME})
# MESSAGE(STATUS "CMAKE_COMMAND  : " ${CMAKE_COMMAND})
# MESSAGE(STATUS "CONFIGURATION  : " ${CMAKE_BUILD_TYPE})

