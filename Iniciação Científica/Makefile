VULKAN_SDK_PATH = /home/bruna/Documentos/vulkan/VulkanSDK/1.0.57.0/x86_64

CFLAGS = -std=c++11 -I$(VULKAN_SDK_PATH)/include
LDFLAGS = -L$(VULKAN_SDK_PATH)/lib `pkg-config --static --libs glfw3` -lvulkan


All: Teste1 Teste2

Teste1: Teste1.cpp
	g++ $(CFLAGS) -o $@ $< $(LDFLAGS)

Teste2: Teste2.cpp
	g++ $(CFLAGS) -o $@ $< $(LDFLAGS)

.PHONY: test clean

test: Test1
	LD_LIBRARY_PATH=$(VULKAN_SDK_PATH)/lib VK_LAYER_PATH=$(VULKAN_SDK_PATH)/etc/explicit_layer.d ./VulkanTest

clean:
	rm -f Test1
