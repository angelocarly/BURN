# BURN
![build](https://github.com/angelocarly/BURN/actions/workflows/cmake.yml/badge.svg)  
Minimal C++ algorithmic art renderer using Vulkan. Made for personal art projects.

## Goals of this project
This project is a next iteration of my [previous generative art engine](https://github.com/angelocarly/burst)..

What I learned from developing it:
- Managing many git submodules is hell.
- Vulkan-hpp and VMA-hpp aren't as useful as I thought.
- I actually would like swapchain resizing.
- I didn't experience much extra usefulness from the layer above Vulkan.
- Presenter framework was nice, but unnecessary. Splitting into modules is nice though.

## Building
Firstly, install the required system dependencies:
```
sudo apt-get install -y libspdlog-dev libglfw3-dev glslang-tools libglm-dev
```

Secondly, install the [Vulkan SDK](https://vulkan.lunarg.com) and set the path environment variables:
```
export VULKAN_SDK=/path/to/vulkan/sdk
# Required for Mac/MoltenVK
export VK_ICD_FILENAMES=/path/to/vulkan/sdk/etc/vulkan/icd.d
```

Then build BURN:
```
git clone https://github.com/angelocarly/BURN.git
git submodule update --init --recursive
cd BURN && mkdir build && cd build
cmake ..
make
```

## Dependencies
- [spdlog (unused)](https://github.com/gabime/spdlog) - Fast header only logging library.
- [glfw (unused)](https://github.com/glfw/glfw) - Cross platform window and input library.
- [glm (unused)](https://github.com/g-truc/glm) - OpenGL Math Library, wonderful to use imo.
- [Vulkan SDK (unused)](https://vulkan.lunarg.com) - Low level graphics API.
- [VulkanMemoryAllocator (unused)](https://github.com/GPUOpen-LibrariesAndSDKs/VulkanMemoryAllocator) - Easy to integrate Vulkan memory allocator.
- [Dear Imgui (unused)](https://github.com/ocornut/imgui) - Lightweight, feature full gui library.
- [stbi (unused)](https://github.com/nothings/stb) - PNG library
- [ImGuiFileDialog (unused)](https://github.com/aiekick/ImGuiFileDialog) - File dialog written for Dear Imgui

