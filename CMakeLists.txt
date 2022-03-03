cmake_minimum_required(VERSION 3.21)
project(opengl_playground)

set(CMAKE_CXX_STANDARD 14)

add_library(glad include/glad/glad.h include/KHR/khrplatform.h src/glad.c)




find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)


add_executable(opengl_playground main.cpp)



target_link_libraries(opengl_playground glfw)

target_link_libraries(opengl_playground OpenGL::GL)
target_link_libraries(opengl_playground X11)
target_link_libraries(opengl_playground pthread)
target_link_libraries(opengl_playground Xrandr)
target_link_libraries(opengl_playground Xi)
target_link_libraries(opengl_playground dl)

target_link_libraries(opengl_playground glad)




