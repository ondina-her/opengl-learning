cmake_minimum_required(VERSION 3.10)
project(OpenGL_Learning)

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)

# Include directories (tells CMake where your GLAD and GLFW headers are)
include_directories(include)

# Find your library files (tells CMake where GLFW .lib/.a files are)
link_directories(lib)

# HERE IS WHERE YOU CHOOSE WHICH MAIN.CPP TO RUN
# Switch between "src/01_hello_opengl/main.cpp" and "src/02_hello_triangle/main.cpp"
add_executable(main 
    src/02_hello_triangle/main.cpp 
    src/glad.c
)

# Link GLFW and your operating system's graphics libraries
target_link_libraries(main glfw3) 
