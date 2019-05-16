---
title: laravel学习笔记
tags: laravel
---

#php常用3种通讯方式
1、nginx+php-fpm
http向nginx发送请求，ngnix将请求发送给php-fpm，php-fpm执行php逻辑，给出响应返回给ngnix，ngnix再响应给http
2、cli
在命令行操作php程序
3、server
能实现nginx+php-fpm的功能，但是php的server受性能限制，在本地调试可以用，但是生产者模式基本不用
为了避免每次都需要启动server，可以在docker-compose文件里面command添加：php artisan serve（laravel的server启动命令）
#lavarel站点配置
1、修改serveCommand文件getOptions方法里面的端口号（默认8000）
2、进入laravel项目目录执行php artisan serve
为了避免每次都需要启动server，可以在docker-compose文件里面command添加：php artisan serve（laravel的server启动命令）
3、在nginx的vhost里面配置站点