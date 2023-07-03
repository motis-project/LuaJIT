cmake_minimum_required(VERSION 3.0)

project(minilua)

add_executable(minilua ../../minilua.c)
if (UNIX)
  target_link_libraries(minilua m)
endif()

if (MSVC)
  set_target_properties(minilua PROPERTIES RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR})
endif()
