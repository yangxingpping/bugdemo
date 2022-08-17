cmake_minimum_required(VERSION 3.23)

PROJECT(bugdemo)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_C_STANDARD 11)


AUX_SOURCE_DIRECTORY(. A)

add_definitions(-DSPDLOG_COMPILED_LIB)

add_executable(bugdemo ${A} )


set_target_properties(bugdemo PROPERTIES VS_GLOBAL_VcpkgEnabled true)

#set_target_properties(bugdemo PROPERTIES VS_Vcpkg_VcpkgConfiguration Debug)

