# 🚀 快速部署指南

## 当前状态

✅ IM 对话框 Demo 已创建完成
✅ Git 仓库已初始化
⏳ 等待部署到公开地址

---

## 方式 1：使用 Vercel 部署（最简单，1 分钟）

### 步骤：

1. **访问 Vercel 官网**
   ```
   https://vercel.com/new
   ```

2. **导入 Git 仓库**
   - 点击 "Import Git Repository"
   - 选择你的 GitHub 仓库
   - 或上传本地文件

3. **一键部署**
   - Vercel 会自动检测静态页面
   - 点击 "Deploy"
   - 获得公开访问地址

### 或直接使用 CLI：

```bash
# 安装
npm install -g vercel

# 登录
vercel login

# 部署
cd /home/admin/.openclaw/workspace/projects/im-chat-demo
vercel --prod
```

---

## 方式 2：使用 GitHub Pages

### 步骤：

1. **创建 GitHub 仓库**
   ```
   https://github.com/new
   仓库名：im-chat-demo
   设为公开
   ```

2. **推送代码**
   ```bash
   cd /home/admin/.openclaw/workspace/projects/im-chat-demo
   git remote add origin https://github.com/你的用户名/im-chat-demo.git
   git branch -M main
   git push -u origin main
   ```

3. **启用 Pages**
   - 进入仓库 Settings
   - 点击 Pages
   - Source 选择 "main" 分支
   - 点击 Save

4. **访问地址**
   ```
   https://你的用户名.github.io/im-chat-demo/
   ```

---

## 方式 3：使用 Netlify Drop（无需注册）

### 步骤：

1. **访问**
   ```
   https://app.netlify.com/drop
   ```

2. **拖拽文件夹**
   - 将 `im-chat-demo` 文件夹拖到上传区域
   - 等待上传完成

3. **获得地址**
   - 自动生成 `https://xxx-xxx.netlify.app`

---

## 方式 4：使用 Cloudflare Pages

### 步骤：

1. **访问**
   ```
   https://pages.cloudflare.com/
   ```

2. **连接 Git 或直接上传**
   - 连接 GitHub 仓库
   - 或直接上传文件

3. **部署**
   - 自动构建和部署
   - 获得 `https://xxx.pages.dev` 地址

---

## 方式 5：使用 tiiny.host（最快，30 秒）

### 步骤：

1. **访问**
   ```
   https://tiiny.host/
   ```

2. **上传 HTML 文件**
   - 拖拽 `index.html` 到上传区域
   - 输入自定义链接名

3. **发布**
   - 点击 "Upload"
   - 立即获得公开地址

---

## 📋 本地测试

如需在本地测试：

```bash
cd /home/admin/.openclaw/workspace/projects/im-chat-demo
python3 -m http.server 8080
```

访问：`http://localhost:8080`

---

## 🎯 推荐方案

| 方案 | 时间 | 难度 | 推荐度 |
|------|------|------|--------|
| tiiny.host | 30 秒 | ⭐ | ⭐⭐⭐⭐⭐ |
| Vercel | 1 分钟 | ⭐⭐ | ⭐⭐⭐⭐⭐ |
| Netlify Drop | 1 分钟 | ⭐ | ⭐⭐⭐⭐ |
| GitHub Pages | 5 分钟 | ⭐⭐⭐ | ⭐⭐⭐⭐ |
| Cloudflare Pages | 3 分钟 | ⭐⭐ | ⭐⭐⭐⭐ |

---

## ✅ 部署后

部署完成后，你将获得：
- 公开访问 URL
- HTTPS 加密
- 全球 CDN 加速
- 自动 SSL 证书

---

*选择最适合你的方式开始部署吧！* 🚀
