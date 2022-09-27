add_library(lcc_base STATIC
	base64.cpp
	crypto_helper.cpp
	openssl/crypto_helper_ssl.cpp
)

target_link_libraries(lcc_base PUBLIC
	crypto
)
