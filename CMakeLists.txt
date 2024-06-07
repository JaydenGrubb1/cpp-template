cmake_minimum_required(VERSION 3.16)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON CACHE INTERNAL "")

project(Example)
enable_language(CXX)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_compile_options(
	-Wall
	-Wextra
	-Wpedantic
	-Wold-style-cast
)

add_executable(
	${PROJECT_NAME}
	src/main.cpp
)

# find_package(Example REQUIRED)

include_directories(
	${CMAKE_CURRENT_SOURCE_DIR}/include
	# ${Example_INCLUDE_DIRS}
)

target_link_libraries(
	${PROJECT_NAME}
	# ${Example_LIBRARIES}
)