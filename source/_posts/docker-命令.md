---
title: docker-命令
tags: 'java'
categories: 'docker-命令'
---
#### docker 镜像命令
````
docker images [options] 查看镜像 options -q:只显示镜像id -a:列出本地所有镜像(含中间映像层) --digests:显示镜像的摘要信息 --no-trunc:显示完整的镜像信息
docker run <镜像名称> 运行镜像如果没有会从远程仓库获取镜像
docker search [options] 镜像名  optione说明: --no-trunc:显示完整的镜像描述 -s:列出收藏数不小于指定值的镜像 --auto mated: 列出automated build类型的镜像
docker pull 镜像名称[:tag] tag:版本号默认为 latest(最新的) 下载镜像
docker rmi [options] 删除镜像 options: -f 镜像id -f 镜像名:tag 镜像名2:tag -f
````
#### 容器命令
````
docker run [options] image [command][ARG..] option: --name 镜像名 -d 后台运行 -i交互模式运行 -t 为容器分配一个伪输入终端it通常都是一起使用 -P 随机端口 -p 指定端口 主机端口:镜像端口
docker ps [options] options: -a:列出当前所有正在运行和历史上运行的容器 -l:显示最近创建的容器 -n:显示最近n个创建的容器 -q:只显示容器编号 --no-trunc:不截断输出
exit 容器内部执行停止退出容器 ctrl+p+q 退出容器不停止(退出伪终端，后台运行容器)
docker start 容器id或容器名称 启动容器
docker restart 容器id或容器名称 重启容器
docker stop 停止容器
docker kill 容器id或容器名称 强制停止
docker rm 容器id 删除
docker rm -f $(docker ps -a -q) 删除多个
docker top 容器id 查看容器内运行的进程 
docker inspect 容器id 查看容器内部细节
docker exec [-it] 容器id 命令 容器id 进入容器 启动新进程 命令:linux命令 docker ecex xxxxx ls -l
docker attach 容器id 进入容器 不会产生新进程
docker cp 容器id:容器内路径 目的主机路径
```` 
