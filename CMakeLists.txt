cmake_minimum_required(VERSION 3.10)

project(imgui)

add_library(imgui STATIC
    imconfig.h
    imgui_tables.cpp
    imgui_demo.cpp
    imgui_draw.cpp
    imgui_internal.h
    imgui_widgets.cpp
    imgui.cpp
    imgui.h
    imstb_rectpack.h
    imstb_textedit.h
    imstb_truetype.h

    misc/cpp/imgui_stdlib.cpp
    misc/cpp/imgui_stdlib.h
)
target_include_directories(imgui PUBLIC .)
#target_link_libraries(imgui)
add_library(imgui::imgui ALIAS imgui)
