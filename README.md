# Aspartame 的博客（Quarto + GitHub Pages）

这是一个基于 Quarto Website 的个人博客仓库，部署目标为 GitHub Pages：
- 仓库：`aspartame4990/aspartame4990.github.io`
- 站点地址：`https://aspartame4990.github.io`
- 渲染输出目录：`docs/`

## 项目用途

用于发布个人技术博客，支持：
- Markdown/Quarto 写作
- 文章列表自动聚合
- LaTeX 数学公式（KaTeX）
- Giscus 评论（已预留最小配置）

## 本地预览

```bash
quarto preview
```

执行后会启动本地预览服务，编辑文件后会自动刷新。

## 本地渲染

```bash
quarto render
```

渲染产物会输出到 `docs/` 目录，该目录需要提交到仓库。

## 推送到 GitHub

```bash
git add .
git commit -m "Update blog content"
git push origin main
```

## GitHub Pages 设置（main 分支 /docs）

1. 打开 GitHub 仓库页面 `Settings`。
2. 进入 `Pages`。
3. 在 `Build and deployment` 中选择 `Deploy from a branch`。
4. 选择分支 `main`，目录选择 `/docs`。
5. 保存后等待部署完成。

## 启用 Giscus 评论

Giscus 生效前需要完成以下步骤：

1. 仓库必须是公开仓库（Public）。
2. 在仓库 `Settings` 中开启 `Discussions`。
3. 安装 Giscus GitHub App，并授权到本仓库。
4. 在 Giscus 配置页面选择仓库和 Discussions 分类，补充 `_quarto.yml` 中需要的 `category` / `category-id` 等参数（当前仓库已保留最小可用配置）。

## 如何替换个人信息和站点标题

1. 修改 `_quarto.yml`：
   - `website.title`（站点标题）
   - `website.site-url`（站点 URL）
2. 修改 `about.qmd`：
   - 个人介绍占位内容
   - 联系方式
   - GitHub 链接
3. 在 `posts/` 目录新增文章（`.qmd` 文件）并重新运行 `quarto render`。
