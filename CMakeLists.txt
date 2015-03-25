cmake_minimum_required(VERSION 2.8)
project(printmess)

set(Boost_USE_STATIC_LIBS ON)
set(Boost_USE_MULTITHREAD ON)
set(Boost_USE_STATIC_RUNTIME OFF)

find_package(Boost 1.32 COMPONENTS program_options)
if(Boost_FOUND)
  add_executable(printmess main.cpp)
endif()

add_library(mess1 SHARED mess1.cpp)
add_library(mess2 SHARED mess2.cpp)
add_library(mess3 SHARED mess3.cpp)
