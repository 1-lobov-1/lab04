cmake_minimum_required(VERSION 3.4)

project(Solver)

set(CMAKE_CXX_STANDARD 11)

set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(solver STATIC  /home/lobov/1-lobov-1/workspace/projects/lab04/solver_lib/solver.cpp   /home/lobov/1-lobov-1/workspace/projects/lab04/formatter_ex_lib/formatter_ex.cpp   /home/lobov/1-lobov-1/workspace/projects/lab04/formatter_lib/formatter.cpp)
include_directories( //home/lobov/1-lobov-1/workspace/projects/lab04/solver_lib  /home/lobov/1-lobov-1/workspace/projects/lab04/formatter_ex_lib  /home/lobov/1-lobov-1/workspace/projects/lab04/formatter_lib)
add_executable(Solver ${CMAKE_CURRENT_SOURCE_DIR}/equation.cpp)
target_link_libraries(Solver solver)
