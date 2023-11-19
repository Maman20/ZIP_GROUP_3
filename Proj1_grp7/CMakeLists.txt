cmake_minimum_required(VERSION 3.26)
project(ZipCodes)

set(CMAKE_CXX_STANDARD 17)

# Copy "us_postal_codes.csv" to the build directory
configure_file(${CMAKE_SOURCE_DIR}/us_postal_codes.csv ${CMAKE_BINARY_DIR}/us_postal_codes.csv COPYONLY)

# Copy "us_postal_codes_place.csv" to the build directory
configure_file(${CMAKE_SOURCE_DIR}/us_postal_codes_place.csv ${CMAKE_BINARY_DIR}/us_postal_codes_place.csv COPYONLY)

add_executable(ZipCodes main.cpp
        CSVReader.cpp
        CSVReader.h
)
