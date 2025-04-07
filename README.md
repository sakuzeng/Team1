# AI驱动的简历智能问答系统

一个基于AI的智能简历智能问答系统，支持项目经验、个人优势和编程能力的综合评估。

## 项目演示

🎥 [点击观看项目演示视频](https://www.bilibili.com/video/BV1HERkYAE8D/)

# 产品定义

本系统是一个基于人工智能的**简历问答与评估平台**，通过结构化解析候选人简历、提取技术与项目关键词，生成定制化问答，并对候选人的回答进行智能评分与能力分析。本系统不模拟完整面试流程，仅专注于候选人简历内容的深度核验与能力验证，辅助面试官高效、客观地判断简历真实性和技术掌握程度。

## 目标用户

**技术类岗位求职者**：作为自测工具，用于检测自身简历中描述是否经得起深度提问，查漏补缺。

**医疗、制造、教育等非技术行业的面试官或HR**，面对包含AI/技术内容的岗位（如AI工程师、数据分析员），自身不具备专业背景但需要评估候选人简历真实性。

## 目标痛点

**HR/面试官难以精准提问**：面对陌生技术栈、泛泛而谈的简历，难以判断候选人真实能力。

**简历“堆料”严重，难辨真伪**：求职者倾向于美化简历，但面试中无法支撑。

**现有问答工具碎片化、低效**：没有一个系统能围绕候选人简历进行结构化提问与评估。

**简历问答的过拟合与欠拟合**：完全针对简历的内容进行提问，缺少灵活性和拓展性，亦或缺少对候选人技术背景的定制性提问。

## 解决方案特色

**聚焦“简历驱动”的精准提问机制**：系统围绕简历中明确提到的技术名词、项目经验或方法工具，生成**定制化、多轮问答**，避免通用模板式提问。

**提问附参考答案与评分要点，非技术人员也能轻松使用**：每一个问题都配备标准答案与可视化评分建议，即使面试官不具备技术背景，也能准确判断候选人回答是否合理。

**问答逻辑层层递进，避免过拟合或浅尝辄止**：采用**基础→理解→应用→优化→批判性反思**的提问路径，既能避免只问简历中表面内容，也不会偏离简历范围，做到“既准又深”。

**能力评估结构化输出，便于快速决策**：系统自动生成多维度评估报告，量化候选人技术水平、表达能力与逻辑思维，支持一键导出，服务HR全流程记录与沟通。

**支持上下文学习**：通过对简历内容及知识库问题的匹配，实现上下文追问与语义连续，兼顾灵活性与针对性，提升问题质量。

# 产品核心竞争力

为了实现上述特色与优势，我们构建了以下核心支撑体系：

- **NLP驱动的简历结构化建模引擎**
  - 运用命名实体识别（NER）、依存句法分析与向量语义匹配技术，精准提取简历中项目经历、技术名词、方法论等关键信息。
  - 构建结构化数据，作为所有问题生成与评分的语义基础。
- **技术实体驱动的问答生成与追问机制**
  - 基于技术词汇与上下文内容，调用可控语言模型生成逐层深入的问答内容，支持多轮会话式提问。
  - 内置参考答案与评分点集，由领域专家或优质开源库支持构建。
- **非技术友好的评分与报告系统**
  - 面向非技术面试官设计评分维度与评估语言，简洁明了，降低理解门槛。
  - 支持自定义打分权重，兼顾灵活与标准化，适用于不同组织使用需求。
- **模块化架构设计，易扩展、易对接**
  - 各核心模块（简历解析、问答生成、评分系统、前端交互）独立运行，便于集成进企业内部系统或外部评估平台。

# 项目团队

- **李昕原（CEO & CTO）**

  - 负责项目整体技术架构设计、模型选型与系统集成，协调进度与推进全栈开发。

- **朱铠坊（CKO & CPO）**

  - 负责产品原型、答辩材料、项目汇报文档撰写与用户研究，统筹产品逻辑与展示流程。

- **彭林航**（简历解析模块负责人）

  - 负责多格式简历解析、信息抽取、实体识别与结构化输出。

- **金浩阳**（问答生成模块负责人）

  - 负责技术关键词提取、单轮与多轮问答生成机制设计、参考答案与评分要点编写。

- **刘浩**（深度追问机制负责人）

  - 负责上下文学习机制设计、追问逻辑实现，确保问答具有连贯性与层次性。

- **李增增**（编程挑战推荐引擎负责人）

  - 负责题库管理、技能识别与个性化题目推荐，涵盖算法、SQL等方向（可选模块）。

- **程盛霖**（评估与报告模块负责人）

  - 负责答案自动评分模型、能力结构化评估与报告生成。

- **黄晨峰 & 薛沁晨**（前端开发与交互设计）

  - 负责系统界面原型设计与前端开发，实现面向用户的友好交互与展示功能。

  

# 项目仓库目录结构

```
├─backend 后端代码
│  │  pipeline.py                 完整的pipeline，由李昕原负责
│  │  report.py                   报告导出与评估，由程盛霖负责
│  │  
│  ├─code
│  │      code_recommender.py     编程题问答，由李增增负责
│  │      
│  ├─parser
│  │      extractor.py            简历内容解析，由彭林航负责
│  │      
│  └─qa_engine
│          advantages.py          优势问答，由刘浩负责
│          item.py                项目问答，由金浩阳负责
│          
├─data
├─demo                             demo展示
│                  
├─frontend
│      frontend.py                 前端展示，由黄晨峰、薛沁晨负责
```



# 项目主计划

| 周次   | 阶段目标内容                                                 | 主要责任人                                                   |
| ------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **1**  | 团队组建与角色分工；明确项目初步方向与目标定位               | 全体参与，李昕原统筹规划                                     |
| **2**  | 明确产品定义与核心功能点；完成初步产品概念稿与功能框架，进行demo展示 | 朱铠坊牵头，彭林航完成简历结构化数据构建，薛沁晨进行demo展示 |
| **3**  | 各模块原型功能开发启动：简历解析、问答生成、评分逻辑等       | 金浩阳/刘浩/李增增/程盛霖完成核心功能                        |
| **4**  | 前端展示开发与系统接口联调，支持结果输出与能力报告生成       | 黄晨峰/薛沁晨完成前端展示                                    |
| **5+** | 各模块集成并最终展示                                         | 李昕原协调集成并部署                                         |

# 团队协同工作制度

**每周固定周会（周一晚）**：回顾上周进度、问题同步、明确本周分工

**微信群即时沟通 + 飞书/语雀文档协作**：任务追踪、文档归档、素材共享

**GitHub代码协作机制**：使用分支开发 + Pull Request + Code Review，由模块负责人合并
