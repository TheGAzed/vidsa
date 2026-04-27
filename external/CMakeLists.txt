set(SDL_TEST OFF CACHE BOOL "" FORCE)
set(SDL_SHARED ON CACHE BOOL "" FORCE)
set(SDL_STATIC ON CACHE BOOL "" FORCE)

add_subdirectory(SDL3)

set(PLATFORM "SDL" CACHE STRING "" FORCE)
set(SUPPORT_SDL2_PACKAGE OFF CACHE BOOL "" FORCE)
set(SUPPORT_SDL3 ON CACHE BOOL "" FORCE)
set(BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(BUILD_GAMES OFF CACHE BOOL "" FORCE)

include_directories(SDL3/include)

add_subdirectory(raylib)

# turned off to avoid SDL2 conflict
set(CLAY_INCLUDE_DEMOS OFF CACHE BOOL "" FORCE)
set(CLAY_INCLUDE_ALL_EXAMPLES OFF CACHE BOOL "" FORCE)

add_subdirectory(clay)
add_library(clay INTERFACE)
target_include_directories(clay INTERFACE clay)
