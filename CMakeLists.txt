cmake_minimum_required(VERSION 3.26)
project(sokol_nuklear_starter C)

set(CMAKE_C_STANDARD 11)
add_compile_definitions(-DSOKOL_METAL)
set(CMAKE_C_COMPILER clang)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS}  -ObjC")

include_directories(vendor/sokol vendor/sokol/util vendor/Nuklear)
add_executable(sokol_nuklear_starter
        main.c)
target_link_libraries(sokol_nuklear_starter "-framework Cocoa -framework QuartzCore -framework Metal -framework MetalKit")
