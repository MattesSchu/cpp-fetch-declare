cmake_minimum_required(VERSION 3.20)

project(cpp-fetch-declare)

add_library(test-lib STATIC test-lib.cpp)

target_include_directories(test-lib 
    PUBLIC 
        ${CMAKE_CURRENT_SOURCE_DIR}
)

set(CMAKE_INSTALL_PREFIX ${CMAKE_BINARY_DIR}/install)
install(TARGETS test-lib DESTINATION lib)
install(FILES test-lib.h DESTINATION include)

