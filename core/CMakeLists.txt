file(GLOB HEADERS "include/core/*.h")
add_library( ultrainio_core
        src/Block.cpp
        src/Chain.cpp
        src/Transaction.cpp
        ${HEADERS} )

target_link_libraries( ultrainio_core ultrainio_crypto ultrainio_log )
target_include_directories( ultrainio_core PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include" )
