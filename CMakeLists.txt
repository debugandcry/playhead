cmake_minimum_required(VERSION 3.20)

project(tactus)

set(CMAKE_CXX_STANDARD 20)

add_executable(tactus tactus.cpp audio/audioengine.cpp audio/preloader.cpp helpers/helpers.cpp ui/controls.cpp)

target_include_directories(tactus PRIVATE audio helpers ui external data)

target_link_libraries(tactus PRIVATE comdlg32)

target_compile_options(tactus PRIVATE -Wall -Wextra -O2)