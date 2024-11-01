set( DEMO_NAME "cellular_demo" )

# Demo target.
add_executable(
    ${DEMO_NAME}
        "${DEMO_NAME}.c"
        "qrencode_print.c"
)

target_link_libraries(
    ${DEMO_NAME}
    PUBLIC
        ${QRENCODE_LIBRARIES}
        link_core
)

target_include_directories(
    ${DEMO_NAME}
    PUBLIC
        ${QRENCODE_INCLUDE_DIR}
        ${CMAKE_CURRENT_LIST_DIR}
)
