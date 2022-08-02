set(STB_HEADERS
    "stb_image.h"
)
list(
    TRANSFORM STB_HEADERS
    PREPEND "${CMAKE_CURRENT_SOURCE_DIR}/include/"
)
source_group("includes"
    FILES ${STB_HEADERS}
)
add_library(stb INTERFACE
    ${STB_HEADERS}
)
target_include_directories(stb
    INTERFACE
        "${CMAKE_CURRENT_SOURCE_DIR}/include/"
)
target_precompile_headers(stb
    INTERFACE
        ${STB_HEADERS}
)
