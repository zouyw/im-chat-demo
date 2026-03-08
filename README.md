# IM 即时通讯对话框 Demo

一个精美的 IM 即时通讯前端 Demo，支持消息发送、自动回复、快捷回复等功能。

## 🎨 功能特性

- ✅ 精美的渐变 UI 设计
- ✅ 实时消息发送和显示
- ✅ 智能自动回复
- ✅ 快捷回复按钮
- ✅ 消息时间戳
- ✅ 滚动动画效果
- ✅ 响应式设计（支持移动端）

## 🚀 快速部署（3 种方式）

### 方式 1：Vercel 部署（推荐，1 分钟上线）

```bash
# 1. 安装 Vercel CLI
npm install -g vercel

# 2. 登录 Vercel
vercel login

# 3. 部署
cd /home/admin/.openclaw/workspace/projects/im-chat-demo
vercel --prod
```

部署完成后会返回一个 `https://xxx.vercel.app` 的网址。

---

### 方式 2：GitHub Pages 部署

```bash
# 1. 初始化 Git 仓库
cd /home/admin/.openclaw/workspace/projects/im-chat-demo
git init
git add .
git commit -m "Initial commit"

# 2. 创建 GitHub 仓库并推送
# 在 GitHub 上创建新仓库，然后：
git remote add origin https://github.com/你的用户名/im-chat-demo.git
git push -u origin main

# 3. 启用 GitHub Pages
# 在 GitHub 仓库设置中：
# Settings → Pages → Source → 选择 main 分支 → Save
```

访问地址：`https://你的用户名.github.io/im-chat-demo/`

---

### 方式 3：Netlify 部署

```bash
# 1. 安装 Netlify CLI
npm install -g netlify-cli

# 2. 登录并部署
netlify login
netlify deploy --prod --dir=.
```

---

### 方式 4：本地运行测试

```bash
# 使用 Python 启动本地服务器
cd /home/admin/.openclaw/workspace/projects/im-chat-demo
python3 -m http.server 8080

# 访问 http://localhost:8080
```

---

## 📁 文件结构

```
im-chat-demo/
├── index.html      # 主页面（包含所有 HTML/CSS/JS）
└── README.md       # 说明文档
```

---

## 🎯 使用方式

1. **发送消息**：在输入框输入文字，点击发送按钮或按回车
2. **快捷回复**：点击预设的快捷回复按钮
3. **自动回复**：系统会根据关键词自动回复

### 支持的关键词回复

| 关键词 | 回复内容 |
|--------|----------|
| 你好 | 问候回复 |
| hello | 英文问候 |
| 在吗 | 在线回复 |
| 天气 | 天气回复 |
| 笑话 | 讲笑话 |
| 推荐 | 美食推荐 |
| 谢谢 | 礼貌回复 |
| 再见 | 告别回复 |

---

## 🎨 自定义

### 修改主题颜色

在 `index.html` 的 `<style>` 部分修改：

```css
/* 主色调 */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* 修改为你喜欢的颜色 */
background: linear-gradient(135deg, #你的颜色 0%, #你的颜色 100%);
```

### 修改自动回复

在 `index.html` 的 `<script>` 部分修改 `autoReplies` 对象：

```javascript
const autoReplies = {
    '你的关键词': '你的回复内容',
    // 添加更多...
};
```

---

## 📱 截图预览

打开页面后可看到：
- 渐变紫色头部
- 机器人头像和在线状态
- 消息气泡（ incoming/outgoing 不同样式）
- 底部输入框和发送按钮
- 快捷回复按钮

---

## 🌐 在线 Demo

如已部署，访问地址将显示在这里。

---

## 📄 License

MIT License

---

*Created with ❤️ for IM Chat Demo*
# im-chat-demo
