add_subdirectory(Bind)
add_subdirectory(HTTP-Methods)
add_subdirectory(Queue)
add_subdirectory(Request-Parser)
add_subdirectory(HTTP-Server)
target_link_libraries(httpmethods PRIVATE requestparser)
target_link_libraries(httpserver PRIVATE httpmethods requestparser queue bind)
