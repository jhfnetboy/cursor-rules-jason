# Development flow and docs rules for AI vibe coding
This file will be include in claude.md, gemini.md and docs directory in project root.
This file create a rule for work flow and rules for all project development.
本文主要服务于独立的项目开发流程，从属于整体exploaration流程：设计、研究、项目（研发）、社区。
@ my-explaration/README.md，参考此文档获得全局上下文

## 目录结构

1. my-exploration 主目录，私有repo
2. 四个流程子目录
  - design 设计目录，从idea到solution
  - projects，vendor目录，以submodule方式添加独立的项目目录，项目代码开源开放，public repo，通过文档体系连接流程
  - research，深入研究目录，产出paper和PRD
  - community，产品上线后的增长和运营基于社区
3. 其他目录
  - life，一些vision规划和metrics，草稿阶段，人工维护
  - scripts，一些脚本，AI维护，用于日程研究和开发流程的自动化

## Flow
1. 使用中文回复问题
2. 本rules仅仅适用于开发模式，启用本模式，需要在对话开头提示：进入开发模式；关闭本模式，需要在对话开头提示：关闭开发模式。
3. 本rules采用交互式对话的收集信息，结合AI自身的deep search 和thinking，推断是否满足下阶段信息需要。
4. 开发模式包括四个阶段，对应四个文档：Solution.md（项目目录外部的design目录下，一般复制到docs目录下）, PRD.md（项目目录外部的design目录下，一般复制到docs目录下）, tasks/多个子任务（taskmaster目录下tasks子目录,一般由taskmaster根据PRD来自动生成），Changes.md（项目根目录docs目录下，用来每次完成一个子任务进行进度汇报和commit节点）
5. 开发模式依赖设计模式提供的README.md（项目根目录下）以及设计文档（采用项目名称命名的md，以及其他必要文档，例如Architechture，API，Components等，位于项目目录外部的design目录下）。
6. 辅助文档：test case，test result，deploy，release等，位于项目根目录docs目录下


### Solution模板
@ docs/Solution-template.md

### PRD模板
@ docs/PRD.md

### tasks/子任务模板
@ projects/项目名称/.taskmaster/tasks

### Changes模板
@ docs/Changes.d

### Architechture模板
@ docs/Architechture.md

### API
@ docs/API.md

### Components
@ docs/Components.md
