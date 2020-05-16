VULKAN_SDK_PATH = /Users/jsm/vulkansdk-macos-1.2.135.0/macOS
CFLAGS = -std=c++17 -I$(VULKAN_SDK_PATH)/include `pkg-config --cflags glfw3 glm`
LDFLAGS = -L$(VULKAN_SDK_PATH)/lib `pkg-config --static --libs glfw3 glm` -lvulkan

hello-triangle: hello-triangle.cpp
	g++ $(CFLAGS) -o hello-triangle hello-triangle.cpp $(LDFLAGS)

.PHONY: test clean

test: hello-triangle
	./hello-triangle

clean:
	rm -f hello-triangle
