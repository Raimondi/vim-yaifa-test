# New escape-sequence processing.
cmake_minimum_required(VERSION 3.16.3)
cmake_policy(VERSION 3.16.3)

project(editorconfig-plugin-tests NONE)

if(${CMAKE_SOURCE_DIR} STREQUAL ${CMAKE_CURRENT_SOURCE_DIR})
    set(GETOPTIONS_CMD ${CMAKE_CURRENT_LIST_DIR}/../bin/getoptions CACHE STRING "getoptions command.")
    enable_testing()
    message(STATUS "tests: Standalone testing enabled")
endif()

add_subdirectory(core)
add_subdirectory(plugin)
