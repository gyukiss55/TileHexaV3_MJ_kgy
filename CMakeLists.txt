cmake_minimum_required(VERSION 3.20)

project(MyGLFWApp LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(glad CONFIG REQUIRED)
find_package(glfw3 CONFIG REQUIRED)
find_package(OpenGL REQUIRED)


add_executable(MyGLFWApp
    Hexa3DApp.cpp
	ButtonHandler.cpp
	TableManager.cpp
	TileSolver.cpp
)

target_link_libraries(MyGLFWApp PRIVATE
    glfw
    glad::glad
)

# Windows system libraries
target_link_libraries(MyGLFWApp PRIVATE
    glfw
    glad::glad
    OpenGL::GL
)