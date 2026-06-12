# 把 Dashboard 放到飞书里给别人在线看

飞书文档不能直接托管这个本地网页。要让师兄点链接就能看，需要先把本文件夹发布成一个公网静态网站，再把网址粘到飞书文档。

## 当前可部署内容

请部署这个文件夹的全部内容：

```text
volleyball-pattern-dashboard-feishu-site/
```

核心文件包括：

```text
index.html
assets/bundle.js
assets/styles.css
volleyball_english_cross_table_v5_renamed_context.xlsx
```

## 方案 A：GitHub Pages

1. 在 GitHub 新建一个仓库，例如 `volleyball-pattern-dashboard`。
2. 把本文件夹里的所有文件上传到仓库根目录。
3. 进入仓库 `Settings > Pages`。
4. `Build and deployment` 选择 `Deploy from a branch`。
5. `Branch` 选择 `main` 和 `/root`，保存。
6. 等 1 到 3 分钟，GitHub 会生成一个 `https://用户名.github.io/仓库名/` 链接。
7. 把这个链接粘到飞书文档里。

如果用命令行推送：

```bash
cd volleyball-pattern-dashboard-feishu-site
git init
git add .
git commit -m "Deploy volleyball dashboard"
git branch -M main
git remote add origin https://github.com/你的用户名/volleyball-pattern-dashboard.git
git push -u origin main
```

然后回到 GitHub 页面开启 Pages。

## 方案 B：Netlify Drop

1. 打开 Netlify Drop。
2. 直接拖入整个 `volleyball-pattern-dashboard-feishu-site` 文件夹。
3. 等它生成网址。
4. 把网址粘到飞书文档里。

## 方案 C：Vercel

1. 在 Vercel 新建项目。
2. 选择导入 GitHub 仓库，或上传这个静态站点目录。
3. Framework 选择 `Other` 或保持默认。
4. Build Command 留空。
5. Output Directory 使用当前目录或留空。
6. 部署完成后，把 Vercel URL 粘到飞书文档里。

## 本地预览

双击：

```text
serve_static.cmd
```

然后浏览器打开：

```text
http://127.0.0.1:4173/
```

注意：这个本地地址只能你自己的电脑访问，不能直接发给师兄。
