# MyAIRecord · 我的个人 AI 档案

让新会话中的 AI 了解我的学习、目标、项目和协作要求，减少重复解释，并保存可核查的经验。

本版汇总了三份可访问的历史，覆盖范围与限制分别见对应文档：

1. **历史聊天逐轮摘要**（S 系列）：2026-11-24 读取工具列出的 49 个其他聊天、204 个轮次，覆盖 11-06 至 11-24，见 [SOURCES.md](SOURCES.md)。
2. **全量清单复盘**（133 场）：同日把会话清单分页读到末尾，日期从 2025-01-31 到 2026-11-24，按年月与领域归纳，见 [CONVERSATIONS.md](CONVERSATIONS.md) 与 [TOPICS.md](TOPICS.md)。
3. **本机桌面会话**（L 系列）：这台电脑上 DeepSeek Harness 桌面版的 35 个会话文件（21 个有真实对话），覆盖 10-23 至 11-24，含提交号、指标与文件级记录，见 [conversations/README.md](conversations/README.md)。

这不是全账号逐字导出，附件正文未读取，也不会让所有 AI 自动拥有长期记忆。

## 使用方法

1. 新会话提供 [PROFILE.md](PROFILE.md)，粘贴 [启动提示词](prompts/start.md)。
2. 做具体任务时再提供对应 [项目](projects/README.md)、[学习记录](records/learning.md) 或相关会话记录。
3. 任务结束用 [更新提示词](prompts/update.md)整理增量，保留来源和日期。
4. 定期纠正过期内容，保持核心档案简短。

## 档案导航

| 内容 | 文件 |
| --- | --- |
| 核心认识、协作要求与项目事实 | [PROFILE.md](PROFILE.md) |
| 英语、编程、数学与模型学习 | [records/learning.md](records/learning.md) |
| 写作、代码与交付方式 | [records/work-style.md](records/work-style.md) |
| 兴趣、工具与阶段计划 | [records/interests-and-plans.md](records/interests-and-plans.md) |
| 跨年主题综述：事实、要求与未结事项 | [TOPICS.md](TOPICS.md) |
| 133 场对话的时间线与主题分布 | [CONVERSATIONS.md](CONVERSATIONS.md) |
| 本机会话的逐条记录（21 个会话） | [conversations/sessions.md](conversations/sessions.md) |
| 本机会话的提取方法与边界 | [conversations/README.md](conversations/README.md) |
| 十三个项目的职责、进展、待核实事项 | [projects/README.md](projects/README.md) |
| AI 使用方式、能力边界与历史纠错 | [AI_COLLABORATION.md](AI_COLLABORATION.md) |
| 来源索引、读取数量与覆盖限制 | [SOURCES.md](SOURCES.md) |
| 公开范围与隐私排除 | [PRIVACY_AND_SCOPE.md](PRIVACY_AND_SCOPE.md) |
| 建设方法与外部调研 | [BUILD_GUIDE.md](BUILD_GUIDE.md) |
| 启动／更新提示词 | [start](prompts/start.md) · [update](prompts/update.md) |
| 新项目模板与变更记录 | [template](templates/project.md) · [changelog](CHANGELOG.md) |

## 三份记录怎么配合用

- 想了解"我是谁、怎么协作、在学什么"：读 PROFILE 与 records/。
- 想知道某事发生在哪个阶段：查 CONVERSATIONS.md（年月 + 主题）和 TOPICS.md（领域综述）。
- 想接着做某个具体技术任务：读 projects/ 里对应项目的"本机会话技术记录"一节，再读 conversations/sessions.md 那一段，里面有提交号、指标和当时的判断。
- 互相冲突时，以日期更近、且有文件或命令输出支撑的为准；无法判断就标"待确认"。

## 读档原则

用户明确表达、观察归纳、历史助手报告、建议和未知项分别标注。这里记录"曾说过／曾做过"的依据，不把当时的阶段状态变成永久画像，也不把旧助手报告当作新验证。

本仓库公开，只保存适合公开的摘要。未上传原始聊天、私人附件、身份、成绩、财务、账户、私人生活与他人信息。具体规则见公开范围文档。
