#Cmake学习
mkdir -p cmakeStudy/build
cd cmakeStudy/build
cmake ..
make

#jsoncpp下载编译
源码下载地址：https://github.com/open-source-parsers/jsoncpp

mkdir -p jsoncpp/build
cd jsoncpp/build
cmake ..
make
将lib和头文件拷贝到cmakeStudy/third_party/jsoncpp下