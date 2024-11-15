cmake_minimum_required(VERSION 3.28)
project(glad LANGUAGES CXX C)

add_library(
	glad STATIC
	"src/glad.c"
)

target_compile_features(glad PRIVATE c_std_11)

target_include_directories(
    glad PUBLIC SYSTEM
    "${PROJECT_SOURCE_DIR}/include"
)
