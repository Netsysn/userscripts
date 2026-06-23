# Netsysn 用户脚本

## 脚本列表

- **chaoxing.user.js** — 超星学习通｜智慧树网课助手

## 安装

在 ScriptCat 中打开以下地址即可安装：

```
https://cdn.jsdelivr.net/gh/Netsysn/userscripts/chaoxing.user.js
```

## 来源说明

本脚本为二次开发，基于 **OCS 网课助手（ocsjs）** 生态：

- 原始项目：[ocsjs/ocsjs](https://github.com/ocsjs/ocsjs) — OCS 网课助手
- 上游 Fork：`noshuang` → `isMobile`
- 本 Fork：**Netsysn** — 针对自建题库 API 和 Linux 服务器运维场景定制

## 本 Fork 修改内容

| 修改 | 说明 |
|------|------|
| 题库 API | 默认指向自建题库 `netsysn.cn`，替代公开题库 |
| 默认关闭 | 所有功能默认关闭（自动提交、自动下一章、自动切换、自动检测），用户按需开启 |
| 移除 IP | 去除第三方 IP `43.139.242.144` 引用 |
| 移动端拖拽 | 新增触摸事件支持，手机/平板可拖拽面板 |
| CDN 分发 | 通过 jsDelivr CDN 分发，绕过 Cloudflare 安全检查 |

## 更新

```bash
cd ~/userscripts
# 修改 chaoxing.user.js 后
git add chaoxing.user.js
git commit -m "更新脚本"
git push
```

jsDelivr 会在几分钟内自动同步最新版本。
