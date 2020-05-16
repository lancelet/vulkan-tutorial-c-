VULKAN_SDK_PATH = /Users/jsm/vulkansdk-macos-1.2.135.0/macOS
CFLAGS = -std=c++17 -I$(VULKAN_SDK_PATH)/include `pkg-config --cflags glfw3 glm`
LDFLAGS = -L$(VULKAN_SDK_PATH)/lib `pkg-config --static --libs glfw3 glm` -lvulkan

VulkanTest: main.cpp
	g++ $(CFLAGS) -o VulkanTest main.cpp $(LDFLAGS)

.PHONY: test clean

test: VulkanTest
	./VulkanTest

clean:
	rm -f VulkanTest
