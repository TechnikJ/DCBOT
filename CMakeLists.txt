cmake_minimum_required(VERSION 3.16)

project(dcBot)

add_subdirectory(libs/DPP)

add_executable(${PROJECT_NAME}
    src/bot.cpp
)

target_include_directories(${PROJECT_NAME} PRIVATE
    libs/DPP
    libs/DPP/include/dpp-10.0
)

target_link_libraries(${PROJECT_NAME}
    PRIVATE dpp
)

set_target_properties(${PROJECT_NAME} PROPERTIES
    CXX_STANDARD 20
    CXX_STANDARD_REQUIRED ON
)