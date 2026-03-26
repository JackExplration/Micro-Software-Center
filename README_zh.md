```markdown
# Micro Software Center - 轻量级跨发行版包管理器图形界面

[![License](https://img.shields.io/badge/License-GPLv3-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Linux-lightgrey.svg)]()
[![Memory](https://img.shields.io/badge/memory-5--10MB-brightgreen.svg)]()

> **为什么做这个项目？**
> 
> 我想要一个轻量级的软件中心。GNOME Software 占用 300+ MB 内存，KDE Discover 也很臃肿。  
> 当使用 Openbox、i3 或 XFCE 等轻量级桌面时，我想找一个图形化的包管理器却找不到。  
> 所以我自己动手做了一个。

---

## ✨ 功能特性

| 功能 | 说明 |
|------|------|
| 🪶 **极致轻量** | 仅占用 5-10 MB 内存 |
| 🐧 **跨发行版** | Fedora、RHEL、CentOS、Rocky、Alma、Debian、Ubuntu、Arch、openSUSE |
| 📦 **包管理** | 安装、卸载、搜索、更新软件包 |
| 🗂️ **仓库管理** | 启用/禁用/添加/删除软件源 |
| ⚙️ **一键添加第三方仓库** | RPM Fusion、EPEL、Google Chrome、VS Code、Docker、Brave、VirtualBox、Steam、Slack、Spotify |
| 🎯 **Flatpak 支持** | 从 Flathub 安装应用 |
| 🌍 **多语言** | 简体中文 / English |

## 🚀 快速安装

### 方法一：一键安装

```bash
git clone https://github.com/yourusername/micro-software-center.git
cd micro-software-center
./install.sh
```

### 方法二：手动安装

```bash
# 1. 安装依赖
# Fedora/RHEL
sudo dnf install yad bc

# Debian/Ubuntu
sudo apt install yad bc

# Arch Linux
sudo pacman -S yad bc

# openSUSE
sudo zypper install yad bc

# 2. 克隆项目
git clone https://github.com/yourusername/micro-software-center.git
cd micro-software-center

# 3. 运行（无需安装）
./micro-software-center

# 或者安装到系统
./install.sh
```

## 🎯 使用方法

启动软件中心：

```bash
micro-software-center
```

或者在应用菜单中找到“Micro Software Center”。

### 快捷键（应用内）

| 快捷键 | 功能 |
|--------|------|
| Ctrl+F | 搜索软件 |
| Ctrl+Q | 退出 |
| F5 | 刷新列表 |

## 🔧 开发故事

### 为什么做这个

2025 年初，我搭建了一个 Openbox 轻量级桌面，内存占用仅 40-60 MB。
一切都很好，直到我想安装软件时——只能用命令行 `dnf install`。

我试了 GNOME Software：它吃掉 300+ MB 内存，比我的整个桌面还多。
KDE Discover 也一样。
难道轻量级桌面用户就只能用命令行吗？

于是我开始了这个项目。
目标：5-10 MB 内存，图形界面，支持主流发行版。

### 开发历程

- **选择 GUI 工具**：YAD — 轻量、依赖少、功能足够强大
- **跨发行版支持**：检测 `/etc/*-release`，实现 dnf/apt/pacman/zypper 命令
- **仓库管理**：解析 `/etc/yum.repos.d/`，支持启用/禁用/添加/删除
- **一键添加第三方仓库**：RPM Fusion、EPEL、Google Chrome、VS Code 等
- **Flatpak 支持**：集成 flatpak 命令
- **多语言**：提取语言文件，支持英文和中文

### 当前状态

- **内存占用**：5-10 MB
- **代码行数**：约 1500 行
- **支持的发行版**：Fedora、RHEL、CentOS、Rocky、Alma、Oracle、Amazon、Debian、Ubuntu、Arch、openSUSE
- **支持的功能**：包管理、仓库管理、第三方仓库、Flatpak

## 📊 与其他软件中心对比

| 软件中心 | 内存占用 | 跨发行版 | 仓库管理 | 轻量优化 |
|----------|----------|----------|----------|----------|
| Micro Software Center | 5-10 MB | ✅ | ✅ | ✅ |
| GNOME Software | 300+ MB | ❌ (仅 GNOME) | ❌ | ❌ |
| KDE Discover | 200+ MB | ❌ (仅 KDE) | ❌ | ❌ |
| Synaptic | 50-80 MB | ❌ (仅 Debian) | ✅ | ❌ |
| 命令行 | 5 MB | ✅ | ✅ | ✅ |

## 🤝 参与贡献

欢迎提交贡献、Bug 报告和建议！

1. Fork 本项目
2. 创建您的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交您的更改 (`git commit -m '添加某个特性'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

### 计划中的功能

- 软件包详情页（依赖、大小、描述）
- 批量卸载
- 图形化仓库编辑器
- 更多语言支持（日语、西班牙语等）
- 深色主题
```
