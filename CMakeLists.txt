cmake_minimum_required(VERSION 2.8)
project(nate_robin_opengl)

set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)
set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)

include_directories(./)
file(GLOB f ./glm.c ./sgi.c)

set(EXT_LIB GL GLU GLEW glut m)


add_executable(fog ./fog.c)
target_link_libraries(fog ${f} ${EXT_LIB})

add_executable(lightmaterial ./lightmaterial.c)
target_link_libraries(lightmaterial ${f} ${EXT_LIB})

add_executable(lightposition ./lightposition.c)
target_link_libraries(lightposition ${f} ${EXT_LIB})

add_executable(projection ./projection.c)
target_link_libraries(projection ${f} ${EXT_LIB})

add_executable(texture ./texture.c)
target_link_libraries(texture ${f} ${EXT_LIB})

add_executable(transformation ./transformation.c)
target_link_libraries(transformation ${f} ${EXT_LIB})
