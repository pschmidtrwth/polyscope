cmake_minimum_required(VERSION 2.8.9)

if("${POLYSCOPE_BACKEND_OPENGL3_GLFW}")

  ## Glad
  if (NOT TARGET glad)
    add_subdirectory(glad)
  endif()

  ## GLFW
  if (NOT TARGET glfw)
    set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
    set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
    set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
    set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)
    add_subdirectory(glfw)
  endif()
endif()

if("${POLYSCOPE_BACKEND_OPENGL_MOCK}")
endif()

## Imgui
if (NOT TARGET imgui)
  add_subdirectory(imgui)
endif()

## Argparse

## STB stuff
add_subdirectory(stb)
