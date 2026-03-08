# 🚀 自动部署配置指南

已为你配置好完整的自动部署流程！

---

## ✅ 已完成的配置

- [x] Git 仓库初始化
- [x] package.json 创建
- [x] Vercel 本地安装
- [x] GitHub Actions 工作流配置
- [x] Vercel 配置文件创建

---

## 📋 接下来需要做的（5 步完成）

### 步骤 1：创建 GitHub 仓库

1. 访问 https://github.com/new
2. 仓库名：`im-chat-demo`
3. 设为 **公开仓库** (Public)
4. 点击 "Create repository"

---

### 步骤 2：推送代码到 GitHub

```bash
cd /home/admin/.openclaw/workspace/projects/im-chat-demo

# 重命名分支为 main
git branch -M main

# 添加远程仓库（替换为你的 GitHub 用户名）
git remote add origin https://github.com/你的用户名/im-chat-demo.git

# 推送代码
git push -u origin main
```

---

### 步骤 3：在 Vercel 创建项目

1. 访问 https://vercel.com/new
2. 点击 **"Import Git Repository"**
3. 选择刚才创建的 `im-chat-demo` 仓库
4. 点击 **"Import"**
5. 保持默认设置，点击 **"Deploy"**

等待部署完成后，你会获得一个预览地址。

---

### 步骤 4：获取 Vercel 密钥

1. 访问 https://vercel.com/account/tokens
2. 点击 **"Create"** 创建 Token
3. 复制 Token（只显示一次，妥善保存）

然后在 Vercel 项目页面获取：
- **Project ID**：在项目设置 → General → Project ID
- **Org ID**：在账户设置 → Settings → Account ID

---

### 步骤 5：配置 GitHub Secrets

1. 进入 GitHub 仓库页面
2. 点击 **Settings** → **Secrets and variables** → **Actions**
3. 点击 **"New repository secret"**
4. 添加以下 3 个密钥：

| Name | Value |
|------|-------|
| `VERCEL_TOKEN` | 步骤 4 创建的 Token |
| `VERCEL_ORG_ID` | 你的 Vercel Org ID |
| `VERCEL_PROJECT_ID` | 你的 Vercel Project ID |

---

## 🎉 完成！

配置完成后，每次推送代码到 `main` 分支时：

```
git push origin main
```

GitHub Actions 会自动：
1. 检出代码
2. 安装依赖
3. 部署到 Vercel
4. 更新公开地址

---

## 📝 验证部署

### 手动触发部署

```bash
# 修改代码后
git add .
git commit -m "更新功能"
git push origin main
```

### 查看部署状态

1. GitHub: Actions 标签页查看构建状态
2. Vercel: 项目页面查看部署历史

---

## 🌐 访问地址

部署成功后，你会获得：

- **生产环境**: `https://你的项目名.vercel.app`
- **预览环境**: 每次 PR 都会生成预览地址

---

## 🔧 本地测试部署

在部署前可以本地测试：

```bash
cd /home/admin/.openclaw/workspace/projects/im-chat-demo

# 使用 npx 运行 Vercel 部署
npx vercel --prod

# 或本地预览
npx vercel dev
```

---

## 📊 自动部署流程图

```
推送代码到 GitHub
       ↓
GitHub Actions 触发
       ↓
安装 Node.js
       ↓
安装依赖 (npm ci)
       ↓
调用 Vercel API
       ↓
Vercel 构建和部署
       ↓
生成公开地址
       ↓
部署完成！✅
```

---

## ⚡ 快速命令

```bash
# 查看部署状态
git status

# 推送代码触发部署
git push origin main

# 查看 GitHub Actions 日志
# 访问：https://github.com/用户名/im-chat-demo/actions
```

---

## 🆘 故障排除

### 问题 1：GitHub Actions 失败

检查：
- Secrets 是否正确配置
- Vercel Token 是否有效
- 网络连接是否正常

### 问题 2：Vercel 部署失败

检查：
- vercel.json 配置是否正确
- 项目是否已在 Vercel 创建

### 问题 3：权限错误

```bash
# 修复 npm 权限问题
npm config set prefix ~/.npm-global
```

---

## 📞 需要帮助？

如果遇到问题：
1. 查看 GitHub Actions 日志
2. 查看 Vercel 部署日志
3. 检查配置文件是否正确

---

*配置完成后，你的每次代码推送都会自动部署！* 🚀
