# dsh-superagent

[English](README.md) | 简体中文

> **本项目仅为研究原型，供参考使用，并非 DeepSeek 官方产品。** 代码源于团队日常开发，其中相当一部分工程工作由编程智能体完成。请将其视为研究代码，而非可直接用于生产环境的软件。项目可能仍有缺陷，代码风格和工程实践也可能不一致。请先审查并按需调整，再用于自己的环境。
>
> 为了公开发布，我们对项目做了调整，因此它与内部版本以及论文 *Exploring Super-agent Design: Towards a More Autonomous Agent System* 中描述的实现并不完全相同。论文中讨论的部分设计属于未来开发方向，尚未在此原型中实现。

dsh-superagent 是一个面向单个 GitHub 仓库的主动式编程智能体，以 bundle 形式供 [DeepSeek Harness](https://www.deepseek.com/en/harness/) 使用。它监听 GitHub，也可以选择监听飞书。当获准的用户向它分派任务时，它会创建工作项，在独立的智能体会话和目录中完成任务，并在原对话中回复，例如提交一个 Pull Request。Web 面板会展示哪些事项需要人工处理。

它也代表了一种与智能体协作的方式：**尽可能少地占用人的注意力，同时尽可能多地创造价值。** 能代表整个团队行动的智能体，也可能浪费整个团队的注意力。因此，它只会在收到请求或团队设定的规则允许时行动；只有在需要有人处理，或有人可以利用结果时才会发言。[docs/000-philosophy.md](docs/000-philosophy.md) 介绍了这一原则及其对操作者的要求。

## 安装与配置

配置步骤较多，可以让编程智能体陪你一起完成。向你的编程智能体发送：

> 阅读本仓库中的 SETUP.md，并和我一起配置 dsh-superagent。

它会一次询问一个简短问题，在汇总完整计划后再开始安装和配置。[SETUP.md](SETUP.md) 是配置流程的操作指南。

## 文档

请按编号顺序阅读文档；每篇文档只依赖此前介绍的内容。

- [000 理念](docs/000-philosophy.md)
- [001 领域模型](docs/001-domain.md)
- [002 授权](docs/002-authorization.md)
- [003 执行](docs/003-execution.md)
- [004 提示词](docs/004-prompts.md)
- [005 面板](docs/005-panel.md)
- [006 部署](docs/006-deployment.md)：手动安装、配置、升级与故障排查
- [007 架构](docs/007-architecture.md)
- [008 实用指南](docs/008-cookbook.md)：添加 Source

## 开发

运行 `pnpm check` 可依次执行类型检查、测试和构建。

## 许可证

[MIT 许可证](LICENSE)