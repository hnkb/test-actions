
cmake_minimum_required (VERSION 3.8)

project ("TestActions")


add_executable (TestActions
	"src/main.cpp")


if (MSVC)
	target_compile_options (TestActions PRIVATE /utf-8)
elseif (WIN32)
	target_link_libraries (TestActions PRIVATE -static)
endif()


target_compile_features (TestActions PRIVATE cxx_std_17)
