```cmake
cmake_minimum_required(VERSION 3.10)
project(ConnectFourGUI)

set(CMAKE_CXX_STANDARD 17)

# Find SFML
find_package(SFML 2.5 COMPONENTS graphics window system REQUIRED)

# Source files
file(GLOB SOURCES "src/*.cpp")

# Executable
add_executable(game ${SOURCES})

# Link SFML
target_link_libraries(game sfml-graphics sfml-window sfml-system)
