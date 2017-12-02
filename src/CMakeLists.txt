
set(FUTIL_SRC futil_atomic.c futil_queue.c)
set(FUTIL_HEADER futil_queue.h futil_typedef.h futil_atomic.h )


# TARGET_LINK_LIBRARIES(futil)
add_library(futil_static STATIC ${FUTIL_SRC})
add_library(futil_shared SHARED ${FUTIL_SRC})
SET_TARGET_PROPERTIES(futil_static PROPERTIES OUTPUT_NAME "futil")
SET_TARGET_PROPERTIES(futil_shared PROPERTIES OUTPUT_NAME "futil")

SET_TARGET_PROPERTIES(futil_shared PROPERTIES VERSION 
	${VERSION_MAJOR}.${VERSION_MINOR} SOVERSION ${VERSION_MAJOR})

include_directories("${PROJECT_BINARY_DIR}")


install (TARGETS futil_static DESTINATION bin)
install (TARGETS futil_shared DESTINATION bin)
install (FILES ${FUTIL_HEADER} DESTINATION include)
