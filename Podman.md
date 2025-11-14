podman 完全兼容 docker 命令，你可以像使用 docker 一样使用 podman，例如：`podman images`。

podman vs docker:
- 无需进程守护
- 无需 root 权限
- cli 直接调用 runc
- 整合了 k8s pod

在 Ubuntu 中安装 Podman:
```sh
sudo apt install podman
```

podman 默认不支持镜像名称的简写，需要全名称，例如：
```sh
podman pull docker.io/library/alpine
```

安装 podman-compose：
```sh
sudo apt install podman-compose
```

podman-compose 也与 docker-compose 完全兼容。