cmake_minimum_required(VERSION 3.16)
project(image_processor)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

find_package(OpenCV REQUIRED)

add_executable(ImageProcessor src/main.cpp)
target_link_libraries(ImageProcessor PRIVATE ${OpenCV_LIBS})
target_include_directories(ImageProcessor PRIVATE ${OpenCV_INCLUDE_DIRS})