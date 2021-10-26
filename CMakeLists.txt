cmake_minimum_required(VERSION 3.10)
project(imgui)

add_library(imgui STATIC)

set(SOURCES
	imconfig.h
	imgui.cpp
	imgui.h
	imgui_demo.cpp
	imgui_draw.cpp
	imgui_internal.h
	imgui_tables.cpp
	imgui_widgets.cpp
	imstb_rectpack.h
	imstb_textedit.h
	imstb_truetype.h

    backends/imgui_impl_glfw.cpp
    backends/imgui_impl_glfw.h
    backends/imgui_impl_opengl2.cpp
    backends/imgui_impl_opengl2.h
)

target_sources(imgui PRIVATE ${SOURCES})
source_group("source" FILES ${SOURCES})
target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR} ${CMAKE_CURRENT_SOURCE_DIR}/../glfw/include)
target_link_libraries(imgui PUBLIC glfw opengl32)
