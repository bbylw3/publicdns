# 🌐 公共 DNS 大全 (Public DNS Hub) - VS Code Theme

一个轻量级、无需后端、单文件运行的公共 DNS 聚合查询工具。采用了深度还原的 Visual Studio Code 暗黑主题设计语言，为开发者提供极客般的浏览体验。

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

- **🎨 极致 VS Code 还原**：
    - **Activity Bar**: 侧边栏模拟了 VS Code 的活动栏（文件、搜索、Git 等图标）。
    - **Status Bar**: 底部状态栏动态显示项目统计（如 DNS 数量作为“行号”），支持 Git 分支模拟。
    - **Editor Style**: 卡片采用代码编辑器风格，带有行号和语法高亮 (`const info = { ... }`)。
- **⚡️ 极致性能与体验**：
    - **平滑启动**: 内置 CSS Loading 动画，消除 React 浏览器端编译时的白屏闪烁。
    - **智能搜索**: 支持 Command Palette 风格搜索，关键词在标题和描述中自动**高亮显示**。
    - **单文件架构**: 所有逻辑（React、Babel、Tailwind）均通过 CDN 引入，下载 `index.html` 即可运行。
- **📋 交互细节**：
    - **一键复制**: 点击 IP 地址自动复制，图标会有✅ 状态反馈。
    - **响应式设计**: 完美适配移动端（Mobile）和桌面端（Desktop），移动端自动隐藏侧边栏。
- **📖 内置教程**: 包含 Windows, macOS, iOS, Android 的 DNS 修改详细教程（Markdown 渲染风格）。

## 🚀 快速开始 (Quick Start)

由于本项目是 **Zero-Build** 架构，部署非常简单：

1.  **下载**：下载本项目中的 `index.html` 文件。
2.  **运行**：直接双击文件，使用任意现代浏览器（Chrome, Edge, Firefox, Safari）打开。
3.  **完成**：即可开始使用，无需 `npm install` 或 `npm run build`。

## 🛠 技术栈 (Tech Stack)

本项目完全基于浏览器端渲染 (Client-side Rendering)，未使用任何构建工具，方便修改和集成。

- **Core**: React 18 (UMD version)
- **UI/Styles**: Tailwind CSS (CDN) + Custom CSS (Scrollbars, Syntax Highlighting)
- **Icons**: Lucide React
- **Compiler**: Babel Standalone (用于浏览器端实时编译 JSX)

## 📦 收录的 DNS 服务商

目前收录了国内外主流、稳定且免费的公共 DNS 服务：

### 🇨🇳 国内优化 (Domestic)

- **AliDNS (阿里)**: 223.5.5.5 / 223.6.6.6
- **DNSPod (腾讯)**: 119.29.29.29 / 182.254.116.116
- **114 DNS**: 114.114.114.114
- **CNNIC SDNS (国家队)**: 1.2.4.8
- **百度 DNS**: 180.76.76.76
- **火山引擎 (字节跳动)**: 180.184.1.1
- **OneDNS**: 117.50.11.11

### 🌍 国际畅通 (International)

- **Google Public DNS**: 8.8.8.8 / 8.8.4.4
- **Cloudflare**: 1.1.1.1 / 1.0.0.1
- **OpenDNS**: 208.67.222.222

### 🛡 安全与隐私 (Security)

- **360 安全 DNS**: 101.226.4.6
- **AdGuard DNS**: 94.140.14.14 (去广告)
- **Quad9**: 9.9.9.9 (恶意域名拦截)

## 🤝 贡献 (Contributing)

如果您发现有更好用的公共 DNS，或者现有信息有误，您可以直接修改 `index.html` 文件。

1.  打开 `index.html`。
2.  搜索 `const DNS_DATA`。
3.  按照以下 JSON 格式添加新的对象：

```javascript
{
    id: 99,
    name: "New DNS",
    provider: "Provider Name",
    tags: ["Tag1", "Tag2"],
    category: "domestic", // 'domestic' | 'international' | 'security'
    ipv4_1: "1.2.3.4",
    ipv4_2: "5.6.7.8",
    ipv6_1: "2001::1", // 可选
    ipv6_2: null,      // 可选
    desc: "描述信息..."
}
```

## 📄 免责声明

本项目仅作为公共 DNS 信息的聚合展示，所列出的 DNS 服务由各自的运营商提供。本项目不保证服务的可用性、速度或安全性，请根据您的网络环境自行测试选择。

Happy Hacking! 💻