project(cpp-particle-system)
set(PROJECT_VERSION 3.1)

set(sources
        ParticleSystem.cpp
        )

set(public_headers
        ParticleSystem.h
        )

add_library(cpp-particle-system ${sources} ${public_headers})

set_target_properties(cpp-particle-system PROPERTIES
        PUBLIC_HEADER "${public_headers}"
        VERSION ${PROJECT_VERSION}
        )

target_include_directories(cpp-particle-system
        PUBLIC
        $<INSTALL_INTERFACE:include>
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
        PRIVATE
        ${CMAKE_CURRENT_SOURCE_DIR}
        )