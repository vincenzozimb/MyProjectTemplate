cmake_minimum_required(VERSION 3.13)
project(MyProjectTemplate)

set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED ON)


# add the library folder
add_subdirectory(myfunc)

# add the binary tree to the search path for include files so that we will find testConfig.h
include_directories(PUBLIC
                        "${PROJECT_BINARY_DIR}"
                        "${PROJECT_SOURCE_DIR}/myfunc"
                        )


# List here the directories in projects
add_subdirectory(code/test)

# doxygen code to add here?
