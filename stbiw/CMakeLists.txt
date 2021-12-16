# 创建stbiw动态库
add_library(stbiw SHARED stb_image_write.c)
# 在子库文件夹里设置头文件搜索路径；并设置为PUBLIC属性，使之能够在被包含时不用写明具体路径
target_include_directories(stbiw PUBLIC .)
