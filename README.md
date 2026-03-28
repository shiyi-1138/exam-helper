# 📚 中高考简化答题助手

> 基于 Claude AI 的智能解题助手，专为中高考学生设计。输入或拍摄任意题目，立即获得三种解法、知识点定位与考试占比分析。

---

## ✨ 功能特点

| 功能 | 说明 |
|------|------|
| ⚡ **三种解法** | 按简便程度排序，方法一优先给出最快捷的速解技巧（特殊值法、整体代换、数形结合等） |
| 📷 **拍题识别** | 支持手机拍照、图片上传、电脑拖拽，Claude Vision 自动识别题目内容 |
| 📚 **知识点定位** | 精确到人教版 / 苏教版年级、学期、章节编号 |
| 📊 **考频分析** | 给出该知识点在中考 / 高考中的题型、分值与考查频率 |
| 📝 **典型例题** | 以最简便方法为示范，逐步讲解解题切入点与每步思路 |
| ⚠️ **易错警示** | 列出常见错误与正确做法 |

---

## 🚀 快速开始

### 1. 克隆仓库

```bash
git clone https://github.com/你的用户名/exam-helper.git
cd exam-helper
```

### 2. 配置 API Key

在 `index.html` 中找到 fetch 请求部分，添加你的 Anthropic API Key：

```javascript
headers: {
  'Content-Type': 'application/json',
  'x-api-key': '你的_ANTHROPIC_API_KEY',          // ← 填在这里
  'anthropic-version': '2023-06-01',
  'anthropic-dangerous-direct-browser-access': 'true'
},
```

> 获取 API Key：[console.anthropic.com](https://console.anthropic.com)

### 3. 本地运行

直接用浏览器打开 `index.html` 即可，**无需安装任何依赖**。

---

## 🌐 部署到 GitHub Pages

```bash
git add .
git commit -m "部署中高考简化答题助手"
git push origin main
```

然后进入仓库 → **Settings** → **Pages** → Source 选 `main` 分支 → 保存。

访问地址：`https://你的用户名.github.io/exam-helper`

---

## 📖 使用说明

**手动输入模式**
1. 在文本框输入题目
2. 选择科目和学段（或保持自动识别）
3. 点击「开始分析」或按 `Ctrl + Enter`

**拍题模式**
1. 切换到「📷 拍题 / 上传图片」标签
2. 手机端点击后直接调用相机拍照；电脑端可拖拽图片上传
3. 可在「补充说明」中注明具体问题，例如"只看第2问"
4. 点击「开始分析」，Claude Vision 自动识别题目文字

---

## 📁 项目结构

```
exam-helper/
├── index.html    # 完整应用（单文件，零依赖）
└── README.md     # 项目说明
```

---

## 🔧 技术栈

- **前端**：纯 HTML / CSS / JavaScript（零依赖，单文件）
- **AI 模型**：Claude Sonnet（Anthropic API）
- **图片识别**：Claude Vision（题目图片自动 OCR）
- **课程体系**：中国人教版 / 苏教版 K12

---

## ⚠️ 注意事项

- API Key 写在前端代码中存在暴露风险，**建议仅用于个人学习使用**
- 如需公开给他人使用，建议搭建后端代理以隐藏 API Key
- 拍题时请保证图片清晰、光线充足，识别效果更佳

---

## 📄 License

MIT License

---

> 由 [Claude AI](https://claude.ai) 驱动 · 适用于人教版 / 苏教版课程体系
