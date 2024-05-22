# compile GCC 13.3.0
## 环境
`Ubuntu 22.04.3 LTS`
```shell
sudo apt install openssh-server -y
sudo apt install gcc -y
sudo apt install g++ -y
sudo apt install make -y
```

```
$ gcc --version
gcc (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0
$ make --version
GNU Make 4.3
```

## 下载GCC源码
```shell
wget https://mirrorservice.org/sites/sourceware.org/pub/gcc/releases/gcc-13.3.0/gcc-13.3.0.tar.gz -O gcc-13.3.0.tar.gz
```
## 解压
```shell
tar xf gcc-13.3.0.tar.gz
```

## 下载依赖
```shell
cd gcc-13.3.0
./contrib/download_prerequisites
```

## 编译配置
```shell
mkdir obj
cd obj/
../configure --prefix=/opt/gcc13.3.0 --with-local-prefix=/opt/gcc13.3.0 --disable-multilib -
-disable-tls --enable-languages=c,c++
```
## 编译
```shell
make -j4
```
## 安装
```shell
sudo make install
```