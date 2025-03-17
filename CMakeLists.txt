cmake_minimum_required(VERSION 3.22)

# Setup project
project(LwLibPROJECT)

if(NOT PROJECT_IS_TOP_LEVEL)
    add_subdirectory("lwutil")
else()
    enable_testing()
    add_executable(${PROJECT_NAME})
    target_sources(${PROJECT_NAME} PRIVATE
        ${CMAKE_CURRENT_LIST_DIR}/dev/main.c
    )
    target_include_directories(${PROJECT_NAME} PUBLIC
        ${CMAKE_CURRENT_LIST_DIR}/dev
    )

    # Add subdir with lwutil and link to the project
    add_subdirectory("lwutil")
    target_link_libraries(${PROJECT_NAME} PUBLIC lwutil)

    # Add additional compile settings to library, which will be propagated to executable (PUBLIC link)
    target_compile_options(lwutil PUBLIC -Wall -Wextra -Wpedantic)
    target_compile_definitions(lwutil PUBLIC WIN32 _DEBUG CONSOLE LWUTIL_DEV)

    # Add test
    add_test(NAME Test COMMAND $<TARGET_FILE:${CMAKE_PROJECT_NAME}>)
endif()
