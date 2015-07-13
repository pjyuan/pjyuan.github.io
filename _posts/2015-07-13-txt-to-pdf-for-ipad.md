---
title: 通过python将txt转化为指定格式的pdf
author: pjyuan
comments: true
layout: post
categories: [python]
tags : [python]
date: 2015-07-13 10:00
---
最近经常用pad看pdf格式的小说，一般都是将txt的内容粘到word中，在word中调好格式（黑体，小四，1.5倍行距，页边距调小）。一遍遍重复这个过程比较繁琐，于是通过python实现了这个过程。


python生成pdf文件采用外置包reportlab，由于字体限制，需要收到在\Python27\Lib\site-packages\reportlab\fonts下添加SURSONG.TTF文件。对pdf格式的设置如下：
	
	normalStyle.fontName ='hei' #字体为黑体
    normalStyle.fontSize = 14.5 #字体大小
    normalStyle.leading = 30    #行间距
    normalStyle.firstLineIndent = 32    #首行缩进


最后实现，可以将此程序同一目录下的所有txt文件全部转化为指定格式的pdf文件。[源码](https://github.com/pjyuan/App/tree/master/txt2PDF)。转化后的pdf在pad上的效果见下图：
![ipd效果图](/wp-content/uploads/2015/07/ipadPDF.jpg =500x)


###参考资料
* http://blog.chinaunix.net/uid-25979788-id-2986379.html
* http://blog.csdn.net/liangyuannao/article/details/8897260