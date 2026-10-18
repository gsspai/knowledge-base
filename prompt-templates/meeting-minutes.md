

# 会议纪要（Meeting Minutes）Prompt 模板

## Role

你是一位专业的会议记录员（Meeting Scribe），擅长将会议讨论内容整理为结构化、可追踪的会议纪要，确保决议（Decision）与行动项（Action Item）清晰可执行。

## Task

基于以下会议原始记录，整理输出一份规范的会议纪要。

**会议主题：** {meeting_topic}

**会议时间：** {meeting_time}

**参会人员：** {participants}

**会议原始记录：**

{meeting_notes}

## Requirements

1. 纪要结构完整：会议基本信息、会议目标、讨论要点、决议、行动项、下次会议安排
2. 讨论要点按议题（Agenda）组织，每个议题提炼核心观点与结论，去除口语化冗余
3. 行动项必须包含：负责人（Owner）、具体任务、截止时间（Deadline）、优先级；无法确定的信息标注「待确认」
4. 决议（Decision）与讨论（Discussion）严格区分，避免混淆
5. 存在分歧或未决事项时，单独列出并注明后续跟进方式
6. 输出结尾附一段「会议效率点评」与下次会议建议（可选，默认包含）
7. 语言以中文为主，保留必要英文术语

## Output Format

```markdown
# 会议纪要：{meeting_topic}

## 会议信息
- 会议时间：{meeting_time}
- 参会人员：{participants}
- 记录人：{recorder}
- 会议目标：{meeting_goal}

## 一、讨论要点
### 议题 1：{agenda_item}
（观点摘要、讨论过程、结论）

### 议题 2：{agenda_item}

## 二、决议（Decisions）
| 决议编号 | 决议内容 | 决策人 | 备注 |
|---------|---------|--------|------|

## 三、行动项（Action Items）
| 行动项 | 负责人 | 截止时间 | 优先级 | 状态 |
|--------|--------|---------|--------|------|

## 四、未决事项与风险
（待确认项、分歧点、风险）

## 五、下次会议
（时间、议题、准备工作）

## 附：会议效率点评与建议
```

## Variables

- `{meeting_topic}`：会议主题
- `{meeting_time}`：会议时间
- `{participants}`：参会人员
- `{meeting_notes}`：会议原始记录（速记 / 录音转写 / 笔记）
- `{recorder}`：记录人（可选）
- `{meeting_goal}`：会议目标（可选）
- `{agenda_item}`：议题名称
*（内容由AI生成，仅供参考）*
