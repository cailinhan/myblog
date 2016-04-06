<!--
author: jockchou
date: 2015-07-30
title: Hello World!
tags: GitBlog
category: GitBlog
status: publish
summary: 你好！GitBlog
-->

#  java数组

>学习Java的数组

数组需要声明和初始化，初始化过的数组具有默认值
- 字符串为空格
- 整数类型为0
- 浮点数类型为0.0
- 布尔类型为false
- 引用类型为null


foreach用法
```
int[] arraya = new int[]{1,2,3,4,5,6};
for(int i : arraya){
    System.out.println(i);
}
```

数组是引用传递
```
System.out.println("数组赋值");
int[] arrayb;
arrayb = arraya;
arraya[5] = 1;
System.out.println("数组A:" + arraya[5]); //数组A:1
System.out.println("数组B:" + arrayb[5]); //数组B:1
for(int i : arrayb){
    System.out.println(i);
}
```

数组在初始化的时候分配堆内存
![Alt text](./img.jpeg "Optional title")