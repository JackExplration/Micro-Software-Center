```
# Micro Software Center - Lightweight Cross-Distro Package Manager GUI

[![License](https://img.shields.io/badge/License-GPLv3-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Linux-lightgrey.svg)]()
[![Memory](https://img.shields.io/badge/memory-5--10MB-brightgreen.svg)]()

> **Why this project exists?**
> 
> I wanted a lightweight software center. GNOME Software takes 300+ MB, KDE Discover also heavy.  
> When using lightweight desktops like Openbox, i3, or XFCE, I wanted a graphical package manager but couldn't find one.  
> So I built it myself.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🪶 **Ultra Lightweight** | Only 5-10 MB memory usage |
| 🐧 **Cross-Distro** | Fedora, RHEL, CentOS, Rocky, Alma, Debian, Ubuntu, Arch, openSUSE |
| 📦 **Package Management** | Install, remove, search, update packages |
| 🗂️ **Repository Manager** | Enable/disable/add/remove repositories |
| ⚙️ **One-Click Third-Party Repos** | RPM Fusion, EPEL, Google Chrome, VS Code, Docker, Brave, VirtualBox, Steam, Slack, Spotify |
| 🎯 **Flatpak Support** | Install apps from Flathub |
| 🌍 **Multi-Language** | English / 简体中文 |

## 🚀 Quick Install

### Method 1: One-click Install

```bash
git clone https://github.com/yourusername/micro-software-center.git
cd micro-software-center
./install.sh
```

### Method 2: Manual Install

```bash
# 1. Install dependencies
# Fedora/RHEL
sudo dnf install yad bc

# Debian/Ubuntu
sudo apt install yad bc

# Arch Linux
sudo pacman -S yad bc

# openSUSE
sudo zypper install yad bc

# 2. Clone the project
git clone https://github.com/yourusername/micro-software-center.git
cd micro-software-center

# 3. Run (no installation required)
./micro-software-center

# Or install to system
./install.sh
```

## 🎯 Usage

Launch the Software Center:

```bash
micro-software-center
```

Or find Micro Software Center in your application menu.

### Keyboard Shortcuts (within the app)

| Shortcut | Function |
|----------|----------|
| Ctrl+F | Search software |
| Ctrl+Q | Quit |
| F5 | Refresh list |

## 🔧 Development Story

### Why I Built This

In early 2025, I set up an Openbox lightweight desktop with memory usage of 40-60 MB.
Everything was perfect until I wanted to install software — I had to use the command line `dnf install`.

I tried GNOME Software: it ate 300+ MB of RAM, more than my entire desktop.
KDE Discover was the same.
Do lightweight desktop users have to live with the command line?

So I started this project.
Goal: 5-10 MB memory, graphical interface, support for mainstream distributions.

### Development Journey

- **Choosing GUI Tool**: YAD — lightweight, minimal dependencies, powerful enough
- **Cross-Distro Support**: Detect `/etc/*-release`, implement dnf/apt/pacman/zypper commands
- **Repository Management**: Parse `/etc/yum.repos.d/`, enable/disable/add/remove
- **One-Click Third-Party Repos**: RPM Fusion, EPEL, Google Chrome, VS Code, and more
- **Flatpak Support**: Integrate flatpak commands
- **Multi-Language**: Extract language files, support English and Chinese

### Current Status

- **Memory Usage**: 5-10 MB
- **Lines of Code**: ~1500
- **Supported Distros**: Fedora, RHEL, CentOS, Rocky, Alma, Oracle, Amazon, Debian, Ubuntu, Arch, openSUSE
- **Supported Features**: Package management, repo management, third-party repos, Flatpak

## 📊 Comparison with Other Software Centers

| Software Center | Memory Usage | Cross-Distro | Repo Manager | Lightweight Optimized |
|-----------------|--------------|--------------|--------------|----------------------|
| Micro Software Center | 5-10 MB | ✅ | ✅ | ✅ |
| GNOME Software | 300+ MB | ❌ (GNOME only) | ❌ | ❌ |
| KDE Discover | 200+ MB | ❌ (KDE only) | ❌ | ❌ |
| Synaptic | 50-80 MB | ❌ (Debian only) | ✅ | ❌ |
| Command Line | 5 MB | ✅ | ✅ | ✅ |

## 🤝 Contributing

Contributions, bug reports, and suggestions are welcome!

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Planned Features

- Package details page (dependencies, size, description)
- Batch uninstall
- Graphical repository editor
- More language support (Japanese, Spanish, etc.)
- Dark theme
```
