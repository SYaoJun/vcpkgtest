# vcpkg
C/C++三方依赖包管理工具
## 安装vcpkg
```bash
git clone https://github.com/microsoft/vcpkg.git 
cd vcpkg 
./bootstrap-vcpkg.sh  # Linux/macOS
```
## 配置环境变量
vim ~/.bashrc
```bash
export PATH=$PATH:/root/vcpkg/
export VCPKG_ROOT=/root/vcpkg
```
## 常用命令
```bash
# 查看安装的库
vcpkg list
# 查看版本
vcpkg --version
```

## 编译C/C++
注意vcpkg改成自己的路径
```bash
vcpkg install 
cmake -B build -S . -DCMAKE_TOOLCHAIN_FILE=/root/vcpkg/scripts/buildsystems/vcpkg.cmake
cmake --build build
```