# MeshTrunk

MeshTrunk 是一套面向 3D 打印模型库的本地管理软件，用于上传、整理、预览、检索和下载 3D 模型。软件安装后会在本机启动 Web 服务，通过浏览器访问：

```text
http://localhost:7998
```

默认登录信息：

```text
账号：admin
密码：3dmaker
```

![MeshTrunk 功能界面展示](docs/images/meshtrunk-showcase.gif)

## 功能介绍

- 模型库管理：支持模型上传、编辑、删除、分类、标签、搜索、浏览量和下载量统计。
- 前台展示控制：后台可控制模型是否在前台展示，关闭后仅后台可见。
- 多格式支持：支持 `STL`、`OBJ`、`3MF`、`GLB`、`GLTF`、`STEP`、`STP`、`IGS`、`IGES` 等模型文件。
- 3D 在线预览：支持旋转、缩放、视角切换、正交/透视、剖切、线框、透明模式和尺寸查看。
- 3MF 分盘预览：支持解析 3MF 分盘信息，并在模型详情页切换分盘 3D 视图。
- 单文件、分组和批量导入：支持单个模型、多文件分组、批量文件和压缩包导入。
- 缩略图和说明书：支持模型缩略图、PDF 说明书等附件资源。
- AI 标签：支持本地 ONNX、LLM 或混合模式自动生成模型标签。
- 后台管理：提供模型管理、分类管理、系统设置、AI 配置、更新检测和数据看板。
- 授权激活：支持试用、激活码、机器码绑定和定期远程校验。

说明：`STEP/STP/IGS/IGES` 的高精度转换依赖原生 `occ_bridge` 库。未安装对应原生库时，这几类格式的原生转换功能会禁用，但 `STL/OBJ/3MF/GLB/GLTF` 等常用格式不受影响。

## 下载安装

请进入 Releases 页面下载对应平台的最新安装包：

```text
https://github.com/TrunkBar/MeshTrunk-Releases/releases
```

## Windows

### 环境要求

- Windows 10 / Windows 11，64 位系统。
- 建议内存 8GB 以上，模型较大时建议 16GB 以上。
- 建议预留 5GB 以上磁盘空间，实际空间取决于上传模型数量。
- 需要可用浏览器，例如 Edge、Chrome。

### 使用 MSI 安装包

推荐普通用户下载：

```text
MeshTrunk-<版本号>.msi
```

安装步骤：

1. 双击 `MeshTrunk-<版本号>.msi`。
2. 按安装向导完成安装。
3. 从桌面快捷方式或开始菜单启动 MeshTrunk。
4. 浏览器打开后访问：

```text
http://localhost:7998
```

如重复点击启动程序，软件会检测本机服务是否已经运行；如果已经运行，会直接打开浏览器访问现有服务。

### 使用 Windows 便携版

不想安装到系统时，可以下载：

```text
MeshTrunk-<版本号>-windows-portable.zip
```

使用步骤：

1. 解压 `MeshTrunk-<版本号>-windows-portable.zip`。
2. 进入解压后的目录。
3. 运行启动脚本或启动程序。
4. 浏览器访问：

```text
http://localhost:7998
```

## Linux

### 环境要求

- Debian / Ubuntu 64 位系统，推荐 Ubuntu 22.04 或 Ubuntu 24.04。
- 建议内存 8GB 以上，模型较大时建议 16GB 以上。
- 建议预留 5GB 以上磁盘空间，实际空间取决于上传模型数量。
- 需要可用浏览器访问 Web 页面。

极简 Linux、NAS Docker 或容器环境如遇到验证码、缩略图相关字体错误，请安装字体组件：

```bash
apt update
apt install -y fontconfig fonts-dejavu-core fonts-dejavu-extra \
  libfontconfig1 libfreetype6 libharfbuzz0b libgraphite2-3 \
  libpng16-16 libbrotli1
```

### 使用 DEB 安装包

适用于 Debian / Ubuntu，推荐下载：

```text
meshtrunk_<版本号>-1_amd64.deb
```

安装步骤：

```bash
sudo apt install ./meshtrunk_<版本号>-1_amd64.deb
```

启动方式：

```bash
/opt/meshtrunk/bin/meshtrunk
```

启动后访问：

```text
http://localhost:7998
```

如当前系统没有 `sudo`，请使用 root 用户执行安装命令。

### 使用 Linux 便携版

不想安装 deb 时，可以下载：

```text
meshtrunk-<版本号>-linux-x64.tar.gz
```

使用步骤：

```bash
tar -xzf meshtrunk-<版本号>-linux-x64.tar.gz
cd meshtrunk
./bin/meshtrunk
```

启动后访问：

```text
http://localhost:7998
```

## 数据与升级

- 模型文件、数据库和激活记录会保存在软件数据目录中，重新安装同版本或升级安装不会主动删除已有数据。
- 升级前建议先停止正在运行的 MeshTrunk，再安装新版本。
- 如需完全卸载并清空数据，请先备份需要保留的模型文件和数据库。
