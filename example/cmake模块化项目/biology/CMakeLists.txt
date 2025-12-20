file(GLOB_RECURSE srcs CONFIGURE_DEPENDS src/*.cpp include/*.h)
add_library(biology STATIC ${srcs})                # 生成真实目标：创建库(默认静态库)，选项(STATIC、OBJECT、SHARED)
target_include_directories(biology PUBLIC include) # 为目标添加 头文件搜索路径 (作用域控制)
