---
title: docker学习笔记
tags: docker
---
1、例如：安装node（在不新建dockerfile和编辑dockercompose的情况下）

docker pull node：拉取node镜像（类似下载安装包）
docker run --name nodejs node:latest：运行镜像
docker run -i -t -d --name node-js node:latest：建立一个容器
docker exec -it 775c2778144c bash：进入容器

注：以上方法在重启虚拟机之后，node容器会被删除，每次都要重新建立，所以最好还是用dockerfile+dockercompose方式

2、每次修改dockercompose（运行镜像的文件）文件后都要cd 到dockercompose所在文件夹
docker-compose down
docker-compose up -d

3、每次修改dockerfile（制作镜像的文件）之后，都要执行
docker-compose down
docker rmi 镜像（删除images）
docker-compose up -d

4、dockercompose里面build和image
每个docker-compose.yml必须定义image或者build中的一个，其它的是可选的。
build：用来指定一个包含Dockerfile文件的路径。一般是当前目录.
image:指定镜像tag或者ID

5、制作镜像image的两种方法
（1）访问Docker Hub可以获取需要的镜像 ：https://hub.docker.com
类似1步骤
（2）dockerfile制作