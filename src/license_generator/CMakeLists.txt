add_library(license_generator_lib STATIC
	command_line-parser.cpp
	license.cpp
	project.cpp
	../ini/ConvertUTF.cpp
)

target_link_libraries(license_generator_lib
	libcrypto.a
)

add_executable(lccgen
	open-license-main.cpp
)

target_link_libraries(lccgen
	lcc_base
	license_generator_lib
	boost_filesystem
	boost_program_options
)
