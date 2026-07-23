# AGENTS.md

本仓库是 [bojieli/ai-agent-book](https://github.com/bojieli/ai-agent-book)（《深入理解 AI Agent：设计原理与工程实践》）的个人学习副本，公开仓库地址 `chemark/ai-agent-book`。只保留中文正文和配套实验代码，用于按章节学习 + 动手跑实验；文档站、多语言翻译、CI 发布流程已清理，不再维护。

## 目录约定

- `book/chapter1.md` ~ `chapter10.md`：正文，只读参考，不改动
- `chapter1/` ~ `chapter10/`：配套实验代码，按 `chapterN/项目名/` 组织，每个项目自带 README、requirements.txt、env.example
- `docs/zh-CN/LEARNING.md`：学习路径建议
- `extras/agent-lab/`：第 1 章示例用的原始 Agent 轨迹数据（JSON）
- `cursor-chats/`：作者开发过程记录，只读参考，不要改动或删除

## Git 约定

- `origin` = 自己的仓库（`chemark/ai-agent-book`），日常 push 到这里
- `upstream` = 原书仓库（`bojieli/ai-agent-book`），想同步作者更新时 `git fetch upstream && git merge upstream/main`
- 推送优先用 SSH（`git@github.com:...`）：HTTPS 大包体在当前网络环境下容易被连接重置
- 浅克隆（`--depth 1`）无法直接 push 到新仓库，先 `git fetch --unshallow` 补全历史

## 跑实验

- 每个 `chapterN/项目名/` 目录独立，先看该项目的 README，按其 `requirements.txt` 装依赖、`env.example` 配 API Key
- `.env` 已被顶层 `.gitignore` 的 `.*` 规则排除，不会误提交密钥；`env.example` 会被提交，不要往里面填真实 Key
- 优先选不需要 API Key 就能跑的部分（各项目 README 会标注），需要 Key 的部分再决定用哪家平台（见 `README.md` 「API 密钥」表）

## 修改原则

- `book/` 和 `chapter*/` 是原书内容，不是自己的项目——除非明确要修 bug 或做练习，否则不做无关重构
- 大范围改动（比如又要清理一批文件）先说清楚要删什么、为什么，确认后再动手
