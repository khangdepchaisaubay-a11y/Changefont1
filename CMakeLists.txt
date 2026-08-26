cmake_minimum_required(VERSION 3.13)
include(FetchContent)

FetchContent_Declare(
    Geode
    GIT_REPOSITORY https://github.com/geode-sdk/geode.git
    GIT_TAG v2.0.0
)
FetchContent_MakeAvailable(Geode)

project(CustomFontMod VERSION 1.0.0 LANGUAGES CXX)

add_geode_mod(
    CustomFontMod
    SOURCES src/main.cpp
    RESOURCES resources/custom_font.fnt resources/custom_font.png
)
