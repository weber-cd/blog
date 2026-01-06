# GitHub Pages 部署指南

## 快速开始

### 1. 推送代码到 GitHub

```bash
git add .
git commit -m "配置 GitHub Pages"
git push origin main
```

### 2. 启用 GitHub Pages

1. 进入你的 GitHub 仓库
2. 点击 **Settings**（设置）
3. 在左侧菜单找到 **Pages**（页面）
4. **重要提示**：如果看到 "Add a verified domain" 的提示，**可以忽略它**（这个选项只在你想使用自定义域名时才需要）
5. 向下滚动，找到 **Build and deployment**（构建和部署）或 **Source**（源）部分：
   - 在 **Source** 下拉菜单中，选择 **Deploy from a branch**（从分支部署）
   - 在 **Branch**（分支）下拉菜单中，选择 `main` 或 `master`（根据你的默认分支）
   - 在 **Folder**（文件夹）下拉菜单中，选择 `/ (root)`（根目录）
6. 点击 **Save**（保存）

**注意**：如果你看到的是 "GitHub Actions" 选项而不是 "Deploy from a branch"，也可以选择 GitHub Actions，但需要先确保代码已推送到仓库。

### 3. 访问你的网站

等待几分钟后，你的网站将在以下地址可用：
- `https://你的用户名.github.io/仓库名/`

例如：`https://username.github.io/blog/`

## 文件说明

- `_config.yml` - Jekyll 配置文件
- `index.html` - 网站主页（博客列表）
- 各个文章目录下的 `README.md` - 文章内容（Markdown 格式）

## 注意事项

1. **首次部署可能需要几分钟**：GitHub Pages 需要时间来构建和部署你的网站
2. **自定义域名**（可选）：如果你想使用自己的域名，可以在 `_config.yml` 中配置 `url` 字段
3. **图片路径**：确保文章中的图片路径使用相对路径（如 `images/xxx.png`）

## 更新内容

每次你推送新的更改到 GitHub，GitHub Pages 会自动重新构建和部署你的网站。通常需要 1-5 分钟。

## 故障排除

如果网站没有正常显示：

1. 检查 GitHub Actions（如果有）是否有构建错误
2. 确认 `_config.yml` 配置正确
3. 检查文件路径是否正确（区分大小写）
4. 查看 GitHub Pages 的构建日志（在 Settings > Pages 中）

