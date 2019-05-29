cmake_minimum_required(VERSION 3.14)

project(Fly-simulator-client)

file(GLOB srcs
        "*.h"
        "*.cpp"
        )

find_package(SDL REQUIRED)
find_package(SDL_net REQUIRED)
include_directories(${SDL_INCLUDE_DIR} ${SDL_NET_INCLUDE_DIRS})

add_executable(Fly-simulator-client ${srcs})
target_link_libraries(Fly-simulator-client ${SDL_LIBRARY} ${SDL_NET_LIBRARIES})
