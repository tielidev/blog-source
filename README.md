# Readme file

# main source branch: main

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