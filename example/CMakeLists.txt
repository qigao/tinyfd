add_executable(hello hello.c)
target_link_libraries(hello PUBLIC tinyfiledialogs)
target_include_directories(hello PUBLIC ${PROJECT_SOURCE_DIR})
install(
    TARGETS hello
     ARCHIVE DESTINATION bin
    LIBRARY DESTINATION lib
    RUNTIME DESTINATION lib
)
 