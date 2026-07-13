# 陈宇轩个人网站

这是一个纯静态个人主页，可直接部署到 GitHub Pages

## 本地预览

在 `personal_website` 目录下运行：

```bash
python -m http.server 8000
```

然后打开：

```text
http://localhost:8000
```

也可以在 VS Code 里用 Live Preview 打开 `index.html`。

## 发布到 GitHub Pages

### 方案 A：个人主页地址

这个方案会得到：

```text
https://<your-github-username>.github.io/
```

步骤：

1. 在 GitHub 新建仓库，仓库名必须是：

```text
<your-github-username>.github.io
```

2. 把本目录下的所有文件上传到仓库根目录。

3. 如果用命令行，可以在本目录运行：

```bash
git init
git add .
git commit -m "Add personal website"
git branch -M main
git remote add origin https://github.com/<your-github-username>/<your-github-username>.github.io.git
git push -u origin main
```

4. 等 GitHub Pages 部署完成后访问：

```text
https://<your-github-username>.github.io/
```

### 方案 B：项目主页地址

这个方案会得到：

```text
https://<your-github-username>.github.io/<repo-name>/
```

步骤：

1. 新建任意仓库，例如 `personal-website`。
2. 上传本目录下所有文件。
3. 进入 GitHub 仓库 `Settings -> Pages`。
4. Source 选择 `Deploy from a branch`。
5. Branch 选择 `main`，目录选择 `/root`。

## 文件结构

```text
index.html
styles.css
script.js
.nojekyll
assets/
  profile.jpg
  evgt-teaser.jpg
  evgt-teaser.png
```
