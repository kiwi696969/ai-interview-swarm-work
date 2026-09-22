# Agent 办公实践：AI 面试协同团队实践

> 会话执行记录（WorkSwarm 多 Agent 协作）

## 部署
- 读取 https://gitcode.com/agent-best-practices/ai-interview-swarm.git
- 按「AI 面试天团 — 快速部署指南」配置 5 角色团队
- 创建 /var/interview_Lab（知识库）与 /var/interview_Log（日志）
- 修改 Skill 知识库路径为 /var/interview_Lab，输出目录为 /var/interview_Log
- 所有 Agent 模型统一使用当前主模型

## 面试任务
用户输入：我要面试
- 面试调度总控（Leader）：确定岗位为 Java 后端开发工程师，编排 DAG：
  通用聊天官（破冰）→ 技术面试官（4 题）→ HR 面试官（3 题）→ 人才测评专员（汇总报告）
- 各 Agent 按知识库题库顺序提问、按三级标准评分、落盘本地。

## 关键产出
interview_Log/面试报告.md：完整面试记录 + 技术/HR 评分 + 综合测评（3.95/5，建议进入下一轮）。

## 多 Agent 协作价值
- 每个 Agent 只做自己擅长的角色，避免单 AI 的 Prompt 膨胀与角色混乱；
- 技术评分与 HR 评分独立量化，消除人为偏见；
- 标准化提问 + 量化评分，可 7×24 随时面试。
