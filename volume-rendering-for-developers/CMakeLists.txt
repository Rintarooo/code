cmake_minimum_required(VERSION 3.10)
project(volume_render_project)

# C++ 17
# https://qiita.com/yumetodo/items/bd8f556ab56298f19ba8
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# find_package(OpenGL REQUIRED)
# find_package(GLFW REQUIRED)
# find_package(glfw3 3.2 REQUIRED)
# find_package(glfw3 REQUIRED)
# find_package(ImageMagick REQUIRED)
# find_package(ImageMagick COMPONENTS convert)
# find_package(ImageMagick COMPONENTS convert mogrify display)
# find_package(ImageMagick COMPONENTS Magick++)
# find_package(ImageMagick COMPONENTS Magick++ convert)

include_directories(
	# ${OPENGL_INCLUDE_DIR}
	# ${GLFW_INCLUDE_DIR}
	# ${ImageMagick_INCLUDE_DIRS}
	include/stb_image/
	# Tutorial1/include/
	# Tutorial1/dependencies/stb_image/
	# Tutorial1/dependencies/tinyobjloader/
)

add_executable(main 
    raymarch-chap2.cpp
    )

target_link_libraries(main 
	# ${OPENGL_LIBRARIES}
	# ${GLFW_LIBRARIES}
	# ${ImageMagick_LIBRARIES}
	# glfw
)


message("-- OpenGL --")
# https://cmake.org/cmake/help/v3.10/module/FindOpenGL.html
# message(STATUS "version : ${OPENGL_FOUND}")
# message(STATUS "OpenGL version: ${OPENGL_VERSION}")
message(STATUS "libs : ${OPENGL_LIBRARIES}")
message(STATUS "include dirs : ${OPENGL_INCLUDE_DIR}")

