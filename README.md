# 中文 AI 味清理器

一个同时面向浏览器用户和 Agent 用户的中文 AI 写作清理项目。

## 两种使用方式

### 1. 离线检测器

双击打开 [`中文AI味检测器.html`](中文AI味检测器.html)，粘贴文本即可实时检查。它不联网、不调用模型、不上传文本，提供：

- 绝对禁用与高风险检查分级
- 命中句子、规则说明和处理建议
- 逐项规则开关
- 使用 `localStorage` 保存的个人规则
- Markdown 检查报告复制与导出
- 51 条内置规则和 8 项浏览器自测试

离线版只负责可靠检测，不执行可能改变原意的自动改写。

### 2. Agent Skill

使用 Codex 的一键安装命令：

```bash
npx skills add https://github.com/chiefcapitalhu/ai-flavor-cleaner-zh/tree/main/skill/ai-flavor-cleaner-zh -g -a codex -y
```

该命令需要本机已安装 Node.js。也可以手动将 [`skill/ai-flavor-cleaner-zh`](skill/ai-flavor-cleaner-zh) 目录安装到 Codex 的 skills 目录。安装后使用：

```text
使用 $ai-flavor-cleaner-zh 检查并改写下面的中文，保留事实和作者立场，不要添加原文没有的信息。
```

Skill 支持检查模式和改写模式。它由宿主 LLM 理解上下文，因此能处理语气、节奏、重复和全文结构；同时明确禁止补写来源、数据、案例和观点。

## 版本规划

- V1：离线规则检测器 + 可安装的 Agent Skill。
- V2：在网页中加入可选 API 配置、隐私说明、模型选择和全文改写。API 模式不会取代离线模式。

## 规则与边界

项目内置规则覆盖常见中文套话、高风险表达和结构信号。需要语义、事实或全文节奏判断的项目不会在离线版中伪装成确定命中。

## 来源与许可证

离线检测器基于 Simon Willison 的 [LLM cliché highlighter](https://github.com/simonw/tools/blob/main/llm-cliche-highlighter.html) 的单文件即时高亮思路开发。项目保留上游归属说明，并按 Apache License 2.0 提供。详见 [`NOTICE.md`](NOTICE.md) 和 [`LICENSE`](LICENSE)。
