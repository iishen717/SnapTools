# SnapTools

面向开发者的轻量级在线工具集，纯静态页面，开箱即用。

## 工具列表

### Base64
- **Base64 转图片** — 粘贴 Base64 或 `data:image/...;base64` 字符串，自动识别图片类型并预览。

### Cron
- **Cron 表达式生成器** — 生成 Quartz 风格 Cron 表达式，支持秒/分/时/日/月/周/年字段，并提供最近运行时间预览。

### Json
- **JSON 解析器** — 格式化、校验与树形浏览 JSON 数据。
- **JSON 转 C# 类** — 将 JSON 结构转换为 C# 强类型类定义。
- **C# 转 TS 实体** — 将 C# 类/模型转换为 TypeScript 接口或类型。
- **DDL 转 C# 实体** — 将 SQL DDL 建表语句转换为 C# 实体类。

### Jwt
- **JWT 解析器** — 解码 JWT 的 Header 与 Payload，直观查看令牌内容。

## 项目结构

```
SnapTools/
├── index.html              # 首页
├── Base64/
│   └── index.html          # Base64 转图片
├── Cron/
│   └── index.html          # Cron 表达式生成器
├── Json/
│   ├── index.html          # JSON 解析器
│   ├── ToCsharp.html       # JSON 转 C# 类
│   ├── ToTypescript.html   # C# 转 TS 实体
│   └── ToEntity.html       # DDL 转 C# 实体
└── Jwt/
    └── index.html          # JWT 解析器
```

## 本地运行

无需安装依赖，直接用任意静态服务器打开即可：

```bash
# 方式一：Python
python -m http.server 8080

# 方式二：Node.js
npx serve .

# 方式三：直接浏览器打开 index.html
```

## 添加新工具

1. 在根目录新建文件夹，放入 HTML 文件。
2. 在首页 `index.html` 的 `[data-folder-track]` 容器中添加对应的 `[data-folder-group]` 卡片分组，首页会自动展示新工具。
