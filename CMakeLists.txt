cmake_minimum_required(VERSION 3.13)
project(fpm LANGUAGES Fortran)

add_executable(fpm fpm/app/main.f90)

add_subdirectory(fpm/src)
add_subdirectory(fpm/src/fpm/manifest)

if(BUILD_TESTING)
  add_subdirectory(fpm/test)
endif()
