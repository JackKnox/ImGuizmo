cmake_minimum_required(VERSION 3.15)
project(ImGuizmo LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

file(GLOB_RECURSE SOURCE_DIR "./*.cpp")

add_library(ImGuizmo STATIC ${SOURCE_DIR})
target_include_directories(ImGuizmo PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}")
target_link_libraries(ImGuizmo PUBLIC ImGui)