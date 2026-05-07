cmake_minimum_required(VERSION 3.10)
project(SparkEngine2D)

set(CMAKE_CXX_STANDARD 17)

# Find SDL2
find_package(SDL2 REQUIRED)
find_package(SDL2_image REQUIRED)

include_directories(${SDL2_INCLUDE_DIRS} ${SDL2_IMAGE_INCLUDE_DIRS} include)

file(GLOB SOURCES "src/*.cpp")

add_executable(SparkEngine2D main.cpp ${SOURCES})

target_link_libraries(SparkEngine2D ${SDL2_LIBRARIES} ${SDL2_IMAGE_LIBRARIES})
