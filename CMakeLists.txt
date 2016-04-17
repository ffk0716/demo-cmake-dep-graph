cmake_minimum_required(VERSION 3.3)

add_library(liba a.cxx)
add_library(libb b.cxx)
add_executable(exe main.cxx)
target_link_libraries(exe liba libb)

add_custom_target(dep ALL 
		COMMAND cmake --graphviz=exe.dot
		COMMAND dot exe.dot -T png -o exe.png)
