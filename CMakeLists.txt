cmake_minimum_required(VERSION 3.4)
project(tinyfiledialogs C)

add_library(tinyfiledialogs tinyfiledialogs.c)
add_subdirectory(example)
install(
    TARGETS tinyfiledialogs
    EXPORT tinyfiledialogsConfig
    ARCHIVE DESTINATION lib
    LIBRARY DESTINATION lib
    RUNTIME DESTINATION bin
)
install(
    FILES tinyfiledialogs.h
    DESTINATION "${CMAKE_INSTALL_PREFIX}/include/tinyfiledialogs"
)

export(
    TARGETS tinyfiledialogs
    NAMESPACE tinyfiledialogs::
    FILE "${CMAKE_CURRENT_BINARY_DIR}/tinyfiledialogsConfig.cmake"
)
install(
    EXPORT tinyfiledialogsConfig
    NAMESPACE tinyfiledialogs::
    DESTINATION "${CMAKE_INSTALL_PREFIX}/share/tinyfiledialogs"
)
