# KochaWeb

个人网页展示

## Vite项目部署步骤
### 1、创建一个 GitHub 仓库
源文件置入 `main` 分支，dist文件夹置入 `gh-pages` 分支
### 2. 安装 `gh-pages` 依赖
在`Vite`项目根目录下，运行以下命令安装`gh-pages`包：
```bash
npm install gh-pages --save-dev
```
### 3. 配置 `vite.config.js`
```javascript
export default {
  // ...其他配置
  base: '/my-vite-app/',
}
```
### 4. 修改 `package.json`
```json
{
  "scripts": {
    "deploy": "gh-pages -d dist"
  }
}
```
### 5. 构建并部署项目
```bash
npm run build
```
```bash
npm run deploy
```

## 配置 Git 仓库
### 1. 初始化 Git 仓库
```bash
git init
```
### 2. 添加远程仓库
```bash
git remote add origin https://github.com/<your-username>/<your-repo>.git
```
将 `<your-username>` 替换为 GitHub 用户名，将 `<your-repo>` 替换为仓库名。
### 3. 添加和提交文件
```bash
git add .
git commit -m "Initial commit"
```
### 4. 推送到 Git 仓库
```bash
git push -u origin main
```
这一步可以在 `webstorm` 中提交和推送

## Tips
### 1. 注意更改本地分支名称
默认情况下，新初始化的 Git 仓库的主分支名称可能不是 `main`，而是 `master`
1. 检查本地分支名称
```bash
git branch
```
2. 重命名 `main` 分支
```bash
git branch -m master main
```
3. 推送到 Git 仓库
```bash
git push -u origin main
```
### 2. 可以使用SSH代理服务
代替HTTPS解决连接失败的问题