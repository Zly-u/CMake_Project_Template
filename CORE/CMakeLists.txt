set(SUB_PROJECT_NAME "Core")
set(CMAKE_CXX_STANDARD 23)

file(GLOB SOURCES "src/*.cpp" "src/*.h")


add_library(${SUB_PROJECT_NAME} SHARED ${SOURCES})

target_include_directories(${SUB_PROJECT_NAME} INTERFACE src)

install(
    TARGETS ${SUB_PROJECT_NAME}
    RUNTIME DESTINATION ${G_INSTALL_DIR}
)