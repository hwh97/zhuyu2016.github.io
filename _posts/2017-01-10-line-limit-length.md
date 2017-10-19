---
layout:         post
title:          Web�����ַ�����
subtitle:       line-limit-length
card-image:     https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1508415843019&di=f8e37a6bbc8502c33f84b1ae87cf28e1&imgtype=0&src=http%3A%2F%2Fwww.cdxwcx.com%2Fupload%2Fimage%2F20141120%2F201411201720148608691.png
date:           2017-01-10 2:24:10
tags:           code
post-card-type: image
---


> Ϊ�˱�֤ҳ����������ۣ��ںܶ��ʱ�����ǳ���Ҫ���س������ȵ����֡������б���Ŀ����Ŀ�����Ƶȵط����õ���

### 1. ���ֳ���һ�У�ʡ�Գ������֣���ʾ'...' 
   �����������Ƚ϶࣬����ȡһ���к����õ��������ڸ��á�
```html
.line-limit-length {
overflow: hidden;
text-overflow: ellipsis;
white-space: nowrap; //�ı������У���������һ�еĲ��ֱ���ȡ����ʾ...
}
<div class="item">
<p class="line-limit-length">������Ϣ�����ص���ڶ���ɲ⣬��ͣ������Χ��ˮ��</p>
<i class="icon icon-arrow-Go"></i> //ͼ������
</div>
```

![](http://img.blog.csdn.net/20160309193259989)

***
### 2. Ȼ���������������ƣ���������ʡ��
```html
.product-buyer-name {
max-width: 110px;
overflow: hidden;
text-overflow: ellipsis;
white-space: nowrap;
}
<h5 class="product-buyer-name">��������</h5>
<h5 class="product-buyer-name">�������������û�����</h5>
```
![](http://img.blog.csdn.net/20160309192609690)
![](http://img.blog.csdn.net/20160309192832691)
***
