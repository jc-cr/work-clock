cmake_minimum_required(VERSION 3.16)
project(work-clock)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 17)

# Set the compiler flags
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O2 -Wall -Wextra -Werror -pedantic -Weffc++")

# Add the include directory to the include path
include_directories(include)

add_library(work-timer src/work-timer.cc)

# Add the executable
add_executable(work-clock src/main.cc)

# Link the library to the executable
target_link_libraries(work-clock work-timer)
