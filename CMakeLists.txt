cmake_minimum_required(VERSION 3.0.0)
project(example VERSION 0.1.0)

include(CTest)
enable_testing()
file(GLOB SRCS CONFIGURE_DEPENDS "src/*.cpp" "src/*.c" "src/*.hpp" "src/*c.h")

add_executable(${PROJECT_NAME} ${SRCS})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
