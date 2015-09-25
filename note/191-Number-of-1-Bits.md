---
layout: post
title: "191-Number-of-1-Bits"
difficulty: Easy
date: 2015-09-25 23:45 +0800
tags: [Bit Manipulation]
---

## 191 Number of 1 Bits

Write a function that takes an unsigned integer and returns the number of ’1' bits it has (also known as the Hamming weight).

For example, the 32-bit integer ’11' has binary representation 00000000000000000000000000001011, so the function should return 3.

## Solution && Code

求数字中一比特的个数。没什么难点，循环移位，一边移位一边做与判断。

代码（C）：

```
int hammingWeight(uint32_t n) {
        int count = 0;
        uint32_t i = 1;
        uint32_t temp = 0;
        int result = 0;
 
        while(count++<=32){
            temp = n & i;
            if(temp!=0)
                result++;
            i<<=1;
        }
        return result;
}
```


