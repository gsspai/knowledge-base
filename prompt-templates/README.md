# Prompt 模板库

本目录收录了一套可复用、结构化的 **Prompt 模板**，覆盖研发、产品、运营、行政等常见工作场景。每个模板采用统一的 `Role / Task / Requirements / Output Format` 结构化字段，可变部分使用 `{variable}` 占位符标注，方便直接套用与二次定制。

## 模板列表

| 模板 | 场景 | 适用对象 | 文件 |
|------|------|---------|------|
| 代码审查 Code Review | 审查代码质量、安全与性能，输出分级问题清单与修复建议 | 研发 / 技术负责人 | [code-review.md](code-review.md) |
| PRD 需求文档 | 将业务想法转化为结构完整的 PRD，含功能需求、验收标准、里程碑 | 产品经理 | [prd.md](prd.md) |
| 测试用例 Test Cases | 基于功能描述设计全覆盖测试用例，含需求追踪矩阵 | 测试工程师 | [test-cases.md](test-cases.md) |
| 竞品分析 Competitor Analysis | 系统分析竞品定位、功能、商业模式与优劣势，输出策略建议 | 产品 / 市场 / 运营 | [competitor-analysis.md](competitor-analysis.md) |
| 数据分析 Data Analysis | 基于数据完成指标拆解、趋势与异常分析，输出可执行结论 | 数据分析师 / 运营 | [data-analysis.md](data-analysis.md) |
| 邮件起草 Email Draft | 按目的、收件人关系与正式程度起草中英文商务邮件 | 全员 | [email-draft.md](email-draft.md) |
| 会议纪要 Meeting Minutes | 将会议记录整理为结构化纪要，含决议与行动项追踪 | 全员 | [meeting-minutes.md](meeting-minutes.md) |

## 模板结构说明

所有模板统一包含以下四个核心字段：

- **Role（角色）**：定义 AI 扮演的专业角色与能力边界，引导输出质量
- **Task（任务）**：明确要完成的具体任务与输入材料
- **Requirements（要求）**：输出必须遵守的规则（结构、质量、约束条件）
- **Output Format（输出格式）**：规定结构化输出模板，便于直接落地使用

## 使用方法

1. **复制模板**：将对应 `.md` 文件内容复制到你的对话 / Prompt 编辑器中
2. **替换占位符**：将 `{variable}` 占位符替换为实际内容（如 `{code_snippet}`、`{meeting_notes}`）
3. **按需裁剪**：`Requirements` 与 `Output Format` 可按实际场景增删条目，保持结构一致即可
4. **二次定制**：如需调整语气或深度，可在 `Role` 或 `Requirements` 中追加约束（如「输出控制在 500 字内」「面向非技术读者」）

## 注意事项

- 模板默认以中文为主，保留必要英文术语；如需英文输出，在 `Task` 或 `Requirements` 中显式声明
- 涉及真实数据（代码、用户信息、财务数据）时，请先脱敏再输入
- 建议将高频使用、表现良好的模板沉淀回本目录，保持库持续演进
