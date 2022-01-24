# Docker NOTES

## 常用命令



- run
- start
- stop
- images
- container
- ps
- pull
- push
- build

### run

启动一个新容器

#### 选项

- -d --detach 后台启动
- --rm 容器退出后删除
- -p 暴露端口 (-p 80:80) 冒号前是暴露出来的端口，冒号后是容器内端口
- -P 暴露全部端口，外部端口随机
- --env 容器内环境变量
- --volume 挂载外部文件夹到容器内

#### Example

```bash
docker run -d -p 80:80 docker/getting-started
```



### stop

停止一个容器

#### 选项

- -t 等待容器停止的最大时间

#### Example

```bash
docker stop [container_id/container_name]
```

### start

启动一个已经存在的容器

#### Example

```bash
docker start [container_id/container_name]
```



### images

查看本地存在的镜像

#### Example

```bash
docker images
```



### ps

查看正在运行的容器

#### Example

```bash
docker ps
```



### container

容器相关的父级命令，常用container ls

#### Example

```bash
docker container ls # 显示正在运行的容器
docker container ls -a # 显示所有容器
```



### pull

拉取远程镜像

#### Example

```bash
docker pull docker/getting-started:latest  # 冒号后的latest是镜像的tag
# tag用于区分版本
```



### push

推送本地镜像到远程

#### Example

```bash
docker push my-image:1.0-yay
```



### build

构建镜像

#### 选项

-t 设置构建完成的镜像的名称

#### Example

```bash
docker build -t my-image:1.1-oh-yes . # 点是当前目录作为build-context
```

