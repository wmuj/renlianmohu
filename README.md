# FaceBlur · 人脸模糊隐私保护工具

<p align="center">
  <img src="https://img.shields.io/badge/AI-人脸检测-6366f1?style=for-the-badge" alt="AI Face Detection">
  <img src="https://img.shields.io/badge/处理-完全本地-34d399?style=for-the-badge" alt="Local Processing">
  <img src="https://img.shields.io/badge/使用-无限次-fbbf24?style=for-the-badge" alt="Unlimited Usage">
</p>

## ✨ 功能特性

- 🧠 **AI 人脸自动检测** — 基于 [face-api.js](https://github.com/justadudewhohacks/face-api.js) TinyFaceDetector 模型
- 🔐 **完全本地处理** — 所有计算在浏览器端完成，图片绝不上传任何服务器
- ♾️ **无限次使用** — 无需注册、无需积分、无使用限制
- 🎨 **多种模糊模式** — 支持矩形模糊、椭圆模糊、像素化三种遮罩方式
- ⚡ **实时参数调节** — 模糊强度、检测灵敏度、边距扩展均可调节
- 📱 **响应式设计** — 完美适配桌面端与移动端

## 🚀 在线使用

访问 GitHub Pages 部署版本：

👉 **[https://wmuj.github.io/renlianmohu/](https://wmuj.github.io/renlianmohu/)**

## 📖 使用方法

1. 打开页面，等待 AI 模型自动加载（首次需要联网，之后自动缓存）
2. 拖放图片到上传区域，或点击选择文件
3. 调整模糊参数（强度、灵敏度、遮罩形状、边距）
4. 点击 **开始处理**
5. 预览结果后点击 **下载结果**

## 🛠️ 技术栈

| 技术 | 说明 |
|------|------|
| HTML5 / CSS3 / JavaScript | 纯前端实现 |
| [face-api.js](https://github.com/justadudewhohacks/face-api.js) | TensorFlow.js 人脸检测模型 |
| Canvas API | 图像处理与模糊渲染 |
| GitHub Pages | 静态站点托管 |

## 📁 项目结构

```
renlianmohu/
├── index.html    # 单页应用（HTML + CSS + JS 一体）
└── README.md     # 项目文档
```

## 💡 为什么做这个？

市面上的在线人脸模糊工具（如 img2go.com）虽然好用，但存在以下问题：

- ❌ 需要上传图片到第三方服务器
- ❌ 有使用次数限制（每次仅 16 积分）
- ❌ 用完需要开无痕窗口重新获取额度

**FaceBlur** 彻底解决这些痛点 —— 完全在浏览器端运行，无需上传，无限使用。

## 📄 许可证

MIT License
