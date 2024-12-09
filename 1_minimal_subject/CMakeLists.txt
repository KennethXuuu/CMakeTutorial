# 明确文件使用cmake语法 所需要的最低cmake版本
# Version 3.2 is perhaps the oldest any modern cmake project should consider
cmake_minimum_required(3.2)

#[[
指定项目名称和项目语言  C,CXX,Fortran,ASM,CUDA and others.
希望表面不用任何语言时  LANGUAGES NONE
如果没有指定语言类型    cmake 默认是 C and CXX
cmake VERSION_3.0之前的版本不支持 LANGUAGES 选项
]]
Project(minimal_subject CXX)
#[[项目名称在语言设置以外的作用:
1. 检查每种启用语言的编译器,并确保它们能够编译和链接成功
检查的结果和参数->CMakeCache.txt
2. 检查通过后 设置对应的变量属性
]]
#[[
三种等价写法
add_executable(minimal_demo main.cpp)
ADD_EXECUTABLE(minimal_demo main.cpp)
Add_Executable(minimal_demo main.cpp)
              (targetName  source_files...)
一个CMakeLists里可以写多个不同target      
]]
add_executable(minimal_demo main.cpp)

message(" this project choose not set target")

#no target
