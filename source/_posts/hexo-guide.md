---
title: hexo guide
date: 2026-03-12 22:50:50
tags: 
  - Hexo
categories: 
  - 随笔
---

# Hexo 常用命令手册

## 1. 核心流程命令 (The Big Four)

| 命令 | 简写 | 描述 |
| :--- | :--- | :--- |
| `hexo clean` | 无 | **清除缓存**：删除 `db.json` 和 `public` 文件夹。建议在生成或部署前执行。 |
| `hexo generate` | `hexo g` | **生成静态文件**：将 Markdown 源码转化为 HTML 页面，保存在 `public` 文件夹。 |
| `hexo server` | `hexo s` | **本地预览**：启动本地服务器（默认端口 4000），用于推送到线上前查看效果。 |
| `hexo deploy` | `hexo d` | **部署**：将生成的静态文件推送到配置好的远程仓库分支（如 `gh-pages`）。 |

## 2. 内容创作命令

- **新建文章**
  ```bash
  hexo new post "文章标题"

- **新建页面**
  ```bash
  hexo new page "about"   # 创建“关于我”之类的独立页面

- **草稿功能**
  ```bash
  hexo new draft "草稿名" # 文件会放在 source/_drafts/，默认预览不可见
  hexo publish "草稿名"   # 将草稿移动到 _posts 文件夹，正式发布

## 3. 配置与信息查看

- **查看版本**
  ```bash
  hexo version  # 检查 Hexo 环境及其插件版本

- **列出所有路由**
  ```bash
  hexo list post    # 查看所有文章的状态（发布、草稿等）
  hexo list route   # 查看生成的页面路径（排查 404 很有用）

## 3. 配置与信息查看

- **-p(Port):** 修改本地预览端口。如果 4000 被占用，可用 hexo s -p 5000。
- **-d (Deploy):** 生成后立即部署。hexo g -d 是效率最高的方式。
- **--debug:** 开启调试模式。如果命令报错，加上这个参数可以看到详细的错误堆栈信息。