set(
    HEADER_FILES
        Buffer.h
)

set(
    SOURCE_FILES
        src/Buffer.cpp
)

add_library(
    BurnGraphics SHARED
        ${SOURCE_FILES}
        ${HEADER_FILES}
)

set_property( TARGET BurnGraphics PROPERTY CXX_STANDARD 20 )

include_directories( .. )
include_directories( ../../libraries/VulkanMemoryAllocator/include )

# Vulkan
find_package( Vulkan REQUIRED )
target_link_libraries( BurnGraphics PUBLIC Vulkan::Vulkan )