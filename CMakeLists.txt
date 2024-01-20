cmake_minimum_required(VERSION 3.21)

project(
  stb_image_helper
  VERSION 0.1
  DESCRIPTION "wrapper of stb image lib."
  LANGUAGES C
)

set(HEADERS
  ${CMAKE_CURRENT_SOURCE_DIR}/include/stb_image_helper/stb_image.h
  ${CMAKE_CURRENT_SOURCE_DIR}/include/stb_image_helper/stb_image_write.h
  ${CMAKE_CURRENT_SOURCE_DIR}/include/stb_image_helper/stb_image_resize.h)
add_library(${PROJECT_NAME} INTERFACE ${HEADERS})

# target_sources(${PROJECT_NAME})
target_compile_features(${PROJECT_NAME} INTERFACE c_std_11)
target_include_directories(${PROJECT_NAME} INTERFACE include/)

# configure_file(
# ${CMAKE_CURRENT_SOURCE_DIR}/cmake/info.h.in
# ${CMAKE_CURRENT_SOURCE_DIR}/include/${PROJECT_NAME}/info.h
# )