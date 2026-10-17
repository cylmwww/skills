# skills

个人在项目学习、文档整理、清理维护和面试准备中沉淀的 Codex skills。每项技能包含可复用的工作说明，必要时附带参考文档或界面元数据。

本仓库只整理个人任务中形成和迭代的技能，不收录从外部下载的技能集合。技能由人工与 AI 协作整理，使用时仍需结合实际材料、当前权限和用户要求判断。

## 技能目录

| 技能 | 用途 | 入口 |
| --- | --- | --- |
| architecture-learning-plan | 围绕真实项目的整体架构、工程问题和设计取舍制定学习计划 | [SKILL.md](.agents/skills/architecture-learning-plan/SKILL.md) |
| project-docs-release | 面向首次读者整理 README 与使用文档，核对能力、链接及 Git 交付范围 | [SKILL.md](.agents/skills/project-docs-release/SKILL.md) |
| project-safe-cleanup | 核对用途、依赖和运行状态后，清理明确安全的项目残留 | [SKILL.md](.agents/skills/project-safe-cleanup/SKILL.md) |
| interview-practice | 围绕简历项目训练、追问、复盘与复测，使用本地作答证据安排重点 | [SKILL.md](.agents/skills/interview-practice/SKILL.md) |

## 使用方式

所有技能位于 `.agents/skills/<技能名>/`，每个目录的 `SKILL.md` 是入口。在当前工作区使用 Codex 时，可显式指定技能，例如：

> 使用 $architecture-learning-plan，为我指定的项目制定以架构和设计取舍为核心的学习计划。

> 使用 $project-docs-release，核对当前实现，面向首次读者整理项目 README，并检查链接。

> 使用 $project-safe-cleanup，先盘点项目残留和依赖，只给出候选清单，暂不执行删除。

> 使用 $interview-practice。今天有 30 分钟，日常训练模式。我会提供简历和项目源码路径，先建立考查范围，再逐题训练并保存实际问答。

若需要在其他项目中使用，将所需技能目录复制到该项目的 `.agents/skills/`。保留该技能的附带文件，例如 `agents/` 和 `references/`。已经存在同名技能时先比较版本，不直接覆盖已有修改。

如果选择列表尚未发现技能，可重新打开 Codex，或直接指定读取对应的 `SKILL.md` 并按其执行。

## 内容组织

```text
.agents/skills/
  architecture-learning-plan/
    SKILL.md
    agents/openai.yaml
  project-docs-release/
    SKILL.md
    agents/openai.yaml
    references/public-docs-rewrite.md
  project-safe-cleanup/
    SKILL.md
    agents/openai.yaml
  interview-practice/
    SKILL.md
```

本仓库提供技能说明和参考资源，无需启动独立应用，也未实现 MCP 服务或运行脚本。

## 个人数据与验证范围

个人简历、项目私有材料、面试复盘、训练历史和本机配置由使用者自行提供；这些数据不随技能分发。现有本地材料保留在工作区，并通过 `.gitignore` 排除。

`interview-practice` 在实际开始训练时初始化或读取用户工作区中的记录；历史复盘作为考查线索，不自动转化为掌握证据。项目事实和真实实验结果需要对应材料支持。

技能文件的格式与引用检查只能说明结构可用，不能证明每次模型判断正确或训练效果已得到验证。具体权限、输入要求、工作流程和限制见各技能入口。