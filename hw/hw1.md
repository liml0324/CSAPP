## hw1

### 2.58
![alt text](hw1_src/image.png)
```C
int is_little_endian() {
    int x = 1;
    return *(char *)&x;
}
```

### 2.61
![alt text](hw1_src/image-1.png)
```C
(!(x+1)) | (!x) | (!((x & 0xFF) ^ 0xFF)) | (!((x >> ((sizeof(int)-1) << 3)) & 0xFF))
```

### 2.77
![alt text](hw1_src/image-2.png)

A:
```C
K << 4 + K
```

B:
```C
-(K << 3 - K)
```

C:
```C
(K << 6) - (K << 2)
```

D:
```C
(K << 4) - (K << 7)
```

### 2.84
![alt text](hw1_src/image-3.png)

```C
((sx == 1) && (sy == 0)) || \
((ux << 1) == 0 && (uy << 1) == 0) || \
(sx == 0 && sy == 0 && ux <= uy) || \
(sx == 1 && sy == 1 && ux >= uy)
```

### 2.89
![alt text](hw1_src/image-4.png)
**表达式A**：
总是为1。double可以精确表达的整数范围比32位int更大，因此dx与x表示同样的精确整数，转换为float的结果也是一样的。

**表达式B**：
x取2^31-1，y取-3时为0。因为左边没有溢出，右边会溢出。

**表达式C**：
