#cmake 最低要求版本号 
cmake_minimum_required(VERSION 2.8)

#项目信息
project(Demo3)

#指定生成的目标
#add_executable(Demo main.c MathFunctions.c)

# 查找当前目录下的所有源文件
# 并将名称保存在 DIR_SRCS变量内

aux_source_directory(. DIR_SRCS)

#添加math子目录
add_subdirectory(math)

#指定生成的目标
add_executable(Demo main.c)

#添加链接库
target_link_libraries(Demo MathFunctions)


