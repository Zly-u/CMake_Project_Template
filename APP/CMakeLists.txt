set(SUB_PROJECT_NAME "App")
set(CMAKE_CXX_STANDARD 23)

file(GLOB SOURCES "*.cpp" "*.h")

add_executable(${SUB_PROJECT_NAME} ${SOURCES})

#include files from CORE project
include_directories(${CMAKE_SOURCE_DIR}/CORE)
target_link_libraries(${SUB_PROJECT_NAME} LINK_PRIVATE "Core")

install(
    TARGETS ${SUB_PROJECT_NAME}
    RUNTIME DESTINATION ${G_INSTALL_DIR}
)