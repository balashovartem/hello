project( hello )

set( SOURCES ${SOURCES} src/main.cpp )

add_executable( ${PROJECT_NAME} ${SOURCES} ${HEADERS}  )

install(TARGETS ${PROJECT_NAME} DESTINATION ./ )