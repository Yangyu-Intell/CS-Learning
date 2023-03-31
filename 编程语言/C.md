# C/C++

以下C代码在32位计算机上运行结果为：C

```c
#include <stdio.h>
int fun1(int i) {
 return i < 10 ? i
    : (5 * fun1(i-1) + 2 * fun1(i-2) + fun1(i-3) + fun1(i-4)) & 0x5fff;
}
 
int fun2(unsigned int i) {
 unsigned int f = 2020;
 return (f & i) / 2;
}
 
int main(int argc, const char* argv[]) {
  printf("%d\n", fun2(fun1(101)) % 4);
  return 0;
}
```
A. 0
B. 1
C. 2
D. 3