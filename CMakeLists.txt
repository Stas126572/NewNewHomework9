cmake_minimum_required(VERSION 3.7.2)
project(TopkWords CXX)

set(CMAKE_CXX_STANDARD 17)

add_executable(top_words topk_words.cpp)

if (MSVC)
    target_compile_options(top_words PUBLIC /W4)
else ()
    target_compile_options(top_words PUBLIC -Wall -Wextra -Wpedantic -Wconversion -Wsign-conversion)
endif ()