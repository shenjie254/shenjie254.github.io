---
title: graphviz教程2（有向图）
categories: 实用工具
tags: Python
date: 2018-12-05 21:29:00
---
本次博文的内容主要为：新建两个节点A、B，然后使用一条线段连接节点A、B，所谓的有向图指的就是连接节点A、B的这条线段有箭头表示方向。如下为代码实现的过程。
<!--more--> 
### 教程如下
```
import graphviz as gv

#创建图对象g1和两个节点A、B，并连接A、B
g2=gv.Digraph(format='png')
#g2.attr(dpi='500')
g2.node('A')
g2.node('B')
g2.edge('A','B')
print(g2.source)
#生成PNG图片
filename=g2.render(r'C:\Users\just\Desktop\有向图')
print(filename)
```

### 所得png图形 
![有向图](http://graphbed.touchcfd.com/images/2018/12/05/9554cde48c9d04be7b7ea82af83c1628.png)
### graphviz格式的命令流
![graphviz有向图](http://graphbed.touchcfd.com/images/2018/12/05/graphz.jpg)