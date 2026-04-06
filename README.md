# Topic 10 作业分享报告 - Quarto Book

这是 Topic 10 作业的分享报告，使用 Quarto Book 编写，可以通过 GitHub Pages 发布。

## 报告结构

```
├── _quarto.yml          # Quarto 配置文件
├── index.qmd            # 首页
├── 01-analysis.qmd      # 第一章：分析过程和主要结论
├── 02-sqlite.qmd        # 第二章：SQLite 技术介绍
├── 03-ai-assistance.qmd # 第三章：AI 协助过程
├── references.qmd        # 参考资料
├── references.bib        # BibTeX 参考文献
└── README.md             # 本文件
```

## 本地预览

### 前置要求

1. 安装 Quarto: [https://quarto.org/docs/get-started/](https://quarto.org/docs/get-started/)

### 预览书籍

在项目目录下运行：

```bash
quarto preview
```

这会在浏览器中打开一个实时预览页面，当你修改 .qmd 文件时，页面会自动刷新。

### 构建书籍

```bash
quarto render
```

这会在 `_book` 目录下生成完整的 HTML 网站。

## 发布到 GitHub Pages

### 方法一：使用 `quarto publish`（推荐）

在项目目录下运行：

```bash
quarto publish gh-pages
```

这会：
1. 自动构建书籍
2. 创建/更新 `gh-pages` 分支
3. 推送到 GitHub
4. 启用 GitHub Pages

### 方法二：手动设置

1. 构建书籍：
   ```bash
   quarto render
   ```

2. 将 `_book` 目录的内容推送到 `gh-pages` 分支，或者使用 GitHub Actions 自动部署。

3. 在 GitHub 仓库的 Settings -> Pages 中：
   - Source: Deploy from a branch
   - Branch: gh-pages, / (root)
   - 点击 Save

## 分享链接

发布成功后，你的报告可以通过以下链接访问：

```
https://<你的用户名>.github.io/<仓库名>/
```

## 15 分钟汇报时间分配建议

| 章节 | 时间 |
|------|------|
| 开场介绍 | 1 分钟 |
| 第一章：分析过程和主要结论 | 6 分钟 |
| 第二章：SQLite 技术介绍 | 4 分钟 |
| 第三章：AI 协助过程 | 3 分钟 |
| 总结与 Q&A | 1 分钟 |
| **总计** | **15 分钟** |

## 自定义修改

- 修改 `_quarto.yml` 可以调整书籍标题、主题、格式等
- 修改各个 `.qmd` 文件来更新内容
- 可以在 `references.bib` 中添加更多参考文献

## 更多 Quarto 资源

- [Quarto 官方文档](https://quarto.org/docs/)
- [Quarto Book 指南](https://quarto.org/docs/books/)
- [Quarto GitHub Pages 发布](https://quarto.org/docs/publishing/github-pages.html)
