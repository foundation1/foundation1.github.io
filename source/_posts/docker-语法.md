---
title: docker-dockerFile
tags: 'java'
categories: 'docker-dockerFile'
---
#### 基本语法
````
FROM 基础镜像，当前新镜像是基于哪个镜像的
MAINTAINER 镜像作者的姓名和邮箱地址
RUN 容器构造时需要运行的命令
EXPOSE 当前容器对外暴露的端口
WORKDIR 进入容器时的文件目录
ENV 什么变量
ADD 拷贝文件并解压
COPY 拷贝文件没有解压功能
VOLUME 容器数据卷
CMD 指定容器运行启动时运行的命令 可以指定多个，但最终只有最后一个有效
ENTRYPOINT 容器启动时运行的命令 可以有多个 每个都有效
ONBUILD 钩子函数 当其他容器继承他 并且build时执行
````
