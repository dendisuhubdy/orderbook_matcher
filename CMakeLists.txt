cmake_minimum_required(VERSION 3.8.0)
project (matching_engine)
set(CMAKE_BUILD_TYPE Release)

set (CMAKE_CXX_STANDARD 11)

# Bring the headers
include_directories(include)

# Adding all sources
file(GLOB SOURCES "src/*.cpp")

#Generate the shared library from the sources
#add_library(exchange SHARED ${SOURCES})

add_executable (matching_engine ${SOURCES})
TARGET_LINK_LIBRARIES(matching_engine)

install(TARGETS matching_engine DESTINATION /usr/local/bin)
