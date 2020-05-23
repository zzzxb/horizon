# HelloWorld

```c++
#include<iostream>

using namespace std;

int main() {
    cout << "Hello World!" << endl;
    return 0;
}
```

## 安装 C++

* Linux 上 安装 **Clang, GNU** 都带有 C/C++ 编译器的
* MAC 通过 上边两个也能安装到， 通过 **Xcode** 也能自动安装
* Windows 通过 **MinGW**

## 编译

* `gcc main.cpp -lstdc++ -o main` 通过 gcc 链接到 C++ 库 进行编译, -o 指定 编译后文件名字
* `g++ main.cpp` 直接通过 g++ 来编译 cpp 代码
* `g++ -g -Wall -std=c++11 main.cpp` 指定 c++ 版本编译
* `g++ -help` 可以查看更多c++帮助信息