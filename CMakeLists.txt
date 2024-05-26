cmake_minimum_required(VERSION 3.0.0)
project(tinyNet VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()

include_directories(${CMAKE_SOURCE_DIR}/Inc)


file(GLOB SOURCE_FILES  "${CMAKE_SOURCE_DIR}/*.cpp" "${CMAKE_SOURCE_DIR}/Src/*.cpp")

add_executable(tinyNet ${SOURCE_FILES})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
