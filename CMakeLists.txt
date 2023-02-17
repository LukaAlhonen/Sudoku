cmake_minimum_required(VERSION 3.25.2)

project(Sudoku)

set(CMAKE_CXX_STANDARD 17)

add_executable(app main.cc)

find_package(PkgConfig)
pkg_check_modules(GTKMM_VARS REQUIRED IMPORTED_TARGET gtkmm-4.0)

target_link_libraries(app PRIVATE PkgConfig::GTKMM_VARS)
