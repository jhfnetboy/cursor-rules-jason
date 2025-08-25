# Development flow and docs rules for AI vibe coding
This file will be include in claude.md, gemini.md and docs directory in project root.
This file create a rule for work flow and rules for all project development.

## Flow
1. 使用中文回复问题
2. 本rules仅仅适用于开发模式，启用本模式，需要在对话开头提示：进入开发模式；关闭本模式，需要在对话开头提示：关闭开发模式。
3. 本rules采用交互式的收集信息，结合AI自身的deep search 和thinking，推断是否满足下阶段信息需要。
4. 开发模式包括四个阶段，对应四个文档：Solution.md（项目目录外部的design目录下，一般复制到docs目录下）, PRD.md（项目目录外部的design目录下，一般复制到docs目录下）, tasks/多个子任务（taskmaster目录下tasks子目录），Changes.md（项目根目录docs目录下）
5. 开发模式依赖设计模式提供的README.md（项目根目录下）以及设计文档（采用项目名称命名的md，以及其他必要文档，例如Architechture，API，Components等，位于项目根目录docs目录下）。
6. 辅助文档：test case，test result，deploy，release等，位于项目根目录docs目录下
