add_executable(${PROJECT_NAME} main.c)

target_link_libraries(${PROJECT_NAME} raylib)
target_include_directories(${PROJECT_NAME} PRIVATE external/raylib/src)
