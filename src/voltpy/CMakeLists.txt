cmake_minimum_required(VERSION 3.20)

file(GLOB_RECURSE TARGET_SOURCES CONFIGURE_DEPENDS
	"${CMAKE_CURRENT_SOURCE_DIR}/include/*.hpp"
    "${CMAKE_CURRENT_SOURCE_DIR}/src/*.hpp"
    "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp"
)

add_library(voltpy ${TARGET_SOURCES})

set_property(TARGET voltpy PROPERTY CXX_STANDARD 20)
