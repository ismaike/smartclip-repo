# SmartClip Resource Hub

English | [简体中文](./README.zh-CN.md)

[![Website](https://img.shields.io/badge/Website-smartclip.app-blue?style=flat-square)](https://smartclip.app)
[![Chrome Web Store](https://img.shields.io/badge/Chrome-Web%20Store-4285F4?style=flat-square&logo=googlechrome&logoColor=white)](https://chromewebstore.google.com/detail/smartclip/oddgijbbpmjcnomkfmcdjiolcciemddf)
[![Edge Add-ons](https://img.shields.io/badge/Edge-Add--ons-0078D7?style=flat-square&logo=microsoftedge&logoColor=white)](https://microsoftedge.microsoft.com/addons/detail/smartclip/lkdcgakepgnmaghahbkgmmjpfmloilml)
[![Firefox Add-ons](https://img.shields.io/badge/Firefox-Add--ons-FF7139?style=flat-square&logo=firefoxbrowser&logoColor=white)](https://addons.mozilla.org/en-US/firefox/addon/smartclip/)
![Version](https://img.shields.io/badge/Version-v2.2-059669?style=flat-square)
![Manifest](https://img.shields.io/badge/Manifest-V3-374151?style=flat-square)
![MCP Ready](https://img.shields.io/badge/MCP-WebSocket%20Ready-7C3AED?style=flat-square)

> **SmartClip v2.2** is a local-first, AI-powered web clipper browser extension (Manifest V3) for Chrome, Edge, and Firefox. Save clean web pages into **18 destinations** — including Notion, Obsidian, Feishu Docs, SiYuan, Flomo, Logseq, Joplin, Memos, Yuque, and Markdown — with **BYOK / offline Ollama AI**, a **5-color radial highlighter**, **bilingual video subtitles**, **anti-hotlink image backup**, and **WebSocket MCP Agent integration**. All paid tiers are **one-time purchases** with zero recurring subscriptions.

This repository (`ismaike/smartclip-repo`) is the official community resource hub for SmartClip, hosting site extraction templates, AI prompt presets, and documentation.

---

## Official Links & Guides

| Resource | Link |
|---|---|
| Official Website (EN / 简中 / 繁中) | [smartclip.app](https://smartclip.app/en) |
| Chrome Web Store | [Install for Chrome](https://chromewebstore.google.com/detail/smartclip/oddgijbbpmjcnomkfmcdjiolcciemddf) |
| Microsoft Edge Add-ons | [Install for Edge](https://microsoftedge.microsoft.com/addons/detail/smartclip/lkdcgakepgnmaghahbkgmmjpfmloilml) |
| Mozilla Firefox Add-ons | [Install for Firefox](https://addons.mozilla.org/en-US/firefox/addon/smartclip/) |
| Best Web Clippers Comparison | [SmartClip vs Notion, Obsidian, Readwise & Raindrop](https://smartclip.app/en/compare/best-web-clippers) |
| Help & Full FAQ | [smartclip.app/en/help](https://smartclip.app/en/help) |
| Changelog | [smartclip.app/en/changelog](https://smartclip.app/en/changelog) |
| AI / LLM Index (`llms.txt`) | [smartclip.app/llms.txt](https://smartclip.app/llms.txt) |
| X (Twitter) | [@maike_93z](https://x.com/maike_93z) |

---

## Core Capabilities (v2.2)

- **Clean Content Extraction**: Strips ads, sidebars, comments, and tracking pixels while preserving headings, lists, code blocks, and tables — with dedicated adapters for WeChat Official Account articles, Bilibili, and YouTube.
- **5-Color Radial Highlighter & Inline AI**: Highlight any text on the page, auto-restore highlights on revisit, and trigger a streaming AI popover for translation, explanation, or summarization.
- **Video Bilingual Subtitles & Vocabulary**: Docks bilingual transcripts beside supported video players (Bilibili / YouTube) and captures unfamiliar terms into a vocabulary list (flashcards in Lite).
- **Reader Preview & AI Outline**: Distraction-free reader modal with Warm Paper, White, and Dark themes, front-matter property inspector, AI outline generation, and image/PDF export (Lite).
- **BYOK Multi-Provider AI Chat**: Bring your own API key (OpenAI, Anthropic, Google, DeepSeek) or run 100% offline with local **Ollama** — requests go straight from your browser to the model provider.
- **Anti-Hotlink Image Backup**: Downloads protected images at clip time and uploads them to your own **AWS S3**, **Aliyun OSS**, **Tencent COS**, or **Cloudinary** bucket so clips survive page deletion.
- **Batch Queue & Offline Resilience**: Multi-tab / CSV batch saving with automatic rate-limit retries and local queue persistence across restarts or offline periods.
- **MCP Agent Bridge (Pro)**: Exposes authenticated browser tabs over local WebSocket **MCP (Model Context Protocol)** so **Claude Code**, **Cursor**, and **Gemini CLI** can read clean Markdown and file clips automatically.

---

## 18 Save Destinations & Deep-Dive Guides

| Category | Supported Destinations | Dedicated Guide |
|---|---|---|
| **Cloud & Team Docs** | Notion, FlowUs, Feishu Docs (飞书文档), Yuque (语雀), Wolai, GitHub | [Notion Guide](https://smartclip.app/en/notion-web-clipper) · [Feishu Guide](https://smartclip.app/en/feishu-web-clipper) |
| **Local & Bi-directional Vaults** | Obsidian, SiYuan (思源笔记), Logseq (`smartclip/` tree), Joplin | [Obsidian Guide](https://smartclip.app/en/obsidian-web-clipper) · [SiYuan Guide](https://smartclip.app/en/siyuan-web-clipper) |
| **Cards & Quick Notes** | Flomo (Webhook), Memos, Dedao Brain (得到大脑) | [Flomo Guide](https://smartclip.app/en/flomo-web-clipper) |
| **Object Storage & Formats** | AWS S3 / Aliyun OSS / Tencent COS Sync, Markdown (`.md`), Clean Clipboard | [WeChat to Markdown](https://smartclip.app/en/wechat-to-markdown) |
| **AI Coding Agents** | Claude Code, Cursor, Gemini CLI via WebSocket MCP | [MCP Browser Extension Guide](https://smartclip.app/en/mcp-browser-extension) |

---

## Repository Contents

```text
smartclip-repo/
├── templates/           # Community site extraction templates (CSS/DOM selectors)
│   ├── templates.json   # Registry index of available site templates
│   ├── tietu.json       # WeChat Official Account (*.mp.weixin.qq.com)
│   ├── zhihu01.json     # Zhihu Column (*.zhuanlan.zhihu.com)
│   ├── zhihu02.json     # Zhihu Q&A — first answer (*.zhihu.com)
│   └── zhihu03.json     # Zhihu Q&A — special layout (*.zhihu.com)
├── prompts/             # Reusable AI prompt presets for SmartClip
│   ├── prompts.json     # Prompt registry index
│   └── recommendation.md
└── docs/                # Documentation assets
```

### Templates (`templates/`)

Indexed by [`templates/templates.json`](./templates/templates.json):

| ID | Name | Pattern | File |
|---|---|---|---|
| `tietu` | 贴图 (WeChat) | `*.mp.weixin.qq.com` | [`templates/tietu.json`](./templates/tietu.json) |
| `zhihu01` | 知乎专栏 | `*.zhuanlan.zhihu.com` | [`templates/zhihu01.json`](./templates/zhihu01.json) |
| `zhihu02` | 知乎问答取第一个 | `*.zhihu.com` | [`templates/zhihu02.json`](./templates/zhihu02.json) |
| `zhihu03` | 知乎问答特殊场景 | `*.zhihu.com` | [`templates/zhihu03.json`](./templates/zhihu03.json) |

### Prompts (`prompts/`)

Indexed by [`prompts/prompts.json`](./prompts/prompts.json):

| Name | Scope | File |
|---|---|---|
| 推荐产品 | `content` | [`prompts/recommendation.md`](./prompts/recommendation.md) |

---

## Contributing Templates & Prompts

Contributions via Pull Request are welcome!

### 1. Contribute a Site Template

1. Add a new JSON file under `templates/<template-id>.json` following the schema used in [`templates/zhihu01.json`](./templates/zhihu01.json):
   - `id`, `name`, `pattern` (URL glob such as `*.example.com`), `version`, `enabled`, `priority`
   - `titleSelector`, `authorSelector`
   - `filter.include` / `filter.exclude` selector arrays
2. Register the template in [`templates/templates.json`](./templates/templates.json) with `{ "id", "name", "file", "pattern" }`.
3. Validate JSON formatting and submit a Pull Request describing the target site and tested URLs.

### 2. Contribute an AI Prompt

1. Add your Markdown prompt file under `prompts/<prompt-name>.md`.
2. Register `{ "file", "name", "scope" }` inside [`prompts/prompts.json`](./prompts/prompts.json).
3. Open a Pull Request explaining the intended reading or summarization workflow.

---

## Pricing & Privacy Overview

All paid SmartClip plans are **one-time purchases** — no subscriptions or automatic renewals.

- **Free ($0 forever)**: Full single-article clipping to one default destination, built-in templates, BYOK AI chat/summary/translation (supports offline Ollama), 5-color highlights, selection capture, user-configured image upload (S3 / OSS / COS / Cloudinary), reader preview & AI outline, and vocabulary annotation.
- **Lite (One-time buyout)**: Everything in Free + save to multiple notes apps at once (pick target at clip time) + unlimited CSV batch saving + unlimited custom templates + export reader preview as image or PDF + vocabulary flashcards.
- **Pro (One-time buyout)**: Everything in Lite + **MCP Agent integration** (Claude Code, Cursor, Gemini CLI) + additional batch saving modes (such as tweet collections) + all future features (cross-app migration, AI workflows) + priority support.

**Privacy & Local-First Security**: Clipped content is written directly from your browser to your chosen notes app without passing through SmartClip servers. API keys and storage credentials are encrypted locally using **AES-GCM**, and choosing **Ollama** keeps all AI processing 100% offline on your machine.
