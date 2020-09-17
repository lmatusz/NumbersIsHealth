cmake_minimum_required(VERSION 3.17)
project(NumbersIsHealth)

set(CMAKE_CXX_STANDARD 14)

include_directories(.)

ADD_EXECUTABLE(LottoGUI
        LottoGUI.cxx
        LottoGUI.h)

FIND_PACKAGE(FLTK REQUIRED)

TARGET_LINK_DIRECTORIES(LottoGUI PRIVATE mingw32/i686-w64-mingw32)
TARGET_LINK_LIBRARIES(LottoGUI mingw32 fltk)