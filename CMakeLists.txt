cmake_minimum_required(VERSION 3.20)

project(
    sliqsys
    LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_subdirectory(src)

execute_process(
    COMMAND bash -c "cd cudd && ./configure --enable-dddmp --enable-obj --enable-shared --enable-static"
    WORKING_DIRECTORY ${PROJECT_SOURCE_DIR}
)
