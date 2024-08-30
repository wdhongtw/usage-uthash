cmake_minimum_required(VERSION 3.11)
project(usage VERSION 0.1.0 LANGUAGES C)

include(FetchContent)

FetchContent_Declare(
  uthash
  GIT_REPOSITORY https://github.com/wdhongtw/uthash
  GIT_TAG        adopt-cmake
)

FetchContent_MakeAvailable(uthash)

add_executable(hello)
target_link_libraries(hello PRIVATE uthash)
target_sources(hello PRIVATE src/hello.c)
