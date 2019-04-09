---
title: 搭建github-blog
date: 2019-04-09 01:19:43
tags: judith1992
---
#github-blog
工具：docker,nodejs,npm,git,hexo
1、dockerfile,docker-compose
2、编辑_config.yml
3、每次编辑完文件，执行hexo d，hexo g
注意：
在github添加ssh
1、执行：ls -al ~/.ssh
2、执行：ssh-keygen -t rsa -C "your_email@example.com"（然后3下enter）
3、执行：cat ~/.ssh/id_rsa.pub
4、在映射docker里面和docker外面的ssh
一般ssh生成在/root下面