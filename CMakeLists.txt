cmake_minimum_required(VERSION 3.17)
project(lul)

set(CMAKE_CXX_STANDARD 14)

find_package(openmesh CONFIG REQUIRED)
add_executable(lul main.cpp)
target_compile_definitions(lul PRIVATE -D_USE_MATH_DEFINES)
message(STATUS "vars: ${OPENMESH_INCLUDE_DIRS} ${OPENMESH_LIBRARIES}")
target_include_directories(lul PRIVATE ${OPENMESH_INCLUDE_DIRS})
target_link_libraries(lul PRIVATE ${OPENMESH_LIBRARIES})