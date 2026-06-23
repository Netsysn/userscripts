# Netsysn 用户脚本

## 脚本列表

- **chaoxing.user.js** — 超星学习通｜智慧树网课助手

## 安装

在 ScriptCat 中打开以下地址即可安装：

```
https://cdn.jsdelivr.net/gh/Netsysn/userscripts/chaoxing.user.js
```

## 来源说明

本脚本为**二次开发**，而非原封不动转载，基于 **OCS 网课助手（ocsjs）** 生态：

- 原始项目：[ocsjs/ocsjs](https://github.com/ocsjs/ocsjs) — OCS 网课助手
- 上游 Fork：`noshuang` → `isMobile`
- 本 Fork：**Netsysn** — 自建题库驱动 + Linux 运维部署 + CDN 分发

## 相比于原始 OCS 的所有新增/修改

### isMobile 阶段新增

| 功能 | 说明 |
|------|------|
| 🎬 视频倍速 | 支持自定义倍速播放，可开关 |
| 🔍 自动检测答题 | 可开关的自动检测题目并作答 |
| 🎯 题目选项不匹配修复 | 修复题目选项与题库答案不匹配时无法正常作答的问题 |
| 🚨 严格模式 | 「不确定则跳过」——减少错误答案提交风险 |
| ⏭️ 跳过已答题目 | 遇到已作答的题目自动跳过，避免重复提交 |
| 🗄️ 自建题库 API | 题库指向自建服务端 `netsysn.cn`，非公开题库 |
| 📊 配额系统 | 服务端配额管理，支持 API Key 生成与用量控制 |

### Netsysn 阶段新增

| 功能 | 说明 |
|------|------|
| 🔒 默认全部关闭 | 所有自动化功能默认 `false`，用户按需开启，避免误操作 |
| 🧹 移除第三方 IP | 清除 `43.139.242.144` 引用，全部指向自建服务 |
| 📱 移动端拖拽 | 新增 `touchstart/touchmove/touchend`，手机/平板可拖拽设置面板 |
| 🌐 CDN 分发 | 通过 jsDelivr 全球 CDN 分发脚本，绕过 Cloudflare 安全检查 |
| 🐳 基础设施 | Cloudflare Tunnel 零端口暴露 + systemd 服务化 + Nginx 反代 |

## 更新

```bash
cd ~/userscripts
# 修改 chaoxing.user.js 后
git add chaoxing.user.js
git commit -m "更新脚本"
git push
```

jsDelivr 会在几分钟内自动同步最新版本。
