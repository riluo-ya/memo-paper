# memo-paper

一个精致的网页便签工具，支持多种字体实时切换、日期水印、一键导出为 PNG 图片。

## ✨ 特性

- 📝 **拟物设计** — 胶带、纸张纹理、横线，还原真实便签质感
- 🔤 **字体切换** — 支持系统字体 + 自定义字体（通过 `fonts.json` 配置）
- 🔍 **字体搜索** — 下拉框内置实时搜索，快速定位字体
- 📅 **日期水印** — 可选在导出图片时添加日期
- 💾 **导出 PNG** — 一键导出高清便签图片（支持 Ctrl+Enter 快捷键）
- 📱 **响应式** — 适配桌面和移动端

## 🚀 在线预览

> 部署到 GitHub Pages 后即可访问 `https://你的用户名.github.io/memo-paper/`

## 📂 项目结构

```
memo-paper/
├── index.html          # 主页面
├── fonts.json          # 字体配置文件
├── README.md           # 本文件
├── .gitignore          # Git 忽略规则
└── fonts/              # 字体文件目录（可选，见下方说明）
    └── ...
```

## 🔤 字体配置

编辑 `fonts.json` 添加你的字体：

```json
{
  "fonts": [
    { "name": "系统默认", "family": "system-ui, sans-serif", "type": "system" },
    { "name": "宋体", "family": "SimSun, serif", "type": "fallback" },
    {
      "name": "英-衬线 · My Font",
      "family": "'MyFont', serif",
      "src": "./fonts/my-font/MyFont-Regular.ttf",
      "type": "custom"
    }
  ]
}
```

### 字体文件路径说明

- `type: "system"` — 系统自带字体，无需文件
- `type: "fallback"` — 系统常见字体，无需文件
- `type: "custom"` — 自定义字体，需放在 `fonts/` 目录下，并通过 `src` 指定相对路径

## ⚠️ 关于字体文件

本项目**默认不包含字体文件**。原因：
- 商用字体文件体积大，不适合放入 Git 仓库
- GitHub 单文件限制 100MB，仓库建议 < 1GB

### 推荐做法

**方式一：本地使用（推荐）**
1. 克隆仓库到本地
2. 将你的字体文件放入 `fonts/` 目录
3. 运行 `python generate_fonts_json.py` 自动生成 `fonts.json
4. 用浏览器打开 `index.html` 即可使用

**方式二：精选字体上传 GitHub Pages**
1. 挑选 10-50 个常用字体放入 `fonts/` 目录
2. 确保总大小 < 100MB
3. 推送至 GitHub，开启 GitHub Pages

**方式三：使用 CDN / 外部链接**
在 `fonts.json` 中，`src` 支持完整 URL：
```json
{ "src": "https://cdn.example.com/fonts/MyFont.woff2" }
```

## 🛠️ 本地开发

无需构建工具，直接用浏览器打开 `index.html`。

如需本地服务器：
```bash
# Python 3
python -m http.server 8000

# Node.js
npx serve .
```

## 📄 开源协议

MIT License
