cmake_minimum_required(VERSION 3.10)

# Set the project name
project(DOOM)

# Set the C++ standard to C++23
add_definitions(-DUNUSED=[[maybe_unused]])
add_definitions(-DLINUX)
add_definitions(-DNORMALUNIX)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)  # Optional: Disable compiler-specific extensions

set(CMAKE_COLOR_MAKEFILE ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
# Specify the folder containing your source files
set(SOURCE_DIR .)


# Use file(GLOB ...) to include all .cpp and .h files
file(GLOB SOURCES "${SOURCE_DIR}/*.cpp" "${SOURCE_DIR}/*.h")

# Add the executable target
add_executable(DOOM ${SOURCES})

