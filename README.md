# 深入理解 AI Agent：设计原理与工程实践

**Agent = LLM + 上下文 + 工具**——本书围绕这个核心公式，用 10 章把 AI Agent 从原理讲到工程实战。全书正文、配图、**92 个配套实验**全部开源，欢迎亲手把实验跑一遍。

中文正文源码位于 [`book/`](book/)，配套实验代码在 [`chapter1/`](chapter1/) ~ [`chapter10/`](chapter10/)。

## 📑 内容速览（第 1–10 章）

全书围绕核心公式 **Agent = LLM + 上下文 + 工具** 展开，十章层层递进：

| 章 | 主题 | 一句话核心 | 正文 | 代码 |
| :--: | --- | --- | :--: | :--: |
| 1 | 🚀 **Agent 基础知识** | **Agent = LLM + 上下文 + 工具**；Harness 工程才是竞争力 | [读](book/chapter1.md) | [4](chapter1/README.md) |
| 2 | 🎯 **上下文工程** | 上下文决定能力上限：KV Cache、提示工程、Agent Skills、上下文压缩 | [读](book/chapter2.md) | [9](chapter2/README.md) |
| 3 | 📚 **用户记忆和知识库** | 跨会话记住用户、接入外部知识：用户记忆、RAG、结构化索引、知识图谱 | [读](book/chapter3.md) | [13](chapter3/README.md) |
| 4 | 🛠️ **工具** | 工具是 Agent 的双手：MCP 协议、感知/执行/协作三类工具、事件驱动异步 Agent、主动工具发现 | [读](book/chapter4.md) | [7](chapter4/README.md) |
| 5 | 💻 **Coding Agent 与代码生成** | 代码是「能创造新工具的工具」，生产级 Coding Agent 全景 | [读](book/chapter5.md) | [12](chapter5/README.md) |
| 6 | 🎯 **Agent 的评估** | 把表现变成可比较信号：评估环境、指标、统计显著性、评估驱动选型 | [读](book/chapter6.md) | [11](chapter6/README.md) |
| 7 | 🧠 **模型后训练** | 预训练/SFT/RL 三阶段：何时选 SFT、何时选 RL，工具调用内化、样本效率 | [读](book/chapter7.md) | [16](chapter7/README.md) |
| 8 | 🔄 **Agent 的自我进化** | 不改权重也能成长：经验学习、从工具使用者到创造者 | [读](book/chapter8.md) | [6](chapter8/README.md) |
| 9 | 🎙️ **多模态与实时交互** | 从文本扩展到语音、GUI、物理世界：语音三范式、Computer Use、机器人 | [读](book/chapter9.md) | [7](chapter9/README.md) |
| 10 | 🤝 **多 Agent 协作** | 群体智能高于个体：协作框架、上下文共享/隔离、涌现的「Agent 社会」 | [读](book/chapter10.md) | [7](chapter10/README.md) |

> 💡 **读** = 在 GitHub 网页直接读章节正文（markdown）；**N** = 该章配套项目数，点击查看代码。项目类型说明（✅ 可运行 / 📖 复现 / 🚧 设计）见各章 README。
>
> 📚 如何高效阅读本书？详见 **[学习建议](docs/zh-CN/LEARNING.md)**（核心理念、学习路径、难度分级、实践建议）。

## 🔑 API 密钥

建议申请下面几个平台的 API Key 方便学习。模型选型可参考 [这篇指南](https://01.me/2025/07/llm-api-setup/)。

| 平台 | 链接 | 特色 | 访问节点 |
| --- | --- | --- | --- |
| **Kimi**（月之暗面） | <https://platform.moonshot.cn/> | Kimi 系列，Coding、Agent 能力强 | 中国大陆 |
| **智谱 GLM** | <https://open.bigmodel.cn/> | GLM-5.2 等，Coding、Agent 能力强 | 中国大陆 |
| **Siliconflow** | <https://siliconflow.cn/> | 各种开源模型（DeepSeek、Qwen 等），中国大陆访问速度快 | 中国大陆 |
| **DeepSeek** | <https://platform.deepseek.com/> | DeepSeek 官方 API | 全球 + 中国大陆 |
| **Krill AI** | [www.krill-ai.com](https://www.krill-ai.com/register?invite=Q8D3L35725) | 一站式访问全球及国内主流模型（OpenAI、Claude、Gemini、Grok、Kimi、GLM、DeepSeek、Qwen、Minimax） | 全球 + 中国大陆 |
| **OpenRouter** | <https://openrouter.ai/> | 一站式访问全球及国内主流模型（GPT、Claude、Gemini、Kimi、GLM、DeepSeek、Qwen 等） | 全球 |

## 📦 附录 · 外部仓库获取

第 6、7、9、10 章的评测基准、训练框架、机器人平台等 19 个外部仓库**未内置**（出于体积与版权），需要自行克隆到对应目录。

### 一键克隆脚本

<details>
<summary><b>🔧 展开克隆命令</b>（共 19 个外部仓库）</summary>

```bash
# 第 6 章 · 评测基准
git clone https://github.com/google-research/android_world.git         chapter6/android_world
git clone https://huggingface.co/datasets/gaia-benchmark/GAIA          chapter6/GAIA
git clone https://github.com/xlang-ai/OSWorld.git                      chapter6/OSWorld
git clone https://github.com/SWE-bench/SWE-bench.git                   chapter6/SWE-bench
git clone https://github.com/sierra-research/tau2-bench.git            chapter6/tau2-bench
git clone https://github.com/laude-institute/terminal-bench.git        chapter6/terminal-bench

# 第 7 章 · 训练框架（bojieli/* 为本书适配的分支）
git clone https://github.com/bojieli/minimind.git                      chapter7/MiniMind-pretrain/minimind      # 实验 7-3 从零训 LLM
git clone https://github.com/bojieli/minimind-v.git                    chapter7/MiniMind-pretrain/minimind-v    # 实验 7-4 从零训 VLM（投影层）
git clone https://github.com/bojieli/AdaptThink.git                    chapter7/AdaptThink-original
git clone https://github.com/bojieli/AWorld.git                        chapter7/AWorld
git clone https://github.com/bojieli/SFTvsRL.git                       chapter7/SFTvsRL
git clone https://github.com/bojieli/verl.git                          chapter7/verl
git clone https://github.com/thinking-machines-lab/tinker-cookbook.git chapter7/tinker-cookbook
git clone https://github.com/19PINE-AI/rlvp.git                        chapter7/RLVP/rlvp                       # 实验 7-14 RLVP 论文代码
git clone https://github.com/PRIME-RL/SimpleVLA-RL.git                 chapter7/SimpleVLA-RL/SimpleVLA-RL       # 实验 7-13 视觉-语言-动作 RL

# 第 9 章 · 浏览器自动化与 Claude 示例
git clone https://github.com/browser-use/browser-use.git               chapter9/browser-use
git clone https://github.com/anthropics/claude-quickstarts.git         chapter9/claude-quickstarts

# 第 10 章 · 双 Agent 架构（已独立为 TalkAct 项目）+ 斯坦福 AI 小镇
git clone https://github.com/19PINE-AI/TalkAct.git                     chapter10/use-computer-while-calling
git clone https://github.com/joonspk-research/generative_agents.git    chapter10/generative_agents             # 实验 10-7 斯坦福 AI 小镇
```

> 各项目 README 如标注了特定 commit，请按说明 `git checkout` 到对应版本以保证复现一致。第 10 章 `use-computer-while-calling` 已发展为独立维护的 [19PINE-AI/TalkAct](https://github.com/19PINE-AI/TalkAct)，本仓库不内置该目录，用上面的克隆命令获取。

</details>

### 其它复现路径

下面这些实验无专属 clone 命令，但有特定的复现方式：

| 实验 | 类型 | 说明 |
| --- | :--: | --- |
| 6-2 / 6-3 / 6-4 / 6-9 | 📝 读者练习 | 人肉基准、记忆评估、JSON Cards vs RAG、记忆选型——改造复用第 3 章 `user-memory` / `user-memory-evaluation` / `contextual-retrieval` |
| 5-12 | 📝 读者练习 | 能创造 Agent 的 Agent——基于 `chapter5/coding-agent` 自举扩展 |
| 7-8 | 📝 读者练习 | Prompt 蒸馏——落地实现见 `chapter8/prompt-distillation`（跨章复用） |
| 7-9 | 📝 读者练习 | CoT 蒸馏 `[扩展]`——配套实现见 `chapter7/cot-distillation`（含 SFT 数据生成与规则验证器） |
| 6-11 | 🤖 仿真评估 | OpenVLA + RoboTwin2——VLA 训练/环境依赖见 `chapter7/SimpleVLA-RL` 的 README |
| 9-8 / 9-9 | 🔧 真实硬件 | XLeRobot 遥操作与 LLM Agent 控制——需 SO-100 机械臂，[Teleop](https://xlerobot.readthedocs.io/en/latest/software/getting_started/XLeRobot_teleop.html) · [LLM Agent](https://xlerobot.readthedocs.io/en/latest/software/getting_started/LLM_agent.html) |
| 9-10 | 🔧 真实硬件 | RGB 零样本 Sim2Real 抓取——[`StoneT2000/lerobot-sim2real`](https://github.com/StoneT2000/lerobot-sim2real)（仿真可纯 GPU，部署需 SO-100） |

