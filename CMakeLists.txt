project(glad)

add_library(glad
    src/glad.c
)

include_directories(
    "include"
)

target_include_directories(glad INTERFACE
	$<BUILD_INTERFACE:${PROJECT_SOURCE_DIR}/include>
	$<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}/include>
)
