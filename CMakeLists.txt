cmake_minimum_required(VERSION 3.0.0)
project(main VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()

add_executable(main main.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

# set(CUSTOM_INSTALL_DIR $ENV{HOME}/my_app_bin)

install(TARGETS main
        RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR})

