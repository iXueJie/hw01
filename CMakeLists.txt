cmake_minimum_required(VERSION 3.12)
project(hellocmake LANGUAGES C CXX) # 添加LANGUAGES C: stbiw由c实现

if (NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE Release)
endif()

add_subdirectory(stbiw)

add_executable(main main.cpp rainbow.cpp mandel.cpp)
target_link_libraries(main PUBLIC stbiw)
