---
layout:         post
title:          phpʵ�ַ�ҳ
subtitle:       pagination by php
card-image:     https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1508909709290&di=84ae3e65c50c06b8aba003aac9098c2c&imgtype=0&src=http%3A%2F%2Fwww.sucaihuo.com%2Fjquery%2F11%2F1175%2Fbig.jpg
date:           2017-10-02 8:04:15
tags:           code
post-card-type: image
---

```html
    <!DOCTYPE html>    
    <html xmlns="http://www.w3.org/1999/xhtml">    
    <head>    
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />    
    <meta name="viewport" content="width=device-width, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no" />    
    <link href="http://apps.bdimg.com/libs/bootstrap/3.3.0/css/bootstrap.min.css" rel="stylesheet">    
    <script src="http://apps.bdimg.com/libs/jquery/2.0.0/jquery.min.js"></script>    
    <script src="http://apps.bdimg.com/libs/bootstrap/3.3.0/js/bootstrap.min.js"></script>    
    </head>       
    <body>    
    <div class="panel panel-default">    
        <div class="panel-body">    
            <table class="table table-hover">    
                <thead>    
                    <tr>    
                        <th>a</th>    
                        <th>b</th>    
                        <th>c</th>    
                        <th>d</th>    
                        <th>e</th>    
                        <th>f</th>    
                    </tr>    
                </thead>    
                <?php if($num>0){?>    
                <tbody>    
                <?php  while($row=mysql_fetch_array ( $res ) ){?>    
                    <tr>    
                        <td><?php echo $row['a'];?></td>    
                        <td><?php echo $row['b'];?></td>    
                        <td><?php echo $row['c'];?></td>    
                        <td><?php echo $row['d'];?></td>    
                        <td><?php echo $row['e'];?></td>    
                        <td><?php echo $row['f'];?></td>    
                        <!--<td><?php if($row['dingdan_status']==1){?><span class="label label-success">�Ѹ�</span><?php }else{?><span class="label label-warning">δ��</span><?php }?></td>-->    
                    </tr>    
                <?php }?>    
                <?php }else{?>    
                <tr><td colspan="6" class="text-center">���޼�¼</td></tr>    
                <?php }?>    
                </tbody>    
            </table>    
            <ul class="pagination">    
            <?php    
            if ($page != 1) { //ҳ��������1    
            ?>    
                <li><a href="List.php?page=<?php echo $page - 1;?>">?</a></li>    
            <?php    
            }    
            for ($i=1;$i<=$totalPage;$i++) {  //ѭ����ʾ��ҳ��    
            ?>    
                <li><a href="List.php?page=<?php echo $i;?>"><?php echo $i ;?></a></li>    
            <?php    
            }    
            if ($page<$totalPage) { //���pageС����ҳ��,��ʾ��һҳ����    
            ?>    
                <li><a href="List.php?page=<?php echo $page + 1;?>">?</a></li>    
            <?php    
            }     
            mysql_close( $link );    
            ?>    
            </ul>    
        </div>    
    </div>    
    </body>    
    </html>  
	
	
	
```php    
<?php    
    ///////////    
    //���ݿ�����    
    ///////////    
    //����ȡ��list������������    
    $perNumber = 15; // ÿҳ��ʾ�ļ�¼��    
    $page = $_GET ['page']; // ��õ�ǰ��ҳ��ֵ    
    $count = mysql_query ( "select count(*) from `list` "); // ��ü�¼����    
        
    $rs = mysql_fetch_array ( $count );    
    $totalNumber = $rs [0];    
    $totalPage = ceil ( $totalNumber / $perNumber ); // �������ҳ��    
    if (! isset ( $page )) {    
        $page = 1;    
    } // ���û��ֵ,��ֵ1    
    $startCount = ($page - 1) * $perNumber; // ��ҳ��ʼ,���ݴ˷����������ʼ�ļ�¼    
        
    // ����ǰ��ļ������ʼ�ļ�¼�ͼ�¼��    
    $sqq="select * from `list` limit $startCount,$perNumber";    
    $res=mysql_query($sqq);    
    $num=mysql_num_rows($res);    
        
?> 
```