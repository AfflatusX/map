if(CONFIG_LIB_MAP)

    zephyr_interface_library_named(map)

    set (MAP_ROOT_DIR ${CMAKE_CURRENT_SOURCE_DIR}/../)

    zephyr_library()
    zephyr_include_directories(map INTERFACE ${MAP_ROOT_DIR}/src)

    FILE(GLOB_RECURSE MAP_SOURCE_FILES ${MAP_ROOT_DIR}/**/*.c)

    zephyr_library_sources(${MAP_SOURCE_FILES})

    zephyr_library_link_libraries(map)

endif()
