cmake_minimum_required(VERSION 3.8)
project(graph500 LANGUAGES C)

find_package(OpenMP REQUIRED)
add_subdirectory(generator)

add_library(graph500::generator ALIAS generator)
