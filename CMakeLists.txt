cmake_minimum_required(VERSION 3.5)

project(aes_library)

set(CMAKE_C_STANDARD 11)

add_library(aes_library SHARED src/AES.c)

set_target_properties(aes_library PROPERTIES
  LIBRARY_OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/build)

install(TARGETS aes_library
  LIBRARY DESTINATION ${CMAKE_CURRENT_BINARY_DIR}/build)
