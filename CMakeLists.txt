cmake_minimum_required(VERSION 3.11.4)
# 工程名
PROJECT(cmakeStudy)

set(CMAKE_CXX_STANDARD 11) 

SET(CMAKE_C_FLAGS_DEBUG "-fPIC -D_FORTIFY_SOURCE=2 -pthread -Wfloat-equal -Wshadow -Wformat=2 -frandom-seed=0 -Wno-deprecated -fstack-protector-strong -Wall -Wextra")
SET(CMAKE_C_FLAGS_RELEASE "-o1 -fPIC -D_FORTIFY_SOURCE=2 -pthread -Wfloat-equal -Wshadow -Wformat=2 -frandom-seed=0 -Wno-deprecated -fstack-protector-strong -Wall -Wextra")
SET(CMAKE_CXX_FLAGS_DEBUG "-fPIC -D_FORTIFY_SOURCE=2 -pthread -Wfloat-equal -Wshadow -Wformat=2 -frandom-seed=0 -Wno-deprecated -fstack-protector-strong -Wall -Wextra")
SET(CMAKE_CXX_FLAGS_RELEASE "-o1 -fPIC -D_FORTIFY_SOURCE=2 -pthread -Wfloat-equal -Wshadow -Wformat=2 -frandom-seed=0 -Wno-deprecated -fstack-protector-strong -Wall -Wextra")

#SET(CMAKE_C_FLAGS_DEBUG "$ENV{CFLAGS} -g -DDEBUG ")
#SET(CMAKE_C_FLAGS_RELEASE "$ENV{CFLAGS} -g -O3 -DNDEBUG ")
#SET(CMAKE_CXX_FLAGS_DEBUG "$ENV{CXXFLAGS} -std=c++11 -g -DDEBUG -Wall -Wno-reorder -Wno-unused-variable -Wno-unused-function -fexceptions -Wno-unused-result -ldl")
#SET(CMAKE_CXX_FLAGS_RELEASE "$ENV{CXXFLAGS} -std=c++11 -g -O3 -DNDEBUG -Wall -Wno-reorder -Wno-unused-variable -Wno-unused-function -fexceptions -Wno-unused-result -ldl")

# 编译模式
SET(CMAKE_BUILD_TYPE Debug)
#SET(CMAKE_BUILD_TYPE Release)


#设置库的存放路径
SET(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/libs)
#设置可执行文件输出目录
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)

#编译自己造的公共接口
ADD_SUBDIRECTORY(common)

#编译业务代码
ADD_SUBDIRECTORY(src)