---
layout:         post
title:          ����CSS�������ȼ�������
subtitle:       CSS priority level
card-image: 
date:           2016-5-14 9:00:19
tags:           code
post-card-type: code
---

## ����


> !important > ������ʽ>IDѡ���� > ��ѡ���� > ��ǩ > ͨ��� > �̳� > �����Ĭ������

�򵥵ļ��㷽����Ȩֵʵ�ʲ����ǰ�ʮ���ƣ������ֱ�ʾֻ��˵��˼�룬һ���classҲ����һ��idȨֵ�ߣ�

- ������ʽ���ȨֵΪ 1000 &nbsp; &nbsp;&nbsp;&nbsp;( style : " " )
- ID ѡ������ȨֵΪ 100  &nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;  ( id = " " )
- Class ��ѡ������ȨֵΪ 10    &nbsp;&nbsp;     ( class = " " )
- HTML ��ǩѡ������ȨֵΪ 1&nbsp;&nbsp;( div,p... )

## ����




```
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style type="text/css">
        div.test{
            background-COLOR:#a00;
            width:100px;
            height: 100px;
        }

        .test.test2{
            background-COLOR:#0e0;
            width:100px;
            height: 100px;
        }
    </style>
</head>
<body>
    <div class="test test2"></div>
</body>
</html>
```
###����div��Ӧ������������?

div.class��Ȩֵ��1+10=11����.test1 .test2��Ȩֵ��10+10=20������div��Ӧ��.test1 .test2�����ɫ��

##��ע��ģ�

�����١�!important�����ȼ�����ߵģ���Ҫ����ʹ��;

�����ڡ����ȼ���ͬʱ������þͽ�ԭ��ѡ�������ֵ���ʽ;

�����ۡ��̳е��������ԣ������ȼ����;







���販��ת�أ��븽��ԭ������

���͵�ַ��http://www.cnblogs.com/zxjwlh
