cmake_minimum_required(VERSION 3.5)

# CHANGE HERE
set(PROJECT_NAME ARKO_PROJECT)

set(CMAKE_PROJECT_NAME ${PROJECT_NAME})
project(${PROJECT_NAME})

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_BUILD_TYPE DEBUG)

set(CMAKE_CXX_COMPILER g++-4.9)

set(CMAKE_ASM_NASM_OBJECT_FORMAT elf32)
set(CMAKE_C_FLAGS -m32)
set(CMAKE_CXX_FLAGS -m32)
enable_language(ASM_NASM)

# ADD SOURCE FILES
set(SOURCE_FILES main.cpp func.asm)

set(EXECUTABLE_NAME ${PROJECT_NAME})
add_executable(${EXECUTABLE_NAME} ${SOURCE_FILES})

#
# SFML
#
# download 32-bit wersion of SFML into ./SFML install dependencies with :i386 suffix and uncomment
# lines below
#
#set(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/cmake_modules")
#set(SFML_ROOT ./SFML)
#include_directories(${SFML_ROOT}/include)
#target_link_libraries(${EXECUTABLE_NAME}
#                            ${CMAKE_SOURCE_DIR}/SFML/lib/libsfml-system.so
#                            ${CMAKE_SOURCE_DIR}/SFML/lib/libsfml-window.so
#                            ${CMAKE_SOURCE_DIR}/SFML/lib/libsfml-graphics.so )


