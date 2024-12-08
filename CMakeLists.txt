cmake_minimum_required(VERSION 3.10)
project(CodeforcesPractice)

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Create an executable for each source file
file(GLOB CPP_SOURCES "*.cpp")
foreach(SOURCE_FILE ${CPP_SOURCES})
    get_filename_component(EXECUTABLE_NAME ${SOURCE_FILE} NAME_WE)
    add_executable(${EXECUTABLE_NAME} ${SOURCE_FILE})
endforeach() 