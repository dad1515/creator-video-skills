# Creator Video Skills

面向个人创作者的一组可复用 Agent Skills。当前首个模块是 `content-positioning`：在生成选题、口播稿和视频之前，先建立可验证、可复用的内容定位。

> Status: `v0.1-alpha`. The workflow is usable, but its schemas may still change before the website reaches v1.0.

## Content Positioning

`content-positioning` 会：

- 用不超过 6-8 个高价值问题收集创作者信息；
- 解释每个问题为什么与定位有关；
- 生成三套具有实质差异的定位策略；
- 对受众、可信度、转变结果、差异化和商业路径进行评分；
- 保存私人定位档案，并可生成脱敏的公开模板；
- 向后续选题、口播稿、配音和视频模块提供统一上下文。

V1 只服务个人知识、技能和专业服务创作者，不处理企业品牌、多账号矩阵或团队审批。

## Install

```bash
npx skills add dad1515/creator-video-skills --skill content-positioning
```

也可以将 `skills/content-positioning/` 复制到支持 Agent Skills 的客户端目录。

## Use

```text
$content-positioning 帮我确定个人账号的内容定位
```

如果用户提供的信息已经完整，skill 会直接生成三套策略；如果信息不足，则进入带进度提示的定位访谈。

## Repository Structure

```text
creator-video-skills/
|-- skills/
|   `-- content-positioning/
|       |-- SKILL.md
|       |-- agents/openai.yaml
|       `-- references/
|           |-- evaluation.md
|           `-- profile-schema.md
|-- examples/                 # Sanitized public templates
`-- tests/                    # Forward-test cases and release gates
```

## Privacy Model

私人定位档案与公开模板是两类不同数据：

- 私人档案包含身份、经历、证据、商业目标和内容边界，默认不公开。
- 公开模板只保留可复用的受众模型、策略结构、内容支柱和设置问题。
- 对外发布前必须展示脱敏结果并取得用户确认。
- 模板使用复制后编辑模式，使用者不会修改原模板。

仓库的 `.gitignore` 默认忽略 `positioning-profile.json` 和常见私密档案目录。

## Validation

下面的行业只是用于验证同一套流程能否根据不同用户回答动态生成定位，**不是内置分类、固定模板或支持范围限制**：

- AI 漫剧教学
- 数据分析知识教育
- 产后营养咨询
- 微缩模型兴趣社群
- 家庭烘焙课程

其中 AI 漫剧完成了真实对话验证；数据分析、产后营养和微缩模型完成了三方案生成测试；家庭烘焙只验证了信息不足时的追问行为。实际用户无需从这些行业中选择。

测试记录与发布门槛见 [`tests/positioning-cases.md`](tests/positioning-cases.md)。

## Website Integration

该 skill 是完整智能口播视频网站的第一个业务模块：

```text
content-positioning
  -> positioning-profile.json
  -> topic and narration generation
  -> voice and media generation
  -> intelligent editing
  -> video export
```

网站应把档案存入数据库，但继续遵守 `references/profile-schema.md` 定义的语义契约。

## License

MIT
