# 编译helloworld.c
```shell
$ /opt/gcc13.3.0/bin/gcc -v -H helloworld.c -o helloworld
```

![头文件搜索路径](images/头文件搜索路径.png)

![依赖的头文件](images/加载所依赖的头文件.png)

![链接命令](images/链接命令.png)

# 运行helloworld
```shell
$ ./helloworld
Hello World!
```