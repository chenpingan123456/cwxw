# 前端项目部署指南 (最简单方案)

## 1. 无需服务器的部署方式

### 方案1: GitHub Pages (完全免费)
1. 在GitHub上创建新仓库
2. 将项目代码上传到仓库
3. 在项目根目录运行构建命令:
```bash
pnpm install
pnpm build
```
4. 将 `dist/static` 目录中的所有文件上传到仓库的 `gh-pages` 分支
5. 在仓库设置中启用GitHub Pages
6. 访问: `https://[你的用户名].github.io/[仓库名]/`

### 方案2: Vercel (免费)
1. 注册Vercel账号(可使用GitHub账号)
2. 将项目上传到GitHub/GitLab/Bitbucket
3. 在Vercel控制台导入项目
4. Vercel会自动检测并部署
5. 访问Vercel提供的域名

### 方案3: Netlify (免费)
1. 注册Netlify账号
2. 拖放 `dist/static` 文件夹到Netlify部署区域
3. 或连接Git仓库自动部署
4. 访问Netlify提供的域名

## 2. 本地开发运行
```bash
pnpm install
pnpm dev
```
访问: http://localhost:3000

## 3. 生产环境构建
```bash
pnpm install
pnpm build
```
构建完成后，生成的文件位于 `dist/static` 目录

## 4. 本地测试生产版本
```bash
npx serve -s dist/static
```
访问: http://localhost:3000

## 5. 常见问题
### Q: 页面刷新后出现404
A: 单页应用需要将所有路由重定向到index.html

### Q: 如何更新网站内容?
A: 重新构建并上传新的 `dist/static` 目录内容

### Q: 这些服务需要付费吗?
A: 对于小型项目，上述服务都有免费套餐足够使用



