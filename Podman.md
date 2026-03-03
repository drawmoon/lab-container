Podman 完全兼容 Docker 命令，你可以像使用 Docker 一样使用 Podman，例如：`podman images`。

Podman vs Docker:
- 无需进程守护
- 无需 Root 权限，原生支持 Rootless 普通用户即可运行
- CLI 直接调用 runc
- 支持将多个容器组合成 Pod（类似 Kubernetes）

Podman 默认不支持镜像名称的简写，需要全名称，例如：
```sh
podman pull docker.io/library/alpine
```

### 安装 Podman

```sh
sudo apt update
sudo apt install -y podman
```

### 配置镜像加速

```sh
mkdir -p ~/.config/containers
vim ~/.config/containers/registries.conf
```
```toml
unqualified-search-registries = ["docker.io", "quay.io"]

[[registry]]
prefix = "docker.io"
location = "f1361db2.m.daocloud.io"
```

### 安装 Podman-Compose：
```sh
sudo apt install podman-compose
```

Podman-Compose 也与 Docker-Compose 完全兼容。