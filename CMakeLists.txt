cmake_minimum_required(VERSION 3.10)

project(dummy_cmake_project VERSION 1.0.0 LANGUAGES CXX)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)


set(sample_code
    ${CMAKE_CURRENT_SOURCE_DIR}/sample.cpp
)

add_library(${PROJECT_NAME} STATIC ${sample_code})

target_include_directories(${PROJECT_NAME}
PUBLIC:
    ${CMAKE_CURRENT_SOURCE_DIR}/sample.h
)
