cmake_minimum_required(VERSION 3.14)

project(Fly-simulator-server)

file(GLOB srcs
        "*.h"
        "*.cpp"
        )

file(GLOB name_gen_srcs
        "../Name_Generator_lib/*.h"
        "../Name_Generator_lib/*.cpp"
        )

file(GLOB show_me_img_srcs
        "../Show me image/Send_const.h"
        )

find_package(SDL REQUIRED)
find_package(SDL_net REQUIRED)
include_directories(${SDL_INCLUDE_DIR} ${SDL_NET_INCLUDE_DIRS})

add_executable(Fly-simulator-server ${srcs} ${name_gen_srcs} ${show_me_img_srcs})
target_link_libraries(Fly-simulator-server ${SDL_LIBRARY} ${SDL_NET_LIBRARIES})
