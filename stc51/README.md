# STC51 Doc

> 我们使用 sdcc 作为硬件编译器开发 51 单片机。

## 下面是一个程序的 demo

```c
// 头文件
#include "mcs51/stc12.h"
#include "mcs51/8052.h"

// 延时函数 单位是 ms
void delay_ms(unsigned int ms) {
    unsigned int i, j;
    for(i=ms;i>0;i--)
        for(j=112;j>0;j--);
}

void main() {
    P1_1 = 0;
    delay_ms(1000);
    P1_1 = 1;
    while(1);
}
```