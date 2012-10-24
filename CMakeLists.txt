
cmake_minimum_required(VERSION 2.6)
if ("${CMAKE_CXX_COMPILER_ID}" STREQUAL "Clang")
  option(USE_CLANG "build application with clang" ON)  # using Clang
endif()

project (clang_visit)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/Modules/")

find_package(LibClang REQUIRED)

include_directories(
    SYSTEM
    ${LibClang_INCLUDE_DIRS}
)

add_executable(clang_visitor clang_visitor.c)
target_link_libraries(clang_visitor
    ${LibClang_LIBRARIES}
)
