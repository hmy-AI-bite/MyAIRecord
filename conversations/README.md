# 对话归档索引

这里记录我与 AI 的实际对话：做过什么、结论是什么、还差什么。目的是在新会话里少解释一遍，也方便回头核对当时的判断。

## 数据范围

- 来源：本机 DeepSeek Harness（DSH Desktop）的会话存储，路径形如 `sessions/<工作目录>/<会话>/session.v4.jsonl.zstd`。只读取本机文件，没有访问云端账号。
- 扫描日期：2026-11-24。
- 覆盖：35 个会话文件，其中 **21 个含真实对话**，14 个是空会话或只有系统消息。
- 时间跨度：2026-10-23 至 2026-11-24，共 13 个有对话的日期。最早的文件是 2026-09-28，但那天没有真实对话。
- 规模：179 条用户消息、418 条助手回复，分布在 11 个工作目录。
- 时区：下文日期均为 UTC+8。

## 提取方法

1. 会话文件是分帧追加的 zstd（一个文件里有几百个独立帧），普通一次性解压只能拿到开头一条，需要按 zstd 帧头逐帧解压后再拼接。
2. 逐行解析事件，取 `session`（会话元信息）、`session/title`、`user/message`、`assistant/message`。
3. 用户消息按 `source.kind` 过滤：只有 `user` 是真实输入；`runtime-context`、`skill-catalog` 等是系统注入的上下文，不计入。
4. 只保留摘要和结论，不保留原文；工具调用的参数和输出不入库。

## 边界

- 与 [README](../README.md) 提到的另外两份来源不同：S 系列（逐轮摘要，11-06 起）和 [CONVERSATIONS.md](../CONVERSATIONS.md)（133 场清单的时间线）偏行为、职责与阶段脉络，这里偏工程细节与提交记录，三份可互为校验。
- 只覆盖这台电脑上 DSH Desktop 的会话。Claude、Copilot、Codex、豆包和网页版的对话没有读取，因此这里的记录不是全部聊天，只是可离线核对的那一部分。
- 姓名、学号、学校、微信文件路径等可识别信息已删除或不写入。原文里出现过的身份信息不复制进仓库。
- 对话里的 AI 结论是当时的输出，不等于已经验证的事实；数字和判断以对应项目文件的说明为准。

## 索引

| 时间 | 主题 | 主要产出 | 详见 |
| --- | --- | --- | --- |
| 2026-10-23 ~ 10-25 | 文物数据集流水线审查、SAM2 接入 Label Studio | 规范化的数据层、一键脚本、SAM2 预标注 223 个候选 | [文物纹样](../projects/heritage.md) · [纹样数据集](../projects/pattern-dataset.md) |
| 2026-10-24 | Windows 桌宠：喂食、抚摸、好感度、侧边悬挂 | 可运行的桌宠 + 13 段动画 + 自检脚本 | [桌宠](../projects/deskpet.md) |
| 2026-11-01 | 人工智能数学基础实验二：矩阵相似度电影推荐 | 教学代码 + 14 页实验报告（DOCX/PDF） | [AI 数学课程作业](../projects/ai-math-coursework.md) |
| 2026-11-01 ~ 11-04 | Pattern Studio 仓库梳理、UI 骨架与玻璃主题 | React 骨架、handover 文档、`205566c` 主题提交 | [文物纹样](../projects/heritage.md) · [工作台](../projects/pattern-studio.md) |
| 2026-11-02 | 机械硬盘写入权限、TypeWords 安装与雅思词库 | 桌面一键启动器、3575 词雅思词库 | [本机环境与网络](../projects/dev-environment.md) |
| 2026-11-04 ~ 11-22 | DSH Desktop 维修、插件与网络排障 | 定位 hosts 污染与路由抢占，恢复校园网 | [本机环境与网络](../projects/dev-environment.md) |
| 2026-11-05 ~ 11-13 | 自行车越界检测（YOLO + 掩膜 + 场景匹配） | 新仓库、335 框数据集、九章报告 + 12 页 PPT 大纲 | [自行车越界检测](../projects/bicycle.md) |
| 2026-11-06 | 研读 rhine-lock 前后端源码 | 26 个文件的学习笔记（含两处纠正） | [前端设计工具包](../projects/frontend-design-kit.md) |
| 2026-11-06 | frontend-design-kit v2 升级 | 六阶段改造、`4103fae`、三条负向测试 | [前端设计工具包](../projects/frontend-design-kit.md) |
| 2026-11-06 ~ 11-14 | Pattern Studio 转场、历史数据页、60 秒演示视频 | 一镜到底演示片、抽屉侧栏、`hmy` 分支同步 | [Pattern Studio](../projects/heritage.md) |
| 2026-11-15 | 阶段成果总结、挑战杯申报书重建 | 按"新项目、无成果"口径的 5 页申报书 | [Pattern Studio](../projects/heritage.md) |
| 2026-11-18 ~ 11-19 | Java 课程设计：环境、README、两人分工、服务端收口 | `7b2b35b`、10 个 JUnit 通过 | [Java 课程设计](../projects/java.md) |
| 2026-11-20 | 德国英语授课 CS/AI 硕士检索与对照 | 2 主申 + 6 备选的两张表、7 页对照文档 | [留学申请](../projects/germany-application.md) |
| 2026-11-21 | 星环算力平台调度课程设计报告 | 6 页 DOCX、五张 Word 表格、96/100 迭代记录 | [星环课程设计](../projects/scheduler.md) |
| 2026-11-21 | C++ 代码习惯梳理与两道题 | 统一的代码版式 + 两篇题解 | [AI 数学课程作业](../projects/ai-math-coursework.md) |
| 2026-11-22 | 挑战杯申报书 v4 评分诊断 | 100 分自查表 + 10 个可改写切入点 | [Pattern Studio](../projects/heritage.md) |
| 2026-11-24 | 建立本档案（读取历史对话） | 本目录与 projects/ | 本节 |

逐条记录见 [sessions.md](sessions.md)。
