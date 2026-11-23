# SmartClip 资源库

[English](./README.md) | 简体中文

[![Website](https://img.shields.io/badge/Website-smartclip.app-blue?style=flat-square)](https://smartclip.app/zh-CN)
[![Chrome Web Store](https://img.shields.io/badge/Chrome-Web%20Store-4285F4?style=flat-square&logo=googlechrome&logoColor=white)](https://chromewebstore.google.com/detail/smartclip/oddgijbbpmjcnomkfmcdjiolcciemddf)
[![Edge Add-ons](https://img.shields.io/badge/Edge-Add--ons-0078D7?style=flat-square&logo=microsoftedge&logoColor=white)](https://microsoftedge.microsoft.com/addons/detail/smartclip/lkdcgakepgnmaghahbkgmmjpfmloilml)
[![Firefox Add-ons](https://img.shields.io/badge/Firefox-Add--ons-FF7139?style=flat-square&logo=firefoxbrowser&logoColor=white)](https://addons.mozilla.org/zh-CN/firefox/addon/smartclip/)
![Version](https://img.shields.io/badge/Version-v2.2-059669?style=flat-square)
![Manifest](https://img.shields.io/badge/Manifest-V3-374151?style=flat-square)
![MCP Ready](https://img.shields.io/badge/MCP-WebSocket%20Ready-7C3AED?style=flat-square)

> **SmartClip v2.2** 是一款本地优先、AI 驱动的浏览器网页剪藏扩展（Manifest V3），支持 Chrome、Edge 与 Firefox。可将网页干净保存至 **18 种目标**（Notion、Obsidian、飞书文档、思源笔记、Flomo、Logseq、Joplin、Memos、语雀、Markdown 等），内置 **BYOK / 离线 Ollama AI 阅读助手**、**五色环形划线**、**视频双语字幕**、**图片防盗链自动转存** 与 **WebSocket MCP Agent 集成**。所有付费方案均为**一次性买断**，无任何订阅。

本仓库（`ismaike/smartclip-repo`）是 SmartClip 的官方资源库，集中维护社区站点剪藏模板、AI 提示词预设与配套使用文档。

---

## 官方链接与指南入口

| 资源 | 链接 |
|---|---|
| 官方网站（简中 / 繁中 / EN） | [smartclip.app/zh-CN](https://smartclip.app/zh-CN) |
| Chrome 应用商店 | [安装 Chrome 版](https://chromewebstore.google.com/detail/smartclip/oddgijbbpmjcnomkfmcdjiolcciemddf) |
| Microsoft Edge 加载项 | [安装 Edge 版](https://microsoftedge.microsoft.com/addons/detail/smartclip/lkdcgakepgnmaghahbkgmmjpfmloilml) |
| Mozilla Firefox 附加组件 | [安装 Firefox 版](https://addons.mozilla.org/zh-CN/firefox/addon/smartclip/) |
| 主流网页剪藏工具横评 | [SmartClip vs Notion、Obsidian、Readwise 与 Raindrop](https://smartclip.app/zh-CN/compare/best-web-clippers) |
| 帮助中心与完整 FAQ | [smartclip.app/zh-CN/help](https://smartclip.app/zh-CN/help) |
| 版本更新日志 | [smartclip.app/zh-CN/changelog](https://smartclip.app/zh-CN/changelog) |
| AI / LLM 索引（`llms.txt`） | [smartclip.app/llms.txt](https://smartclip.app/llms.txt) |
| X (Twitter) | [@maike_93z](https://x.com/maike_93z) |

---

## 核心能力（v2.2）

- **净室正文提取**：自动剥离广告、侧栏、评论区与追踪像素，高保真保留标题、列表、代码块与表格，并对微信公众号、Bilibili、YouTube 提供专项适配。
- **五色环形划线与划词 AI**：网页划词即时五色高亮，二次访问自动恢复；支持流式划词翻译、解释与摘要。
- **视频双语字幕与生词本**：支持 Bilibili / YouTube 视频双语字幕停靠与生词自动收录（Lite 解锁生词本闪卡）。
- **沉浸阅读预览与 AI 大纲**：提供暖纸、白纸、深色三套阅读主题，支持属性面板检查、AI 一键生成大纲与图片 / PDF 导出（Lite）。
- **自带密钥（BYOK）多模型 AI 对话**：支持 OpenAI、Anthropic、Google、DeepSeek 以及本地 **Ollama**（可完全离线），请求从浏览器直连模型提供商。
- **防盗链图片自动转存**：剪藏时下载受保护图片并上传至你自己的 **AWS S3**、**阿里云 OSS**、**腾讯云 COS** 或 **Cloudinary**，原网页删除或加付费墙后图片依然完整。
- **批量队列与断网续传**：支持多标签页与 CSV 清单批量保存（Lite / Pro），遇限流自动重试并持久化队列。
- **MCP Agent 桥接（Pro）**：通过本地 WebSocket 实现 **MCP（Model Context Protocol）**，让 **Claude Code**、**Cursor** 与 **Gemini CLI** 直接读取已打开的浏览器标签页并自动归档笔记。

---

## 18 种保存目标与专题指南

| 分类 | 支持目标 | 专题指南 |
|---|---|---|
| **云端与团队文档** | Notion、FlowUs 息流、飞书文档、语雀、Wolai、GitHub | [Notion 指南](https://smartclip.app/zh-CN/notion-web-clipper) · [飞书指南](https://smartclip.app/zh-CN/feishu-web-clipper) |
| **本地与双链知识库** | Obsidian、思源笔记（SiYuan）、Logseq（`smartclip/` 页面树）、Joplin | [Obsidian 指南](https://smartclip.app/zh-CN/obsidian-web-clipper) · [思源笔记指南](https://smartclip.app/zh-CN/siyuan-web-clipper) |
| **卡片与轻笔记** | Flomo（Webhook 卡片）、Memos、得到大脑 | [Flomo 指南](https://smartclip.app/zh-CN/flomo-web-clipper) |
| **对象存储与通用导出** | AWS S3 / 阿里云 OSS / 腾讯云 COS 同步、Markdown (`.md`) 下载、剪贴板纯净复制 | [微信文章转 Markdown 指南](https://smartclip.app/zh-CN/wechat-to-markdown) |
| **AI 编程助手** | 通过 WebSocket MCP 接入 Claude Code、Cursor、Gemini CLI | [MCP 浏览器扩展指南](https://smartclip.app/zh-CN/mcp-browser-extension) |

---

## 仓库目录结构

```text
smartclip-repo/
├── templates/           # 社区站点提取模板（CSS / DOM 选择器规则）
│   ├── templates.json   # 模板注册表索引
│   ├── tietu.json       # 微信公众号适配（*.mp.weixin.qq.com）
│   ├── zhihu01.json     # 知乎专栏（*.zhuanlan.zhihu.com）
│   ├── zhihu02.json     # 知乎问答取首条（*.zhihu.com）
│   └── zhihu03.json     # 知乎问答特殊场景（*.zhihu.com）
├── prompts/             # 可复用的 AI 提示词预设
│   ├── prompts.json     # 提示词注册表索引
│   └── recommendation.md
└── docs/                # 说明文档资源
```

### 剪藏模板（`templates/`）

由 [`templates/templates.json`](./templates/templates.json) 统一索引：

| ID | 名称 | 匹配规则 | 文件 |
|---|---|---|---|
| `tietu` | 贴图（微信公众号） | `*.mp.weixin.qq.com` | [`templates/tietu.json`](./templates/tietu.json) |
| `zhihu01` | 知乎专栏 | `*.zhuanlan.zhihu.com` | [`templates/zhihu01.json`](./templates/zhihu01.json) |
| `zhihu02` | 知乎问答取第一个 | `*.zhihu.com` | [`templates/zhihu02.json`](./templates/zhihu02.json) |
| `zhihu03` | 知乎问答特殊场景 | `*.zhihu.com` | [`templates/zhihu03.json`](./templates/zhihu03.json) |

### 提示词预设（`prompts/`）

由 [`prompts/prompts.json`](./prompts/prompts.json) 统一索引：

| 名称 | 作用域 | 文件 |
|---|---|---|
| 推荐产品 | `content` | [`prompts/recommendation.md`](./prompts/recommendation.md) |

---

## 参与贡献模板与提示词

欢迎通过 Pull Request 贡献站点适配规则与高质量提示词：

### 1. 贡献站点剪藏模板

1. 参考 [`templates/zhihu01.json`](./templates/zhihu01.json) 的结构，在 `templates/<template-id>.json` 新建配置文件：
   - 基础字段：`id`、`name`、`pattern`（如 `*.example.com`）、`version`、`enabled`、`priority`
   - 元信息选择器：`titleSelector`、`authorSelector`
   - 正文过滤规则：`filter.include` 与 `filter.exclude` 选择器数组
2. 在 [`templates/templates.json`](./templates/templates.json) 中追加 `{ "id", "name", "file", "pattern" }` 注册条目。
3. 校验 JSON 格式无误后提交 PR，并附上目标站点与测试链接。

### 2. 贡献 AI 提示词

1. 在 `prompts/<prompt-name>.md` 新增 Markdown 提示词文件。
2. 在 [`prompts/prompts.json`](./prompts/prompts.json) 中登记 `{ "file", "name", "scope" }`。
3. 提交 PR 说明适用场景与预期输出效果。

---

## 定价与隐私说明

所有付费方案均为**一次性买断**，无订阅、无自动续费：

- **免费版（¥0 永久免费）**：完整单篇剪藏（限默认单个保存目标）、内置模板、BYOK AI 对话 / 摘要 / 翻译（支持本地离线 Ollama）、五色划线高亮、框选提取、自配图床上传（S3 / OSS / COS / Cloudinary）、阅读预览与 AI 大纲、生词标注。
- **Lite 买断（一次性付费）**：包含免费版全部功能 + 同时保存至多个笔记应用（保存时任选目标）+ CSV 批量保存（无限制）+ 不限量自定义模板 + 预览导出图片或 PDF + 生词本闪卡。
- **Pro 买断（一次性付费）**：包含 Lite 版全部功能 + **MCP Agent 接入**（Claude Code、Cursor、Gemini CLI）+ 更多批量方式（如推文收藏夹）+ 后续全部新功能（跨笔记迁移、AI 工作流）+ 优先支持。

**本地优先与隐私保护**：剪藏内容由浏览器直写目标笔记应用，不经过 SmartClip 服务器；API Key 与图床密钥采用 **AES-GCM** 本地加密保存；搭配 **Ollama** 时可实现 100% 离线运行。
