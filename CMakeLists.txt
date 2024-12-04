cmake_minimum_required (VERSION 3.8)

project(rectruitment_task VERSION 1.0)

set (CMAKE_CXX_STANDARD 20 REQUIRED)

add_subdirectory(external/glfw)

add_executable(multiline src/main.cpp)

find_package(OpenGL REQUIRED)

target_link_libraries(multiline PRIVATE OpenGL::GL glfw ${GLFW_LIBRARIES})

include_directories(external/glfw/include)
