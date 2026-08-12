# Yi Hong (洪逸) — Personal Homepage

个人学术主页，风格参考 [acad-homepage](https://github.com/RayeRen/acad-homepage.github.io)。
纯静态站点（HTML + CSS），无需构建，可直接部署到 GitHub Pages。

## 本地预览

直接用浏览器打开 `index.html`，或起一个本地服务器：

```bash
python3 -m http.server 8000
# 打开 http://localhost:8000
```

## 部署到 GitHub Pages

1. 新建仓库 `Yi-Eaaa.github.io`（用户主页仓库）。
2. 把本目录内容推上去：

   ```bash
   cd /Users/bytedance/workspace/YiHong-HomePage
   git init
   git add .
   git commit -m "Init personal homepage"
   git branch -M main
   git remote add origin https://github.com/Yi-Eaaa/Yi-Eaaa.github.io.git
   git push -u origin main
   ```

3. 仓库 Settings → Pages → Source 选 `main` 分支根目录，保存。
4. 稍等片刻访问 `https://Yi-Eaaa.github.io`。

> 若部署到项目仓库（如 `Yi-Eaaa.github.io/homepage`），资源路径为相对路径，同样可用。

## 结构

```
.
├── index.html            # 主页内容（About / Education / Experience / Publications / Projects / Honors）
├── .nojekyll             # 跳过 Jekyll 构建，按静态文件直接托管
├── assets/
│   ├── css/style.css     # 样式（左侧栏 + 右侧内容，响应式）
│   └── js/main.js
└── images/
    ├── avatar.jpg        # GitHub 头像
    └── intern.png
```

## 更新内容

所有文字都在 `index.html` 中，直接编辑对应 `<section>` 即可。
