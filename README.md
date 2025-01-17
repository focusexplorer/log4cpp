## 基于以下代码构建，当前仓库未修改原代码
https://log4cpp.sourceforge.net/ 
原代码最后更新日期2016年，可以直接构建。

## 源代码可以直接编译
不建议使用CMakeLists.txt，可以直接configure构建。
### 先安装相关工具
```bash
sudo apt-get install autotools-dev
sudo apt-get install autoconf
./configure  --prefix=`pwd`/myinstall
make -j 10
make install
```
### 
然后所有相关库都会被安装到当前目录的myinstall目录。


如果只编译静态库可以指定--enable-shared=no，./configure -h可以看到其它相关配置信息。
```bash
./configure --enable-shared=no --prefix=`pwd`/myinstall
```