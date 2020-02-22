cmake_minimum_required(VERSION 3.12)
project(template VERSION 0.1.0)

if (NOT TARGET ${PROJECT_NAME})
  add_subdirectory(src)
endif()
