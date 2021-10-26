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
)

target_sources(imgui PRIVATE ${SOURCES})
source_group("source" FILES ${SOURCES})
