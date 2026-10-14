<div align="center">

# Lucky to Know · 性知

**一款面向青少年与家长的性知识教育 Android 应用**
*A sex-education Android app for teenagers and parents*

[![Platform](https://img.shields.io/badge/Platform-Android-green.svg)](https://www.android.com/)
[![Language](https://img.shields.io/badge/Language-Java-orange.svg)](https://www.java.com/)
[![Gradle](https://img.shields.io/badge/Gradle-7.2.1-blue.svg)](https://gradle.org/)
[![minSdk](https://img.shields.io/badge/minSdk-21-brightgreen.svg)](https://developer.android.com/)
[![License](https://img.shields.io/badge/License-Educational-lightgrey.svg)](#免责声明disclaimer)

[中文](#中文说明--chinese) · [English](#english-version)

</div>

---

## 中文说明 / Chinese

### 项目简介

**Lucky to Know（中文名：性知，代号 XZ）** 是一个本科阶段完成的安卓应用项目。
应用以「普及科学性知识教育」为目标，面向青少年及其家长，提供系统化的性教育内容、互动问答、书籍推荐与经验分享社区，希望用更轻松、更易接受的方式去回答那些「不好意思开口问」的问题。

### 背景与目标

- 传统性教育内容分散、缺乏体系，青少年难以获得科学、适龄的引导。
- 家长与孩子之间往往羞于沟通相关话题。
- 性知希望做一层「内容分层 + 场景引导」的教育桥梁：既让青少年自己学，也让家长能陪伴孩子一起学。

### 功能特性

| 模块 | 说明 |
| --- | --- |
| 引导与分层 | 首次启动选择「自己学 / 给孩子学」，并按性别、年龄段（10 后 / 00 后 / 90 后 / 80 后 / 70 后 / 其他）推荐合适内容 |
| 首页 | 轮播 Banner、书城 / 动态 / 竞赛 / 学堂 四大入口、热门话题榜单 |
| 发布 | 编辑并发布个人动态，分享新鲜事 |
| 消息 | 与「性性」「医生」「奇奇」「乐乐」等虚拟角色对话式交流，支持搜索与未读提醒 |
| 幸知书城 | 性教育相关书籍展示、好书推荐与书籍搜索 |
| 个人中心 | 个人主页（动态 / 关注 / 粉丝）、历史记录、我的收藏、草稿箱、我的课程、我的测试 |
| 常用工具 | 健康咨询、知识库、话题广场 |
| 动态广场 | 关注 / 发现 / 官方 三个频道，支持跳转视频与动态详情 |
| 测试 | 提供简单 / 中等 / 困难三个难度层级的自测内容 |

### 应用流程

```
启动海报 (MainActivity)
        │
        ▼
选择学习对象 (gyxselect1) —— 自己学 / 给孩子学
        │
        ▼
选择性别与年龄层 (gyxselect2)
        │
        ▼
登录 (gyxlogin)
        │
        ▼
主界面 (BaseActivity)：首页 · 发布 · 消息 · 书店 · 个人
```

### 技术栈

- **语言**：Java 8
- **平台**：Android（`compileSdk 32` / `targetSdk 32` / `minSdk 21`）
- **构建**：Gradle 7.2.1 + Android Gradle Plugin 7.2.1
- **UI**：TabLayout + ViewPager2 + Fragment 底部导航、Material Components、ConstraintLayout
- **架构**：AndroidX、ViewModel / LiveData（`lifecycle-viewmodel-ktx`、`lifecycle-livedata-ktx`）
- **包名**：`com.example.xz`

### 项目结构

```
Lucky-to-Know/
├── app/
│   └── src/main/
│       ├── java/com/example/xz/
│       │   ├── MainActivity.java            # 启动海报页
│       │   ├── gyxselect1.java              # 学习对象选择
│       │   ├── gyxselect2.java              # 性别 / 年龄层选择
│       │   ├── gyxlogin.java                # 登录
│       │   ├── BaseActivity.java            # 主容器（TabLayout + ViewPager2）
│       │   ├── one/   → 首页 FoneFragment、动态 DynamicsActivity
│       │   ├── two/   → 发布 FtwoFragment
│       │   ├── three/ → 消息 FthreeFragment、Dialogue、Search
│       │   ├── four/  → 书店 FfourthFragment
│       │   ├── five/  → 个人 FfirthFragment
│       │   └── Adapters/                    # ViewPager2 适配器
│       ├── res/layout/                      # 各页面布局
│       ├── res/drawable-*/                  # 图标与 Banner 资源
│       └── AndroidManifest.xml
├── build.gradle
├── settings.gradle
└── gradlew / gradlew.bat
```

### 环境要求与构建

- Android Studio（Arctic Fox 及以上）
- JDK 11 / 17
- Android SDK（Platform 32、Build-Tools）

```bash
# 克隆仓库
git clone https://github.com/sansuiyi/Lucky-to-Know-.git

# 命令行构建 Debug 包
./gradlew assembleDebug

# 安装到已连接的设备 / 模拟器
./gradlew installDebug
```

也可直接用 Android Studio 打开根目录，等待 Gradle Sync 完成后点击 Run。

### 贡献者

本项目为多人协作的本科课程 / 竞赛项目，主要提交者包括：
`GYX505`、`Dwp`、`huadongxiaolin`、`Lfy5`、`Chenn099`。

### 免责声明 / Disclaimer

- 本项目仅用于**教学、学习与课程展示**目的。
- 应用内涉及的性教育内容仅供科普参考，**不能替代专业医生或心理咨询师的诊断与建议**。
- 若身体或心理出现不适，请及时就医或寻求专业帮助。

---

## English Version

### Introduction

**Lucky to Know** (Chinese name: *性知*, code name *XZ*) is an Android application developed as an undergraduate project.
Aimed at popularizing accurate sex education, it serves teenagers and their parents with structured educational content, interactive conversations, book recommendations, and a sharing community — trying to answer the questions people are often too embarrassed to ask.

### Background & Goals

- Traditional sex-education resources are scattered and unsystematic, making it hard for teenagers to find scientific, age-appropriate guidance.
- Parents and children often feel awkward discussing these topics.
- Lucky to Know acts as a bridge with *tiered content + scenario-based guidance*: so teenagers can learn on their own, and parents can learn alongside their children.

### Features

| Module | Description |
| --- | --- |
| Onboarding & Tiering | On first launch, choose "Learn for myself / Learn for my child", then pick gender and age group (Gen-10s / 00s / 90s / 80s / 70s / other) to get tailored content |
| Home | Carousel banners, four entry points (Bookstore / Moments / Competition / Academy), and a trending-topics board |
| Publish | Compose and post personal moments to share updates |
| Messages | Chat-style interaction with characters such as "性性" "医生" "奇奇" "乐乐", with search and unread reminders |
| Bookstore | Sex-education book showcase, curated recommendations, and book search |
| Profile | Personal page (Moments / Following / Followers), history, favorites, drafts, my courses, my quizzes |
| Tools | Health consultation, knowledge base, topic square |
| Moments Feed | "Following / Discover / Official" channels, with links to videos and detail pages |
| Quizzes | Self-assessment content at three difficulty levels: Easy / Medium / Hard |

### App Flow

```
Poster (MainActivity)
        │
        ▼
Choose audience (gyxselect1) —— for myself / for my child
        │
        ▼
Choose gender & age group (gyxselect2)
        │
        ▼
Login (gyxlogin)
        │
        ▼
Main screen (BaseActivity): Home · Publish · Messages · Bookstore · Profile
```

### Tech Stack

- **Language**: Java 8
- **Platform**: Android (`compileSdk 32` / `targetSdk 32` / `minSdk 21`)
- **Build**: Gradle 7.2.1 + Android Gradle Plugin 7.2.1
- **UI**: TabLayout + ViewPager2 + Fragment bottom navigation, Material Components, ConstraintLayout
- **Architecture**: AndroidX, ViewModel / LiveData (`lifecycle-viewmodel-ktx`, `lifecycle-livedata-ktx`)
- **Package**: `com.example.xz`

### Project Structure

```
Lucky-to-Know/
├── app/
│   └── src/main/
│       ├── java/com/example/xz/
│       │   ├── MainActivity.java            # Poster / splash page
│       │   ├── gyxselect1.java              # Choose learning audience
│       │   ├── gyxselect2.java              # Choose gender / age group
│       │   ├── gyxlogin.java                # Login
│       │   ├── BaseActivity.java            # Main container (TabLayout + ViewPager2)
│       │   ├── one/   → Home FoneFragment, Moments DynamicsActivity
│       │   ├── two/   → Publish FtwoFragment
│       │   ├── three/ → Messages FthreeFragment, Dialogue, Search
│       │   ├── four/  → Bookstore FfourthFragment
│       │   ├── five/  → Profile FfirthFragment
│       │   └── Adapters/                    # ViewPager2 adapter
│       ├── res/layout/                      # Layouts for each screen
│       ├── res/drawable-*/                  # Icons and banner assets
│       └── AndroidManifest.xml
├── build.gradle
├── settings.gradle
└── gradlew / gradlew.bat
```

### Requirements & Build

- Android Studio (Arctic Fox or later)
- JDK 11 / 17
- Android SDK (Platform 32, Build-Tools)

```bash
# Clone the repository
git clone https://github.com/sansuiyi/Lucky-to-Know-.git

# Build a debug APK from the command line
./gradlew assembleDebug

# Install to a connected device / emulator
./gradlew installDebug
```

You can also open the project root in Android Studio, wait for Gradle Sync, then click Run.

### Contributors

This is a collaborative undergraduate course / competition project. Main contributors include:
`GYX505`, `Dwp`, `huadongxiaolin`, `Lfy5`, `Chenn099`.

### Disclaimer

- This project is intended for **teaching, learning, and coursework presentation** only.
- The sex-education content provided is for general informational purposes and **is not a substitute for professional medical or psychological advice**.
- If you experience physical or mental discomfort, please seek medical attention or professional help promptly.
