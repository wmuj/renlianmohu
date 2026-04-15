# FaceBlur · 人脸模糊隐私保护工具

<p align="center">
  <img src="https://img.shields.io/badge/AI-双引擎人脸检测-6366f1?style=for-the-badge" alt="AI Face Detection">
  <img src="https://img.shields.io/badge/处理-完全本地-34d399?style=for-the-badge" alt="Local Processing">
  <img src="https://img.shields.io/badge/使用-无限次-fbbf24?style=for-the-badge" alt="Unlimited Usage">
  <img src="https://img.shields.io/badge/批量-最多50张-fb923c?style=for-the-badge" alt="Batch Processing">
</p>

## ✨ 功能特性

- 🧠 **双引擎 AI 人脸检测** — MediaPipe BlazeFace + face-api.js SSD MobileNet 双引擎并行检测，互为补充
- 🔐 **完全本地处理** — 所有计算在浏览器端完成，图片**绝不上传**任何服务器
- ♾️ **无限次使用** — 无需注册、无需积分、无使用限制
- 📦 **批量处理** — 单次最多支持 50 张图片，自动打包为 ZIP 下载
- 🎨 **椭圆模糊遮罩** — 以人脸为中心的椭圆形模糊，效果自然
- ⚡ **参数实时调节** — 模糊强度（0.1–20）、边距扩展（0–100）均可自由调节
- 🔀 **IoU 去重** — 双引擎检测结果自动合并去重，避免同一张脸重复模糊
- 📱 **响应式设计** — 完美适配桌面端与移动端

## 🚀 在线使用

👉 **[https://wmuj.github.io/renlianmohu/](https://wmuj.github.io/renlianmohu/)**

## 📖 使用方法

1. 打开页面，等待双引擎 AI 模型自动加载（首次需联网，此后自动缓存）
2. 拖放图片到上传区域，或点击选择文件（支持单张或批量）
3. 调整参数：
   - **模糊强度**：数值越大模糊越明显，推荐 3–5
   - **模糊范围**：人脸周围的扩展区域，0 为紧贴人脸
4. 点击 **开始处理** / **批量处理**
5. 预览结果后点击 **下载结果**（单张下载 JPG，批量下载 ZIP）

## 🛠️ 技术栈

| 技术 | 说明 |
|------|------|
| HTML5 / CSS3 / JavaScript | 纯前端单页实现，无框架依赖 |
| [MediaPipe Tasks Vision](https://ai.google.dev/edge/mediapipe/solutions/vision/face_detector) | 引擎①：Google BlazeFace 短程人脸检测 |
| [face-api.js](https://github.com/justadudewhohacks/face-api.js) | 引擎②：TensorFlow.js SSD MobileNet 人脸检测 |
| Canvas API | 图像处理与椭圆模糊渲染 |
| JSZip | 批量结果打包为 ZIP |
| GitHub Pages | 静态站点托管 + CI/CD 自动部署 |

## 📁 项目结构

```
renlianmohu/
├── index.html                          # 单页应用（HTML + CSS + JS 一体）
├── lib/
│   └── face-api.min.js                 # face-api.js 本地库
├── models/
│   ├── ssd_mobilenetv1_model-shard1    # SSD MobileNet 模型权重（分片1）
│   ├── ssd_mobilenetv1_model-shard2    # SSD MobileNet 模型权重（分片2）
│   └── ssd_mobilenetv1_model-weights_manifest.json
├── .github/
│   └── workflows/deploy.yml            # GitHub Actions 自动部署配置
└── README.md
```

## 💡 为什么做这个？

在制作含真人的视频/图集时，过审往往需要对人脸进行遮挡处理。市面上工具存在以下痛点：

- ❌ 需要上传图片到第三方服务器（隐私风险）
- ❌ 有使用次数限制（如每次仅 16 积分）
- ❌ 不支持批量处理

**FaceBlur** 彻底解决这些痛点 —— 完全在浏览器端运行，无需上传，无限使用，支持批量。

## 🔧 本地运行

无需安装任何依赖，直接用任意静态文件服务器打开即可：

```bash
# 方式一：Python
python -m http.server 8080

# 方式二：Node.js
npx serve .
```

然后访问 `http://localhost:8080`

> ⚠️ 不要直接双击 index.html 以 `file://` 协议打开，部分浏览器会因 CORS 限制导致模型加载失败。

## 📄 许可证

MIT License — 自由使用、修改、分发。

---

## ☕ 支持作者

如果这个工具帮到了你，欢迎请作者喝杯咖啡 ☕  
你的支持是持续维护和迭代的动力！

<p align="center">
  <img src="image/WV.jpg" alt="微信收款码" width="260" style="border-radius:12px;margin:8px">
  &nbsp;&nbsp;&nbsp;
  <img src="image/ZHI.jpg" alt="支付宝收款码" width="260" style="border-radius:12px;margin:8px">
</p>

<p align="center">
  <sub>微信扫码 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 支付宝扫码</sub>
</p>

---

<p align="center">
  <b>作者：<a href="https://github.com/wmuj">码上全栈创享家</a></b><br><br>
  <a href="https://github.com/wmuj/renlianmohu">
    <img src="https://img.shields.io/github/stars/wmuj/renlianmohu?style=social" alt="GitHub Stars">
  </a>
  &nbsp;
  <a href="https://github.com/wmuj/renlianmohu">
    <img src="https://img.shields.io/badge/GitHub-wmuj%2Frenlianmohu-181717?style=flat&logo=github" alt="GitHub Repo">
  </a>
  <br><br>
  📦 仓库地址：<a href="https://github.com/wmuj/renlianmohu">https://github.com/wmuj/renlianmohu</a><br>
  🌐 在线体验：<a href="https://wmuj.github.io/renlianmohu/">https://wmuj.github.io/renlianmohu/</a><br><br>
  <a href="https://github.com/wmuj/renlianmohu">⭐ 如果对你有帮助，欢迎 Star！</a>
</p>
