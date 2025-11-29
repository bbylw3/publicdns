# 🌐 公共 DNS 大全 (Public DNS Hub) - VS Code Theme

一个轻量级、无需后端、单文件运行的公共 DNS 聚合查询工具。采用了程序员最熟悉的 Visual Studio Code 暗黑主题设计语言，提供极客般的浏览体验。

## 目录

- [🌐 公共 DNS 大全 (Public DNS Hub) - VS Code Theme](#-公共-dns-大全-public-dns-hub---vs-code-theme)
  - [目录](#目录)
  - [✨ 特性 (Features)](#-特性-features)
  - [🚀 快速开始 (Quick Start)](#-快速开始-quick-start)
  - [🛠 技术栈 (Tech Stack)](#-技术栈-tech-stack)
  - [📦 收录的 DNS 服务商](#-收录的-dns-服务商)
    - [🇨🇳 国内优化 (Domestic)](#-国内优化-domestic)
    - [🌍 国际畅通 (International)](#-国际畅通-international)
    - [🛡 安全与隐私 (Security)](#-安全与隐私-security)
  - [🤝 贡献 (Contributing)](#-贡献-contributing)
  - [📄 免责声明](#-免责声明)

## ✨ 特性 (Features)

- 🎨 VS Code 风格 UI：深度复刻 VS Code 界面，包括配色、侧边栏、状态栏及语法高亮风格的卡片设计。
- ⚡️ 单文件运行：所有逻辑（React、Babel、Tailwind）均通过 CDN 引入，无需 npm install 或构建，下载 HTML 即可直接运行。
- 🔍 实时搜索与过滤：
  - 支持按服务商名称或描述搜索（类 Command Palette 体验）。
  - 支持按类别筛选：国内加速、国际畅通、安全防护、IPv6 支持。
- 📋 一键复制：点击 IP 地址（IPv4 或 IPv6）即可自动复制到剪贴板。
- 📖 内置教程：包含 Windows, macOS, iOS, Android 的 DNS 修改详细教程（Markdown 渲染风格）。
- 📱 响应式设计：完美适配桌面端和移动端访问。

## 🚀 快速开始 (Quick Start)

由于本项目是单文件架构（Single File Component），部署非常简单：

- 下载：下载本项目中的 `public_dns_hub.html` 文件。
- 运行：直接双击文件，使用任意现代浏览器（Chrome, Edge, Firefox, Safari）打开。
- 完成：即可开始使用。

## 🛠 技术栈 (Tech Stack)

本项目完全基于浏览器端渲染，未使用任何构建工具（如 Webpack/Vite），方便修改和集成。

- 核心框架: React 18 (UMD version)
- 样式库: Tailwind CSS (CDN script)
- 图标库: Lucide React
- 编译器: Babel Standalone (用于浏览器端编译 JSX)

## 📦 收录的 DNS 服务商

目前收录了国内外主流、稳定且免费的公共 DNS 服务：

### 🇨🇳 国内优化 (Domestic)

- AliDNS (阿里): 223.5.5.5 / 223.6.6.6
- DNSPod (腾讯): 119.29.29.29 / 182.254.116.116
- 114 DNS: 114.114.114.114
- CNNIC SDNS (国家队): 1.2.4.8
- 百度 DNS: 180.76.76.76
- 火山引擎 (字节跳动): 180.184.1.1
- OneDNS: 117.50.11.11

### 🌍 国际畅通 (International)

- Google Public DNS: 8.8.8.8 / 8.8.4.4
- Cloudflare: 1.1.1.1 / 1.0.0.1
- OpenDNS: 208.67.222.222

### 🛡 安全与隐私 (Security)

- 360 安全 DNS: 101.226.4.6
- AdGuard DNS: 94.140.14.14 (去广告)
- Quad9: 9.9.9.9 (恶意域名拦截)

## 🤝 贡献 (Contributing)

如果您发现有更好用的公共 DNS，或者现有信息有误，可以通过修改 html 文件中的 dnsData 数组来提交更改。

数据结构示例：

```json
{
    "id": 99,
    "name": "New DNS",
    "provider": "Provider Name",
    "tags": ["Tag1", "Tag2"],
    "category": "domestic", // domestic, international, or security
    "ipv4_1": "1.2.3.4",
    "ipv4_2": "5.6.7.8",
    "ipv6_1": "2001::1", // 可选
    "ipv6_2": null,      // 可选
    "desc": "描述信息..."
}
```

## 📄 免责声明

本项目仅作为公共 DNS 信息的聚合展示，所列出的 DNS 服务由各自的运营商提供。本项目不保证服务的可用性、速度或安全性，请根据您的网络环境自行测试选择。

Happy Hacking! 💻
