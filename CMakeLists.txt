cmake_minimum_required(
  VERSION 3.14
  FATAL_ERROR
)

project(
  dtrack
  VERSION 2.7.0
  LANGUAGES CXX
)

add_library(
  dtrack

  DTrackSDK/src/DTrackSDK.cpp
  DTrackSDK/src/DTrackData.cpp
  DTrackSDK/src/DTrackNet.cpp
  DTrackSDK/src/DTrackParse.cpp
  DTrackSDK/src/DTrackParser.cpp
)
target_include_directories(
  dtrack
  PUBLIC
    DTrackSDK/include
)

add_library(dtrack::dtrack ALIAS dtrack)
