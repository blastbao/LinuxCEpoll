cmake_minimum_required(VERSION 3.5)
project(eserver)
include_directories(${PROJECT_SOURCE_DIR}) #like gcc: -I
set(CMAKE_C_FLAGS "-Wall -DDEBUG")
file(GLOB sources "*.c")
file(GLOB headers "*.h")
#aux_source_directory(. DIR_SRCS)
add_executable(eserver ${sources} ${headers})
#  here must be dynamic  libraries
target_link_libraries(eserver pthread)
target_link_libraries(eserver mysqlclient)
