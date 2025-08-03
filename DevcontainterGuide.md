# Docker使用

## 拉取镜像

```bash
docker pull yuflyingfish/nav_sim:v1.0
```

## 创建容器

```bash
docker run --name nav_test --gpus all -dit --ipc=host --net=host --privileged -e DISPLAY=host.docker.internal:0.0 -e NVIDIA_DRIVER_CAPABILITIES=all docker.io/yuflyingfish/nav_sim:v1.0
```

## 编译

```bash
colcon build --symlink-install
```

## 安装groot2

```bash
chmod +x . Groot2-v1.5.0-linux-installer.run
./Groot2-v1.5.0-linux-installer.run
```
