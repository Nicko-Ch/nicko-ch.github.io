---
title: "Git恢复之前版本的两种方法reset、revert"
date: 2021-06-04
tags: 
  - Git
draft: false
---

**方法一：git reset**

**原理：** git reset的作用是修改HEAD的位置，即将HEAD指向的位置改变为之前存在的某个版本，如下图所示，假设我们要回退到版本一：

![img](../../static/images/202106040000/aHR0cDovL2ltZy5ibG9nLmNzZG4ubmV0LzIwMTgwNDE0MjEyMjIxMDMz.png)

**适用场景：** 如果想恢复到之前某个提交的版本，且那个版本之后提交的版本我们都不要了，就可以用这种方法。

**具体操作：**

**1. 查看版本号：**

可以使用命令“git log”查看：

![img](../../static/images/202106040000/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3l4bHNoaw==,size_16,color_FFFFFF,t_70.png)

也可以在github网站上查看：

![img](../../static/images/202106040000/aHR0cDovL2ltZy5ibG9nLmNzZG4ubmV0LzIwMTgwNDE0MjAzMzQ0MTM4.png)