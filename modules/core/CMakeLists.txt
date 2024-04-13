set(
    HEADER_FILES
        Engine.h
)

set(
    SOURCE_FILES
        src/Engine.cpp
)

add_library(
    BurnCore SHARED
        ${HEADER_FILES}
        ${SOURCE_FILES}
)

set_property(TARGET BurnCore PROPERTY CXX_STANDARD 20)

include_directories(..)
