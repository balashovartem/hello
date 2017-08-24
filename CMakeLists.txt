project( hello )

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

include_directories(include)
set( SOURCES ${SOURCES} src/hello.cpp )

add_library( ${PROJECT_NAME} ${SOURCES} ${HEADERS}  )
target_link_libraries(${PROJECT_NAME} ${CONAN_LIBS})

enable_testing()
add_subdirectory(test)