cmake_minimum_required(VERSION 3.29)

set(PROJECT_NAME CMake_Project_Template)

set(CMAKE_CXX_STANDARD 23)

project(
    ${PROJECT_NAME}
    VERSION 1.0
    DESCRIPTION "Some Description."
    LANGUAGES C CXX
)



################################################################

set(G_INSTALL_DIR ${CMAKE_SOURCE_DIR}/__BUILD__ CACHE INTERNAL "")

################################################################

if(WIN32)

endif()

################################################################

add_subdirectory(APP)
add_subdirectory(CORE)
