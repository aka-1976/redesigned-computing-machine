cmake_minimum_required(VERSION 3.10)

project(redesigned-computing-machine)

add_executable(main main.cpp functions.cpp functions.h)

enable_testing()

if(ENABLE_CODE_COVERAGE)
    if(CMAKE_COMPILER_IS_GNUCXX)
        add_compile_options("-g" "-O0" "--coverage")
        add_link_options("--coverage")
    endif()
endif()
