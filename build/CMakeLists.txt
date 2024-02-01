# For now I don't know the minumum version of cmake that I will be requiring.
# Otherwise, I will just need to check the mininum required for the other depen-
# dencies.
cmake_minimum_required(VERSION 3.10)

# Create a project
project(Solver VERSION 1.0)

# Make cmake check the C++ version required.
# Set the variable CMAKE_CXX_STANDARD to 11
# and the variable CMAKE_CXX_STANDARD_REQUIRED to True
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Configure file?
#configure_file(TutorialConfig.h.in TutorialConfig.h)

# Add an executable called Solver to the project
add_executable(solver ../src/main.cpp)

# I don't know how to use the target_include_directories to include ${PROJECT_BINARY_DIR}
#target_include_directories(Solver PUBLIC 
#                           $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>../include/
#                           $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>../src/
#                           )
