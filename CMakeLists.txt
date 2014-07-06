cmake_minimum_required(VERSION 2.6)

# Project configuration
project(p5)
set(LIBRARY_OUTPUT_PATH lib/)
set(SRC_DIR src)
set(INCLUDE_DIR include)

# Public headers include
include_directories(include)


file(
  GLOB_RECURSE
  SRC_FILES
  ${SRC_DIR}/*
  )

file(
  GLOB_RECURSE
  HEADER_FILES
  ${INCLUDE_DIR}/*
  )

add_library(p5 SHARED ${SRC_FILES} ${HEADER_FILES})

