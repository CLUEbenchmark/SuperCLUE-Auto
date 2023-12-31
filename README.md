# SuperCLUE-Auto
汽车行业中文大模型测评基准，基于多轮开放式问题的细粒度评测

## 前言
近年来，随着人工智能技术的发展，大模型在各个领域得到了广泛应用。当前高速发展的汽车行业中，随着智能化、智能驾驶、车联网等技术的不断进步，
对于中文大模型的需求也日益增长。

然而，尽管大模型在汽车领域的应用潜力巨大，但现有的大模型测评基准并未能覆盖汽车行业的需求，它们主要是针对通用能力的测评，这导致了行业内对
大模型能力的评估缺乏公开的评价标准。

为了解决这一问题，我们推出了专门针对汽车行业的大模型测评基准（SuperCLUE-Auto）。

这是首个汽车行业大模型测评基准，它是一个多维度的多轮开放式问题的测评基准。它不仅能评价汽车行业大模型的能力，也能结合具体维度对模型回答给出细化的反馈。

我们希望这一基准能够促进评价和提升中文大模型在汽车行业中的应用效果，促进智能化水平的提高，同时也为行业内的研发提供方向指引。

<img src="https://github.com/CLUEbenchmark/SuperCLUE-Auto/blob/main/resources/img/superclue_auto.png"  width="100%" height="100%"></img>


# SuperCLUE-Auto

## 一、定义与能力维度

### 1.智能座舱与交互
一个高度集成的人机交互环境，它整合了驾驶信息管理、车辆控制功能及娱乐系统，通过强大的信息处理能力，提供一个高效、直观且充满未来感的驾驶和乘坐体验。
不仅致力于提升用户体验，增加驾乘舒适度和安全性，而且通过人工智能、多屏幕显示、互联网连接和主动响应式交互等技术，使汽车逐渐从单纯的交通工具转变
为旨在满足用户全面需求的“第三生活空间”。

使用场景包括但不限于：用车、出行、娱乐和信息获取。


### 2.车辆使用指南
车辆使用指南是车主的操作和维护百科全书，提供详尽的车辆功能使用方法、维护指南、故障诊断以及售后资源，以确保车辆得到正确使用和最佳维护。


### 3.汽车营销
汽车营销是一系列旨在促进汽车销售和品牌忠诚度的策略和活动，它涵盖广告、促销、品牌建设、市场研究以及客户关系管理。

包括但不限于：汽车厂商的产品发布会文案、汽车媒体介绍产品亮点、汽车测评、4S宣传促销文案、选车、汽车视频、汽车资讯等。


### 4.汽车理解与通用知识
汽车理解与通用知识是指对汽车行业的全面认知和解释能力。

包括但不限于：
对品牌、子品牌、型号和设计特性的识别；
汽车通用知识和新能源汽车知识的了解和掌握；
对用户查询的解析以提供个性化推荐和服务；
以及利用这些知识来提供定制资讯和支持精准营销策略的制定与执行。


## 二、测评方法及打分规则
评估流程-评价标准-打分规则

### 1.评估流程
 1) 设定每个维度下的评估标准
 2) 针对每一个维度下的问题，基于该维度下的多个评价标准，结合打分规则并使用超级模型作为裁判逐个打分，并获得该题目的得分（即每个维度下的平均分）
 3) 获得每一个维度下所有题目的分数，并计算特定模型（如GPT3.5）在该维度的得分（即平均分）

  超级模型，是指显著超越绝大多数可用模型的强语言模型。

### 2.评价标准

针对每一个维度，都有自己的评价标准。

如，汽车营销这个维度，使用了下面三个评价标准：符合场景设定的程度、满足客户的要求、内容的创造性。

### 3.打分规则

针对模型回答问题的质量的打分规则（1-5分）：

1：不相关，或严重错误

2：轻微错误，质量较低

3：质量中等，视为及格

4：质量良好，符合预期

5：质量优秀，超出预期



# 示例
### 示例1：智能座舱与交互

（第一轮对话）

  <img src="https://github.com/CLUEbenchmark/SuperCLUE-Auto/blob/main/resources/img/auto10.png"  width="87%" height="87%"></img>

（第二轮对话）

  <img src="https://github.com/CLUEbenchmark/SuperCLUE-Auto/blob/main/resources/img/auto11.png"  width="87%" height="87%"></img>

### 示例2：汽车营销

（第一轮对话）

  <img src="https://github.com/CLUEbenchmark/SuperCLUE-Auto/blob/main/resources/img/auto20.png"  width="87%" height="87%"></img>

（第二轮对话）

  <img src="https://github.com/CLUEbenchmark/SuperCLUE-Auto/blob/main/resources/img/auto21.png"  width="87%" height="87%"></img>

### 示例3：汽车理解及知识

（第一轮对话）

  <img src="https://github.com/CLUEbenchmark/SuperCLUE-Auto/blob/main/resources/img/auto30.png"  width="87%" height="87%"></img>
 
 （第二轮对话）
 
  <img src="https://github.com/CLUEbenchmark/SuperCLUE-Auto/blob/main/resources/img/auto31.png"  width="87%" height="87%"></img>

### 示例4：车辆使用指南

（第一轮对话）

  <img src="https://github.com/CLUEbenchmark/SuperCLUE-Auto/blob/main/resources/img/auto40.png"  width="87%" height="87%"></img>
 
 （第二轮对话）
 
  <img src="https://github.com/CLUEbenchmark/SuperCLUE-Auto/blob/main/resources/img/auto41.png"  width="87%" height="87%"></img>



# 测评结果

### SuperCLUE-Auto四大能力与应用

| 序号 | 模型               | 机构         | 智能座舱<br/>与交互 | 汽车<br/>营销 | 车辆使<br/>用指南 | 汽车理解<br/>通用知识 |
|:----:|:----:|--------------|:----:|:----:|:----:|:----:|
| -    | GPT4-Turbo         | OpenAI       | **83.2**          | **80.4**     | **91.8**        | **80.4**              |
| -    | GPT-4              | OpenAI       | 79.4          | 74.4     | 85.8        | 77.6              |
| 1   | 文心一言3.5           | 百度          | 77.8          | 76.6     | 86.2        | 76.0              |
| 2   | ChatGLM-Turbo      | 清华&智谱AI     | 72.6          | 75.6     | 86.6        | 78.4              |
| 3   | XVERSE-13B-2-Chat  | 元象科技       | 72.4          | 74.2     | 84.4        | 77.0              |
| 4    | Baichuan2-13B-Chat | 百川智能       | 67.4          | 75.4     | 84.2        | 79.4              |
| -    | GPT-3.5-Turbo      | OpenAI       | 71.8          | 73.6     | 84.8        | 74.4              |
| 5    | Qwen-14B-Chat      | 阿里巴巴       | 69.4          | 73.2     | 83.2        | 78.0              |
| 6    | MiniMax-Abab5.5    | MiniMax      | 72.0          | 74.8     | 74.4        | 78.8              |
| 7    | 讯飞星火V3.0          | 科大讯飞       | 66.2          | 74.2     | 78.4        | 72.4              |
| 8    | ChatGLM3-6B        | 清华&智谱AI       | 53.2          | 70.8     | 76.0        | 68.2              |
| -    | Llama2-13B-Chat    | Meta         | 55.4          | 76.2     | 76.8        | 53.0              |

### SuperCLUE-Auto第一二轮得分分解表

| 序号 | 模型名称           | 第一轮  | 第二轮  | 分数差异 |
|:----:|:------------------:|:-------:|:-------:|:--------:|
|  -   | GPT-4-Turbo        |  85.08  |  82.92  |  -2.16   |
|  -   | GPT-4              |  81.38  |  76.98  |  -4.40   |
|  1   | 文心一言3.5       |  80.46  |  78.16  |  -2.30   |
|  2   | ChatGLM-Turbo      |  80.46  |  76.24  |  -4.22   |
|  3   | XVERSE-13B-2-Chat  |  78.66  |  75.40  |  -3.26   |
|  4   | Baichuan2-13B-Chat |  77.94  |  75.26  |  -2.68   |
|  -   | GPT-3.5-Turbo      |  75.98  |  76.52  |   **0.54**   |
|  5   | Qwen-14B-Chat      |  76.98  |  75.08  |  -1.90   |
|  6   | MiniMax-Abab5.5    |  74.84  |  75.18  |  **0.34**   |
|  7   | 讯飞星火-V3.0     |  75.10  |  70.70  |  -4.40   |
|  8   | ChatGLM3-6B        |  66.36  |  67.86  |   **1.50**   |
|  -   | Llama2-13B-Chat    |  66.58  |  64.18  |  -2.40   |

注：分数差异=第二轮得分-第一轮得分

# 结论与分析

### 1. 总体表现

多个中文大模型在汽车行业上具有良好表现（75分或以上），说明当前大模型在汽车场景已经显现出应用价值。

### 2. 能力成熟度与模型潜力

有4个中文大模型在中文的汽车场景的表现超过了GPT-3.5，表明中文大模型在汽车场景上已经具备了的良好的潜力；
车辆使用指南这一维度上，多个模型达到了80分以上的优异表现，说明在一些对用户有用的任务上（如操作指南、车辆故障诊断、维修保养）已经具有较高的成熟度。

### 3. 能力的进步空间

本次测评有一个中文模型在智能座舱与交互这一维度上达到了良好表现，说明中文大模型在智能座舱与交互还有不少的进步空间。

### 4. 云 vs 端侧模型的能力
在13-14B这一当前认为中小的模型上，在汽车场景中有一些模型也超过了云端的闭源模型，说明可满足用户需求具备良好能力的汽车场景的
端侧模型存在很大的可能性。

### 5. 多轮能力的鲁棒性
相对于第一轮问题的得分，多数模型的第二轮问题得分都有不同程度的下降（最高下降4.4分）；但也有一些模型的得分保持相对稳定
（如，GPT3.5, MiniMax-Abab5,5,ChatGLM3-6B），表明这些模型在多轮交互场景中具有良好的鲁棒性。

# 交流与沟通

<p float="left">   
  <img src="https://github.com/CLUEbenchmark/SuperCLUE-Auto/blob/main/resources/img/superclue_autogroup.jpeg"  width="30%" height="30%"></img>
  <img src="https://github.com/CLUEbenchmark/SuperCLUE-Auto/blob/main/resources/img/brightmart_s.jpeg"  width="30%" height="30%"></img>
</p>
