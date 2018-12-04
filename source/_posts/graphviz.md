---
title: graphviz教程1（无向图）
categories: 实用工具
tags: Python
date: 2018-12-04 21:45:00
---
本次博文的内容主要为：新建两个节点A、B，然后使用一条线段连接节点A、B，所谓的无向图指的就是连接节点A、B的这条线段没有箭头表示方向。如下为代码实现的过程。
<!--more--> 
### 教程如下
```

import graphviz as gv

#创建图对象g1和两个节点A、B，并连接A、B
g1=gv.Graph(format='svg') #图片格式设置为png
g1.attr(dpi='500')        #图片dpi设置为500
g1.node('A')
g1.node('B')
g1.edge('A','B')
print(g1.source) #输出graphviz格式的命令流

#生成PNG图片
filename=g1.render(filename=r'C:\Users\just\Desktop\无向图')
print(filename) 


```
### 所得png图形  
![无向图](http://cfd.red/?/images/2018/12/04/X2NblywgvK/%E6%97%A0%E5%90%91%E5%9B%BE.png)
### graphviz格式的命令流
![graphviz](http://cfd.red/?/images/2018/12/04/cetbo7dHHd/%E8%BE%93%E5%87%BA.JPG)