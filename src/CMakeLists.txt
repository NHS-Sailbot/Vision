set(sources template/core/add.cpp)

if (WIN32)
    set(sources ${sources} template/plat/windows/windows.cpp)
elseif (APPLE)
    set(sources ${sources} template/plat/macos/macos.cpp)
elseif (UNIX)
    set(sources ${sources} template/plat/linux/linux.cpp)
endif()

add_library(${PROJECT_NAME} ${sources})
target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_LIST_DIR})
