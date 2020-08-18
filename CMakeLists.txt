cmake_minimum_required (VERSION 2.6)


SET(PROJECT_NAME Fluppy)
# コンパイラ
SET(CMAKE_C_COMPILER clang)
SET(CMAKE_CXX_COMPILER clang++)
# リリースビルド用オプション
SET(CMAKE_CXX_FLAGS_RELEASE "-Wall -O2")
# デバッグビルド用オプション
SET(CMAKE_CXX_FLAGS_DEBUG "-Wall -g -O0")
# ビルドの基本フラグ
SET(CMAKE_CXX_FLAGS "-std=c++11 -stdlib=libc++ ${CMAKE_CXX_FLAGS}")
# ビルドのタイプ
SET(CMAKE_BUILD_TYPE Debug)
# ext type
SET(PUTTYPE ".out")
# バージョン
SET(serial "0.0.1")

SET(CMAKE_CURRENT_SOURCE_DIR "/Users/yo/program/fluppy")
SET(MAIN_SOURCES "${CMAKE_CURRENT_SOURCE_DIR}/main.cpp")

SET(SFML_INCLUDE_DIR "/usr/local/Cellar/sfml/2.5.1/include")
SET(SFML_LIBRARIES "/usr/local/Cellar/sfml/2.5.1/lib")
PROJECT(${PROJECT_NAME}${PUTTYPE})

ADD_EXECUTABLE(${PROJECT_NAME} ${MAIN_SOURCES})

find_package(SFML 2 COMPONENTS system window graphics audio REQUIRED)

# includes
include_directories(${PROJECT_NAME} ${SFML_INCLUDE_DIR})

# target link
target_link_libraries(${PROJECT_NAME} ${SFML_LIBRARIES}) 

