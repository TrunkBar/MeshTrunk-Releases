# MeshTrunk

MeshTrunk 是一套面向 3D 打印模型库的本地管理软件，用于上传、整理、预览、检索和下载 3D 模型。

```text
默认访问地址：http://localhost:8080
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

## 下载安装

请在右侧或页面顶部进入 **Releases** 下载最新版本安装包：

```text
https://github.com/TrunkBar/MeshTrunk-Releases/releases
```

### Windows

环境要求：

- Windows 10 / Windows 11，64 位系统。
- 建议内存 8GB 以上，模型较大时建议 16GB 以上。
- 建议预留 5GB 以上磁盘空间，实际空间取决于上传模型数量。
- 安装包已内置 Java 运行环境，不需要单独安装 Java。

推荐下载：

```text
MeshTrunk-<版本号>.msi
```

便携版下载：

```text
MeshTrunk-<版本号>-windows-portable.zip
```

### Linux

环境要求：

- Debian / Ubuntu 64 位系统，推荐 Ubuntu 22.04 或 Ubuntu 24.04。
- 建议内存 8GB 以上，模型较大时建议 16GB 以上。
- 建议预留 5GB 以上磁盘空间，实际空间取决于上传模型数量。
- 安装包已内置 Java 运行环境，不需要单独安装 Java。

Ubuntu / Debian 推荐下载：

```text
meshtrunk_<版本号>-1_amd64.deb
```

Linux 便携版下载：

```text
meshtrunk-<版本号>-linux-x64.tar.gz
```

## 说明

此仓库仅用于公开发布 MeshTrunk 安装包和用户说明，不包含 MeshTrunk 私有源码。
