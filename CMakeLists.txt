cmake_minimum_required (VERSION 2.8)
cmake_policy(VERSION 2.8)

project (LearnOpenGL)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/includes)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/third_part)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/third_part/glfw/include)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/third_part/glad glad)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/third_part/glfw glfw)

link_directories(${CMAKE_CURRRENT_BINARY_DIR}/glad)
link_directories(${CMAKE_CURRRENT_BINARY_DIR}/glfw)

add_executable(testopengl ${CMAKE_CURRENT_SOURCE_DIR}/hello_window.cpp)
target_link_libraries(testopengl glfw Glad)