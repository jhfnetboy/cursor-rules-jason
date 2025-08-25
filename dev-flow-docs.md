# Development flow and docs rules for AI vibe coding
This file will be include in claude.md, gemini.md and docs directory in project root.
This file create a rule for work flow and rules for all project development.
本文主要服务于独立的项目开发流程，从属于整体exploaration流程：设计、研究、项目（研发）、社区。
@ my-explaration/README.md，参考此文档获得全局上下文
本文存在于任何用于开发为目的的项目目录，包括子项目内，一般是claude.md和gemini.md，产出的文档一般在项目目录下的docs目录。

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
7. 所有文档开头是创建时间，修改时间（多条历史），版本号，持续维护

### 工作方式
1. 按四个阶段，检查文档是否齐全，从Solution开始，如果没有，则按模板进行交互式提问，收集足够信息，进行深度思考和研究后建立文档，依赖模板，但不局限于模板，产出一个针对问题的清晰描述和解决方案的核心阐述。
2. 其他文档类似，依赖模板，不局限于模板，交互收集信息，产出对应文档
3. 从prd到tasks，需要调用taskmaster工具，参考readme文档说明，子任务文档没有模板，依赖taskmaster提供标准
4. 然后开始完成子任务

### Solution模板
@ docs/Solution-template.md

### PRD模板
@ docs/PRD-template.m
PRD文档强制要求分为三个Phase，设计思路是循序渐进的迭代，类似原型迭代法，先建立最简单和基础的prototype，运行并迭代：
- 概念验证的原型阶段：罗列出三个问题，回答这三个问题，可以拆分为子问题，通过开发来验证，确定要回答这几个问题，需要的业务主流程和架构雏形。
- 主要能力验证的核心组件迭代阶段：问题和子问题需要系统来提供能力解决，依赖业务主流程和架构雏形进一步迭代，完善业务流程，明确子模块的出入参数和能力定义，调试整体业务流程的衔接，找到制约或者难点，给出方案并解决。有一个完整的用户故事，拆分为若干UserCase，从用户视角和系统实现两个视角描述和实现，并在系统技术层面进行严格检验，状态转换，数据存储，业务一致性，都要有具体的检查和测试标准。
- 产品级别完善的阶段：

### tasks/子任务模板
@ projects/项目名称/.taskmaster/tasks
此部分交给

### Changes模板
@ docs/Changes-template.d
完成一次任务进行一次汇报，如果是一个完整的用例或者小版本阶段，写入Changes.md
禁止任何浮夸的自我感动，用词精确，工程师冷静思维模式，不相信言语文字，提供验证报告和复现流程。

### Architechture模板
@ docs/Architechture-template.md
要包括主要技术栈，备选技术栈，核心技术验证，主要组件定义，系统架构图（mermaid）

### API
@ docs/API-template.md
串联所有业务流程的核心API定义，可以兼容Restful，但以JSONRPC为主
划分为功能API（少而精）和非功能API

### Components
@ docs/Components-template.md
组件入口参数约定和内部的设计，包括核心函数和其他函数，流程，异常处理，安全检查和校验
