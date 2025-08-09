cmake_minimum_required(VERSION 3.10)
set(MY_PROJECT_VERSION 1.0.0)
project(vscode_template VERSION ${MY_PROJECT_VERSION})

option(ENABLE_RELEASE_DEBUG_INFO "Enable debug info in Release mode" ON)
option(DISABLE_RELEASE_OPTIMIZATION "Disable optimization in Release mode" ON)

include(cmake/Preset.cmake)

if(WIN32)
else()
    find_package(spdlog REQUIRED)

    if(spdlog_FOUND)
        message(STATUS "found spdlog")
    endif()
endif()

if(WIN32)
    add_subdirectory(template)
else()
    add_subdirectory(template)
endif()