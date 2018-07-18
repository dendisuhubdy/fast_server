cmake_minimum_required(VERSION 3.8.0)

project(FAST_PUBLISHER)

set(CMAKE_BUILD_TYPE Release)
set(CMAKE_CXX_STANDARD 11)

find_package(mFAST REQUIRED COMPONENTS coder)
find_package(Boost 1.65 COMPONENTS system REQUIRED)

include_directories( 
    ${FAST_PUBLISHER_SOURCE_DIR}/include
)

link_directories(
    ${FAST_PUBLISHER_SOURCE_DIR}/lib
)

set(
	CMAKE_CXX_LINK_FLAGS 
)

add_subdirectory(src)
#add_subdirectory(test)
#enable_testing()
#add_test (NAME UnitTests COMMAND FASTPUBLISHERTest)
