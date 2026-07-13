#  memo-paper

> 一个纯前端、零依赖的在线便签工具，单 HTML 文件即可运行。

## 预览

![preview](/jpg/1.jpg)

## 功能特性

| 特性 | 说明 |
|------|------|
| 🎨 **6 种便签颜色** | 暖黄、柔粉、淡蓝、薄荷、浅紫、暖橙 |
| ✍️ **3 种纸张纹理** | 横线、方格、空白 |
| 🔤 **字体管理** | 支持系统字体 + 本地字体文件上传（.ttf / .otf / .woff / .woff2） |
| ⚙️ **排版微调** | 字号（14–28px）、行距（1.4–2.4）实时可调 |
| 💾 **自动保存** | 内容自动写入 LocalStorage，刷新不丢失 |
| 📤 **导出图片** | 一键导出高分辨率 PNG（3x DPR） |
| 📅 **日期水印** | 可选在导出图片底部显示当前日期 |
| ⌨️ **快捷键** | `Ctrl + Enter` 快速导出 |

## 快速开始

无需构建，直接打开即可使用：

```bash
git clone https://github.com/YOUR_USERNAME/memo-paper.git
cd memo-paper
open index.html
```

或部署到任意静态托管服务（GitHub Pages、Vercel、Netlify 等）。

## 字体上传说明

1. 点击字体选择框中的「上传字体文件」
2. 选择本地字体文件（支持多选批量上传）
3. 上传成功后自动加入「我的字体」分组
4. 上传的字体仅在当前浏览器会话中有效（通过 Blob URL + FontFace API 加载）

## 技术栈

- 纯原生 HTML / CSS / JavaScript
- 零第三方依赖
- 使用 Canvas API 生成导出图片
- 使用 FontFace API 动态加载本地字体
- LocalStorage 持久化存储

## 浏览器兼容性

| 浏览器 | 支持情况 |
|--------|----------|
| Chrome / Edge | ✅ 完整支持 |
| Firefox | ✅ 完整支持 |
| Safari | ✅ 完整支持 |
| 移动端浏览器 | ✅ 基本支持（导出功能可用） |

> 字体上传功能需要浏览器支持 [FontFace API](https://caniuse.com/font-loading)。

## 项目结构

```
memo-paper/
└──jpg          # 存放截图的地方（用于展示图片）
└── index.html          # 完整的单文件应用（含样式、脚本、HTML）
```

## 自定义主题

便签颜色定义在 CSS 变量中，可自由修改：

```css
/* 在 <style> 标签中搜索以下颜色值 */
#fef9e7   /* 暖黄 */
#ffe4e1   /* 柔粉 */
#e0f0ff   /* 淡蓝 */
#e8f5e9   /* 薄荷 */
#f3e5f5   /* 浅紫 */
#fff3e0   /* 暖橙 */
```

## 许可证

[MIT](LICENSE)

---

Made with ☕ and sticky notes.
