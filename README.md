# 立创开源硬件平台 (LCSC OSHW Hub)

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Android](https://img.shields.io/badge/Android-5.0%2B-brightgreen.svg)]()
[![Language](https://img.shields.io/badge/Language-Java-orange.svg)]()

> 一个极简的立创开源硬件平台 (OSHWHub) 第三方客户端 App，纯原生 Android，零外部依赖。

## 简介

本项目是立创开源硬件平台 ([oshwhub.com](https://oshwhub.com/)) 的非官方第三方客户端，采用纯原生 Android 技术栈开发，代码极简，适合作为 WebView 封装 App 的入门示例。

## 特性

- ✅ **纯原生 Android** - 零 AndroidX、零 AppCompat、零 Material 依赖
- ✅ **极简代码** - 仅 2 个 Activity，代码量极少
- ✅ **启动页** - 3 秒启动页，显示品牌信息
- ✅ **深色主题** - 全局暗色风格
- ✅ **立创官方图标** - 使用 OSHWHub 官方 Logo
- ✅ **返回键支持** - WebView 内页面可返回

## 截图

| 启动页 | 主页 |
|--------|------|
| 欢迎使用立创开源硬件平台 | OSHWHub 网页 |

## 技术栈

| 技术 | 说明 |
|------|------|
| 语言 | Java |
| 最低 SDK | API 21 (Android 5.0) |
| 目标 SDK | API 34 (Android 14) |
| 构建工具 | Gradle |
| 依赖 | 无 |

## 项目结构

```
app/src/main/
├── AndroidManifest.xml
├── assets/
│   └── index.html          # 网页跳转入口
├── java/com/lcsc/oshw/
│   ├── SplashActivity.java # 启动页 (3秒)
│   └── MainActivity.java   # WebView 主页面
└── res/
    ├── layout/
    │   ├── activity_splash.xml
    │   └── activity_main.xml
    ├── mipmap-*/           # 应用图标
    └── values/
        ├── colors.xml
        ├── strings.xml
        └── themes.xml
```

## 构建

### 使用 Android Studio
1. 克隆仓库
2. 用 Android Studio 打开项目
3. 点击 Run

### 使用命令行
```bash
./gradlew assembleDebug
```

APK 输出路径：`app/build/outputs/apk/debug/app-debug.apk`

## 自定义

### 修改跳转网址
编辑 `app/src/main/assets/index.html`：
```html
<meta http-equiv="refresh" content="0;url=https://oshwhub.com/">
```

### 修改启动页文字
编辑 `app/src/main/res/layout/activity_splash.xml`

### 修改应用名称
编辑 `app/src/main/res/values/strings.xml`

## 复刻信息

- **原作者**: 刘文轩的3D打印
- **项目灵感**: 立创商城 App 复刻

## 免责声明

本项目为个人学习作品，与立创商城、OSHWHub 官方无关。所有商标和 Logo 归其 respective 所有者。

## License

[MIT](LICENSE) © 刘文轩的3D打印
