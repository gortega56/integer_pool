cmake_minimum_required(VERSION 3.26.0)

project(integer_pool LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_library(integer_pool INTERFACE)
	
target_sources(integer_pool
	PRIVATE
	${CMAKE_CURRENT_SOURCE_DIR}/include/integer_pool.h
	${CMAKE_CURRENT_SOURCE_DIR}/include/integer_coder.h
)

target_include_directories(integer_pool
  INTERFACE
    ${CMAKE_CURRENT_LIST_DIR}/include)
