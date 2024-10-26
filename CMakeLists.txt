cmake_minimum_required(VERSION 3.12)
project(llm.hlsl)

# 设置C++版本
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(SOURCES
    src/main.cpp
)
add_subdirectory(third_party/imgui)
add_executable(llm.hlsl ${SOURCES})

target_link_libraries(llm.hlsl PRIVATE d3d12 dxgi dxguid ImGui)
