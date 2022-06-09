cmake_minimum_required(VERSION 3.8)
project(Test_rdlock)

set(CMAKE_CXX_STANDARD 17)

# enable_testing()
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -D__CMAKE_FILE__='\"$(notdir $(abspath $<))\"'")

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bins)
set(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/libs)

include_directories(
        ${PROJECT_BINARY_DIR}/include
        ${PROJECT_SOURCE_DIR}/
)

link_directories(
        ${PROJECT_BINARY_DIR}/lib
)

add_subdirectory(tar)
add_subdirectory(redis-plus-plus)
# add_subdirectory(libs)
# add_subdirectory(sample)
# add_subdirectory(unittest)