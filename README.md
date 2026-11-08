# project-ops-builder

为代码仓库建立和维护渐进式 agent 指令、项目运维 Skill 与按任务读取的项目文档。

入口保留必要约束和任务路由；详细契约放在对应文档；可复用操作由项目 Skill 与必要脚本承载。简单项目可以保持一个入口。

## 使用

在支持本地 Skills、具备相应仓库读写能力的 agent 中安装本仓库后，在目标项目提出任务：

```text
使用 project-ops-builder，为当前项目建立按任务读取的 agent 入口和运维 Skill，复用现有文档与脚本。
```

```text
使用 project-ops-builder，精简当前 AGENTS.md，保留原有约束，为专项内容补充明确的读取触发条件。
```

```text
本次启动命令已调整，更新受影响的项目 Skill 和文档引用。
```

前两类任务按需读取架构参考或模板；已知命令和路径的小修直接更新所属位置。生成的项目入口包含维护约定，使后续任务能够同步修正受影响的说明。

## 安装与更新

将本仓库完整安装到当前 agent 支持的 Skill 发现位置，保留 `SKILL.md` 与 `references/` 的相对结构。发现位置以目标客户端的当前文档和配置为准；也可以将仓库链接交给 agent，要求它完成安装。

需要共用一份本地来源时，在发现目录建立指向仓库的目录链接；Windows 可使用目录联接。使用复制安装时，更新完整目录。安装或更新后检查实际发现路径与目标内容，再通过客户端确认加载。

本 Skill 的授权来自当前任务。项目运行、验证、提交、推送和部署遵循各自已有要求与授权。通用个人偏好保留在用户全局指令中。

## 内容

| 文件 | 用途 |
|---|---|
| [SKILL.md](SKILL.md) | 工作选择、按任务取证及局部维护 |
| [渐进式架构](references/agent-architecture.md) | 规则归属、读取触发、文档约定与跨工具接入 |
| [项目 Skill 模板](references/project-skill-template.md) | 项目运维 Skill 的编写、操作边界和发现接入 |

设计参考：[agents-progressive-disclosure](https://github.com/Caph-dev/agents-progressive-disclosure)、[claude-md-optimizer](https://github.com/wrsmith108/claude-md-optimizer)。采用按内容分类、必要摘要与条件链接的方法，迁移时核对约束含义。
