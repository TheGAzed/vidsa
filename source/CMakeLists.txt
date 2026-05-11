add_executable(${PROJECT_NAME} main.c)

add_definitions(-DDIRECTORY="${CMAKE_SOURCE_DIR}/")

target_link_libraries(${PROJECT_NAME} raylib SDL3::SDL3-static clay)
target_include_directories(${PROJECT_NAME} PRIVATE external/raylib/src)
