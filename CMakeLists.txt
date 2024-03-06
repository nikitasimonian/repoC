cmake_minimum_required(VERSION 3.21)
project(C)

if (NOT TARGET ${PROJECT_NAME})
    add_library(${PROJECT_NAME} STATIC)
    target_sources(${PROJECT_NAME} PRIVATE
        ${CMAKE_CURRENT_SOURCE_DIR}/${PROJECT_NAME}/c.h
        ${CMAKE_CURRENT_SOURCE_DIR}/${PROJECT_NAME}/c.cpp
    )
    target_include_directories(${PROJECT_NAME} INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
    target_include_directories(${PROJECT_NAME} PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>)
endif()