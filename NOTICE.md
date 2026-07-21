# 来源与归属

本工具基于 Simon Willison 的开源项目 **LLM cliché highlighter** 的产品思路和交互模式开发：

- 上游文件：https://github.com/simonw/tools/blob/main/llm-cliche-highlighter.html
- 上游仓库：https://github.com/simonw/tools
- 上游作者：Simon Willison 及该仓库贡献者
- 上游许可证：Apache License 2.0

本目录中的 `LICENSE` 保留 Apache License 2.0 全文。本工具不是对上游作品“完全原创”的表述；中文版在其单文件高亮器思路上增加了中文规则体系、风险分级、命中详情、个人规则、报告导出、自测试和响应式中文界面。

中文规则由项目作者根据实际中文写作场景整理。自动化仅覆盖适合稳定字面或句式匹配的规则；需要语义、事实、节奏或全文结构判断的规则未被伪装成确定命中。

同目录的 `ai-flavor-cleaner-zh` Skill 在方法上参考了 Wikipedia “Signs of AI writing”、`blader/humanizer` 和 `hardikpandya/stop-slop`。本项目重新组织了工作流和规则表达，并加入“不补写原文没有的信息”等约束，不将这些参考内容表述为完全原创。
