cmake_minimum_required(VERSION 3.10)
project(yamlgenpp-example CXX)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
include(${CMAKE_CURRENT_LIST_DIR}/../yamlgenpp.cmake)
add_yamlgenpp_target(config_target ${CMAKE_CURRENT_LIST_DIR}/config.yaml)
add_executable(yamlgenpp-example main.cpp)
target_link_libraries(yamlgenpp-example PRIVATE config_target)
