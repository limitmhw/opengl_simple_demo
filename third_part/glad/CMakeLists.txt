cmake_minimum_required( VERSION 3.4.0 )

project(External.Glad)

add_library(Glad STATIC ${CMAKE_CURRENT_SOURCE_DIR}/glad.c)

target_sources(Glad
    PRIVATE "glad.c" "khrplatform.h"
    PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/glad.h"
    )

target_include_directories(Glad PUBLIC .)
target_compile_features(Glad PUBLIC c_std_99)