# 文脉 WenMai

> 学习用户写作思路的 AI 协作文档平台 —— 为会计 / 税务 / 审计报告场景而生
> 上传历史报告 → AI 提取「思路画像」→ 按你们的笔锋与思维写新报告

姊妹项目：[湛箴 zhanzhen](https://github.com/Ya-MiC/zhanzhen)（中小企业审计风险平台）
本仓库解决的是湛箴生态中「报告写作」这一环：**不是套模板，而是读懂人怎么写。**

---

## 一、产品形态（无 Docker 原则）

| 端 | 技术 | 产出 | 优先级 |
|---|---|---|---|
| 网页（主） | Vue 3 + TipTap | 浏览器直接用 | ★★★ |
| Windows 桌面 | Tauri 2.0 | 单文件 exe（约 10–20 MB） | ★★ |
| Android | Tauri 2.0 Mobile | APK，可上架应用商店 | ★ |

**一套 Vue 3 代码，三个端。** Tauri 2.0 原生支持 desktop + mobile 构建，
全程不需要 Docker：数据库用单文件 SQLite，AI 走 API（DeepSeek / 通义）或可选本地 Ollama。

## 二、核心：双 Skill 智能体

```
用户上传历史文章（docx/pdf/xlsx）
        │
        ▼
┌─────────────────┐     ┌──────────────────┐     ┌─────────────────┐
│  读书 Skill      │ ──► │  思路画像          │ ──► │  女娲 Skill      │
│  （理解作者）     │     │  Writing DNA      │     │  （按思路创作）   │
│                 │     │  （JSON + 向量库） │     │                 │
│ · 解析篇章结构    │     │ · 论证链条        │     │ · 生成思路大纲    │
│ · 提取论证逻辑    │     │ · 句式/术语指纹   │     │ · 分段成文        │
│ · 归纳推理路径    │     │ · 常用证据类型    │     │ · 对照画像自检    │
│ · 建立术语表      │     │ · 风险披露习惯    │     │ · 输出终稿        │
└─────────────────┘     └──────────────────┘     └─────────────────┘
```

- **读书 skill**：不是摘要，是逆向工程「这个人/这家所怎么思考」——章节怎么搭、结论怎么推、风险怎么披露。
- **女娲 skill**：先模仿思路出大纲，用户确认后再成文。思路对，文章才对。
- 技术路线：**RAG（检索增强）**，不微调模型。画像存 JSON + sqlite-vec 向量库，随写随更新。

详见 [SKILLS.md](SKILLS.md)。

## 三、编辑器（Proton Docs 美学）

- **TipTap** 块编辑器：每个段落/表格/图片是可拖拽的块，动态调整位置
- 左侧文档、右侧 AI 协作面板（类 Cursor 布局），面板可折叠
- 原生 Excel / Word：SheetJS 解析 xlsx，docx.js 生成 docx，双向导入导出
- 暗色/亮色主题，字体与图标全开源（见下）

## 四、多语言与开源资产

| 需求 | 开源方案 | License |
|---|---|---|
| 界面多语言 | vue-i18n | MIT |
| 文档翻译 | Argos Translate（离线开源）/ LLM 翻译 | MIT |
| 中文字体 | 思源黑体 / 思源宋体（Noto Sans SC/TC） | OFL |
| 西文字体 | Inter / Noto Sans | OFL |
| 图标 | Lucide | ISC |
| 编辑器 | TipTap | MIT |
| 表格解析 | SheetJS Community | Apache-2.0 |

## 五、技术栈与仓库结构

```
wenmai/
├─ src/                    # Vue 3 前端（三端共用）
│  ├─ editor/              # TipTap 编辑器与块系统
│  ├─ panel/               # 右侧 AI 协作面板
│  ├─ skills/              # 读书 / 女娲 skill 编排
│  ├─ rag/                 # 向量检索（sqlite-vec）
│  └─ i18n/                # 多语言
├─ src-tauri/              # Tauri 2.0（exe + APK 外壳）
├─ docs/                   # 设计文档
│  ├─ DDL.md               # 工程里程碑与死线
│  └─ SKILLS.md            # 双 skill 详细设计
└─ package.json
```

- 前端：Vue 3 + TypeScript + Vite + Pinia + Tailwind CSS
- 桌面/移动：Tauri 2.0（`npm run tauri build` 直接出 exe / APK）
- 数据：SQLite + sqlite-vec（单文件，免安装，随 exe 走）
- AI：DeepSeek API（默认）/ 通义千问 / 可选 Ollama 本地模型
- 未来对接：湛箴的规则引擎与证据哈希链（作为插件）

## 六、为什么不做 Docker

目标用户是事务所从业人员，不是运维。
exe 双击即用、APK 商店安装、网页打开即写 —— 数据默认存在本地，
需要团队协作时再可选接服务器。**能一个文件解决的，绝不上容器。**

## License

MIT
