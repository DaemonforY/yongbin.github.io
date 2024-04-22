

```markdown
# 数据分析4层次DDPP

*历经20余年，我们似乎终于进入一个真正的数据时代。但当我们在讨论数据分析时，我们究竟在讨论什么？*、
- 凡客当年很高调：我们做的不是电子商务，我们做的是数据分析。Google也吹牛：我们已不需要模型，我们只要数据
- 但Tableau近期和IDC联合对10个国家的1100多位企业管理者做了调查，调研结果表明，有83%的CEO都希望自己的企业能够做到更多的数据驱动。但只有33%能明确的讲清楚业务KPI和数据分析之间的链条。
- 数据分析到底是什么？什么是算法？是工具？是方法论？是业务解决方案？还是某种价值观？



我们小时候都玩过乐高积木。通过堆砌各种颜色和形状的积木，我们可以构建出城堡、飞机、甚至整个城市。现在，想象一下如果有一个数字世界的乐高，我们可以用这样的“积木”来构建智能程序，这些程序能够阅读、理解和撰写文本，甚至与我们对话。这就是大型语言模型（LLM）能够做到的，比如GPT-4，它就像是一套庞大的乐高积木套装，等待我们来发掘和搭建。

## LangChain概念和结构

### LangChain是什么？

LangChain就是那个让我们能将这些语言模型乐高积木组合成有趣应用的工具箱。它不是一个实物，而是一个开源的软件框架，帮助开发者像搭乐高一样快速构建和优化基于语言模型的应用。

### 为什么需要Langchain？

想一想，虽然我们有了乐高积木，但如果没有说明书或者构建工具，那么要搭建出一个复杂的模型将是非常困难的。同样地，即使我们有了强大的LLM，比如GPT-4，它们也需要“说明书”和“工具”来更好地服务于现实世界的需求。GPT-4有无与伦比的能力去处理语言，但是它还是需要额外的组件和连接才能完全发挥潜力，比如访问最新的数据、与外部API互动、处理用户的上下文信息等。LangChain就是这样一套“说明书”和“工具”，让GPT-4能够更好地融入到我们的应用中去。

### LangChain的乐高世界

举个例子，假设你想要用GPT-4建一个旅行顾问机器人。单独的GPT-4就像是一堆杂乱无章的乐高积木。它可能知道很多关于世界各地的信息，但如果不能实时查找最新的航班信息或者酒店价格，它提供的旅行建议可能就不够准确或实用。LangChain就好比是提供了一本指导手册和一套辅助工具，它能让你的旅行顾问机器人链接到航班数据库，记住用户的旅行偏好，甚至根据用户以往的提问历史来提供个性化的建议。

假设你正计划一场旅行，你向智能旅行问答助手提问：“我该带些什么去泰国旅行？”如果只有GPT-4，它可能会基于以往的数据提供一般性的建议，如防晒霜、泳衣等。但配备了LangChain的问答系统，它可以查询实时的天气预报API，了解当前泰国的季节和天气情况，提供更精确的建议，比如“泰国正处于雨季，记得带上雨具和防潮包”。同样地，如果你问：“泰国哪里的垂钓体验最佳？”LangChain可以帮助连接到最新的旅行博客和垂钓爱好者论坛，甚至直接查阅最近的旅行者评论，给你提供最受推荐的目的地。

另一个例子，如果你想要一个可以帮你总结长篇报告的工具，单用GPT-4可能会因文章太长而无法处理。LangChain提供的工具就像是设计用来构建复杂构造的专用乐高积木，它可以帮你把长篇报告切分成小部分让GPT-4处理，再将结果整合起来，最终生成一个完整的摘要。

### LangChain主要概念

Langchain主要提供了6大类组件帮助我们更好的使用大语言模型，可以视为开源版的GPT插件，提供了丰富的大语言模型工具，可以在开源模型基础上快速增强模型的能力。想象一下，你手中有一盒乐高积木，但这不是普通的积木，而是能够编程、交流甚至思考的智能积木。LangChain就像是这样一盒特殊的积木盒，里面装满了不同功能的积木块，这些积木组件集成了数十种大语言模型、多样的知识库处理方法以及成熟的应用链，几十种可调用的工具箱，为用户提供了一个快速搭建和部署大语言模型智能应用程序的平台。

![](https://oss-ata.alibaba.com/article/2024/01/319fc6bf-ccef-46ec-b63c-8a55dedc4fa1.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

### Models（模型）

#### LLMs（大型语言模型）

这些模型是LangChain积木盒中的基础积木。如同用乐高搭建房屋的地基，LLMs为构建复杂的语言理解和生成任务提供了坚实的基础。

#### Chat Models（聊天模型）

这些模型就像是为你的乐高小人制作对话能力。它们能够让应用程序进行流畅的对话，好比是给你的乐高积木人注入了会说话的灵魂。

#### Text Embedding Models（文本嵌入模型）

如果说其他模型让积木能够理解和生成文本，文本嵌入模型则提供了理解文本深度含义的能力。它们就像是一种特殊的积木块，可以帮助其他积木更好地理解每个块应该放在哪里。

### Prompts（提示）

#### Prompt Templates（提示模板）

想象一下，你正在给乐高小人编写剧本，告诉他们在不同场景下应该说什么。Prompt Templates就是这些剧本，它们指导模型如何回答问题或者生成文本。

### Indexes（索引）

LangChain通过Indexs索引允许文档结构化，让LLM更直接、更有效地与文档互动。

#### Document Loaders（文档加载器）

这些就像是一个个小仓库，帮助你的乐高世界中的智能模型存储和访问信息。Document Loaders能够将文档加载到系统中，方便模型快速查找。

#### Text Splitters（文本分割器）

有时候你需要将一大块乐高板分成几个小块来构建更复杂的结构。Text Splitters可以将长篇文本拆分成易于处理的小块。

#### Vector Stores（向量存储）

这些是一种特殊的存储设施，帮助你的乐高模型记住文本的数学表示（向量）。这就像是让积木块记住它们在整个结构中的位置。

#### Retrievers（检索器）

想象一下你需要从一堆积木中找到一个特定的小部件。Retrievers能够快速在向量存储中检索和提取信息，就像是乐高世界里的搜索引擎。

![](https://oss-ata.alibaba.com/article/2024/01/f87b0314-9ff0-4e69-98fa-be15be7792b5.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

### Memory（记忆）：对话的连贯性

LangChain通过Memory工具类为Agent和Chain提供了记忆功能，让智能应用能够记住前一次的交互，比如在聊天环境中这一点尤为重要。

#### Chat Message History（聊天消息历史）

最常见的一种对话内容中的Memory类，这就好比是在你的乐高角色之间建立了一个记忆网络，使它们能够记住过去的对话，这样每次交流都能在之前的基础上继续，使得智能积木人能够在每次对话中保持连贯性。

### Chains（链）

#### Chain、LLM Chain、Index-related Chains

CHAIN模块整合了大型语言模型、向量数据库、记忆系统及提示，通过Agents的能力拓展至各种工具，形成一个能够互相合作的独立模块网络。它不仅比大模型API更加高效，还增强了模型的各种应用，诸如问答、摘要编写、表格分析和代码理解等。

![](https://oss-ata.alibaba.com/article/2024/01/21580353-6e1d-4680-922b-d80b7d5bc01b.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

Chain是连接不同智能积木块的基本方式，而LLM Chain是最简单的LLM+Prompts的一种chain，专门用于链接语言模型。Index-related Chains则将索引功能集成进来，确保信息的高效流动。

![](https://oss-ata.alibaba.com/article/2024/01/84b5c00e-94f3-4375-9ad7-61322fc99f28.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

### Agents（代理）

在LangChain的世界里，Agent是一个智能代理，它的任务是听取你的需求（用户输入）和分析当前的情境（应用场景），然后从它的工具箱（一系列可用工具）中选择最合适的工具来执行操作。这些工具箱里装的是LangChain提供的各种积木，比如Models、Prompts、Indexes等。

如下图所示，Agent接受一个任务，使用LLM（大型语言模型）作为它的“大脑”或“思考工具”，通过这个大脑来决定为了达成目标需要执行什么操作。它就像是一个有战略眼光的指挥官，不仅知道战场上的每个小队能做什么，还能指挥它们完成更复杂的任务。

![](https://oss-ata.alibaba.com/article/2024/01/adb8793f-b242-4909-ae56-a70564ebe3b3.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

LangChain中Agent组件的架构图如下，本质上也是基于Chain实现，但是它是一种特殊的Chain，这个Chain是对Action循环调用的过程，它使用的PromptTemplate主要是符合Agent Type要求的各种思考决策模版。Agent的核心思想在于使用LLM进行决策，选择一系列要执行的动作，并以此驱动应用程序的核心逻辑。通过Toolkits中的一组特定工具，用户可以设计特定用例的应用。

![](https://oss-ata.alibaba.com/article/2024/01/8c0a47b9-5e1c-468b-a3e4-5ba71f280165.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

#### Agent执行过程：AgentExecutor

AgentExecuter负责迭代运行代理，直至满足设定的停止条件，这使得Agent能够像生物一样循环处理信息和任务。

![](https://oss-ata.alibaba.com/article/2024/01/0e3ff3ec-11c3-496a-93f6-97400eb8a3c6.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

##### 观察（Observation）

在这个阶段，代理通过其输入接口接收外部的触发，比如用户的提问或系统发出的请求。代理对这些输入进行解析，提取关键信息作为处理的基础。观察结果通常包括用户的原始输入或预处理后的数据。

##### 思考（Thought）

在思考阶段，代理使用预先设定的规则、知识库或者利用机器学习模型来分析观察到的信息。这个阶段的目的是确定如何响应观察到的情况。代理可能会评估不同的行动方案，预测它们的结果，并选择最合适的答案或行为。

在LangChain中，这个过程可能涉及以下几个子步骤：

1.

理解用户意图：使用NLP（自然语言处理）技术来理解用户的问题是什么。

2.

推断所需工具：确定哪个工具（或工具组合）能解决用户的问题。

3.

提取参数：提取所需工具运行的必要参数。这可能涉及文本解析、关键信息提取和验证等过程。

##### 行动（Action）

根据思考阶段的结果，代理将执行特定的行动。行动可能是提供答案、执行任务、调用工具或者与用户进行进一步的交云。

在LangChain代理中，这通常涉及以下几个子步骤：

1.

参数填充：将思考阶段提取的参数填入对应的工具函数中。

2.

工具执行：运行工具，并获取执行结果。这可能是查询数据库、运行算法、调用API等。

3.

响应生成：根据工具的执行结果构建代理的响应。响应可以是纯文本消息、数据、图像或其他格式。

#### Agent推理方式：AgentType

代理类型决定了代理如何使用工具、处理输入以及与用户进行交互，就像给机器人挑选不同的大脑一样，我们有很多种"智能代理"可以根据需要来选择。有的代理是为聊天模型（接收消息，输出消息）设计的，可以支持聊天历史；有的代理更适合单一任务，是为大语言模型（接收字符串，输出字符串）而设计的。而且，这些代理的能力也不尽相同：有的能记住你之前的对话（支持聊天历史），有的能同时处理多个问题（支持并行函数调用），也有的只能专心做一件事（适用于单一任务）。此外，有些代理需要我们提供一些额外信息才能更好地工作（所需模型参数），而有些则可以直接上手，不需要额外的东西。所以，根据你的需求和你所使用的模型，你可以选择最合适的代理来帮你完成任务，常见的代理类型如下：

#### Agent与Chain的关系

如果说Chain是LangChain中的基础连接方式，那么Agent就是更高阶的版本，它不仅可以绑定模板和LLM，还能够根据具体情况添加或调整使用的工具。简单来说，如果Chain是一条直线，那么Agent就是能够在多个路口根据交通情况灵活选择路线的专业司机。

## LangChain实际案例：人脸技术问题的智能排查助手

### 使用LangChain处理人脸识别问题的排查

随着人脸识别服务的线上线下日调用量和应用场景快速发展，人脸识别团队正在面临一个巨大的挑战，每天反馈到团队的各种识别问题的case过多，排查起来费时费力，为了快速诊断问题，团队决定使用LangChain来构建一个智能排查助手。这个助手可以分析用户问题，错误日志，与人脸识别的APIs进行交互，甚至生成修复建议。

在LangChain框架中，工具（Tools）是用于解决特定问题的可调用的功能模块。它们可以是简单的函数，也可以是更复杂的对象，能够实现一项或多项特定任务。下面将详细介绍几种不同的工具定义及其在人脸识别问题排查过程中的应用。

首先，我们需要导入依赖的函数，主要来自各个现有日志系统的接口，能够提取比对分，黑名单，读取人脸库大小等信息：

#### zmng\_query 工具

当用户遇到人脸比对失败的情况时，人脸的日志系统都在zmng平台上，我们现在通过zmng\_query工具提取UID，根据UID查询相关的用户信息，包括他们是否在黑名单上，提取比对分数，并获取机具端及实际的人脸库大小信息，判断是什么原因识别不通过。

#### extract\_compare\_scores 工具

这个工具用于从日志文件中提取比对分数，这对于诊断是人脸比对技术问题还是用户本身的问题非常关键。

#### extract\_local\_group\_size 和 extract\_actual\_group\_size 工具

这两个工具分别用于提取机具端和实际的人脸库大小（groupSize）。这项信息有助于判断是否所有必要的人脸数据都已经下发到机具端。

#### blacklist\_query 工具

此工具用于查询指定用户是否在黑名单中，这是人脸识别系统中的一项常见检查。

#### perform\_logic\_judgement 工具

根据比对分数和本地库与实际库的大小，此工具能够给出比对不通过的分析结论。

在LangChain框架中，tools是一系列用于执行特定任务的函数或类的实例，它们可以被智能代理（Agent）调用以完成用户请求。在提供的上下文中，需要用到的tool已经定义好了

将所有这些工具组装到一个列表中，然后可以使用这个列表来初始化一个智能代理（Agent），该代理能够运行工具并与用户进行互动。在LangChain中，智能代理负责管理用户的输入，并决定调用哪个工具来处理特定的请求或问题。通过这种方式，我们可以构建一个强大的、能够解决人脸识别相关问题的智能系统。

#### 聊天模型实例化

LangChain使用大型语言模型（LLM）如GPT-4来处理自然语言的理解和生成。在这里，我们创建一个聊天模型实例，这将允许我们的代理与用户进行自然语言交互：

temperature参数控制生成文本的创造性；较低的temperature值（例如0）将导致更确定性和一致性的响应。

#### 用户交互

一旦工具和聊天模型都被实例化，我们就可以初始化智能代理。在LangChain中，代理（Agent）是与用户进行交云的主体，它使用上面定义好的tools和LLM来处理用户的输入并提供响应，。

现在，我们可以开始与用户的交互：

在这个交互式循环中，智能代理会根据用户的输入运行相应的工具，并使用聊天模型生成自然语言响应。这使得用户可以以对话方式提出问题，并得到解答。

#### 智能代理运行过程

在LangChain框架中，智能代理（Agent）通常按照观察（Observation）- 思考（Thought）- 行动（Action）的模式来处理任务。这个模型相当于一个决策循环，代理首先观察外部输入，然后进行内部思考以产生相应的行动方案。下面详细解释这个技术链路和逻辑：

#### 完整的技术链路示例

我们构建了一个关于人脸识别的问答智能代理，用户询问：“为什么我的脸无法被系统识别？”以下是这个代理按照Observation-Thought-Action模式处理此请求的过程：

![](https://oss-ata.alibaba.com/article/2024/01/0678fa37-a752-4a84-babd-aec01efe7581.gif)

### 利用LangChain与人脸问答知识库进行交互

下面这些技术模块共同构成了一个基于LangChain与人脸知识库进行交互的系统。

#### 模块1: 问题与答案数据的加载

这个模块负责读取问题和答案对，并将它们存储在一个字典结构中，以便后续检索。

#### 模块2: 嵌入向量的生成和Faiss索引创建

Faiss 是 Facebook AI Research (FAIR) 精心打造的一款强大向量数据库，专为高效执行相似性搜索和稠密向量聚类而设计。在处理大型数据集时表现尤为出色，能迅速在海量向量中锁定与查询向量最为匹配的项，极大地加速了搜索流程。无论是机器学习还是数据挖掘，Faiss 都是一个不可或缺的工具，常见的应用场景包括但不限于推荐系统、图像搜索和自然语言处理。

除了 Faiss，LangChain 支持的向量数据库范围广泛，覆盖了多种语言和平台。这些数据库包括阿里云的 OpenSearch、AnalyticDB、Annoy、Atlas、AwaDB，以及 Azure Cognitive Search、BagelDB、Cassandra、Chroma、Clarifai 等。此外，还有 ClickHouse Vector Search、Activeloop's Deep Lake、Dingo，以及各种DocArray搜索能力，如DocArrayHnswSearch和DocArrayInMemorySearch。ElasticSearch、Hologres、LanceDB、Marqo、MatchingEngine、Meilisearch、Milvus、MongoDB Atlas 和 MyScale 也在支持之列。OpenSearch 和 pg\_embedding 也提供了优质的搜索服务。这些多样化的数据库选择使得LangChain能够在不同的环境和需求下提供灵活、高效的搜索能力。

##### OpenAIEmbeddings() 初始化

这一行创建了一个OpenAIEmbeddings实例，它是用来生成文本embedding的。这些embedding是高维向量，可以捕捉文本内容的语义信息，用于文本之间的相似性比较。

##### 创建FAISS索引

create\_faiss\_index函数接受一个embedding矩阵（通常是二维数组，其中每行是一个向量），初始化一个FAISS索引，并将这些向量添加到索引中。这个索引后续将用于相似性搜索。

##### 在FAISS索引中搜索

search\_faiss\_index函数获取一个查询向量和一个FAISS索引作为输入，然后使用这个索引来找到与查询向量最相似的存储向量。函数返回最相似项的索引，这通常用来在一个数据库或列表中检索具体项。

#### 模块3: 精确匹配查询

当用户提出一个特定的问题时，这个功能会根据用户的输入在知识库中查找精确匹配的问题。

#### 模块4: 模糊匹配查询

这个模块使用嵌入向量和Faiss索引来找到与用户查询最相似的问题，并返回相应的答案。

4.

当用户提出查询时，将查询文本也转换为嵌入向量。

##### search\_by\_exact 和 search\_by\_fuzzy 工具

在tools列表中，增加search\_by\_exact 和 search\_by\_fuzzy 两个工具能力，其他逻辑不变

通过LangChain的灵活性和模块化，这个能够自动化处理人脸识别问题的智能排查助手，大大提高了问题诊断的效率并减轻了人工负担。

注意观察下面agent的Observation Thought Action三个阶段，agent会自动提取出tool需要的参数，形成action

![](https://oss-ata.alibaba.com/article/2024/01/951af5a3-bb1c-460c-91e1-e63092beceb9.gif)

## 智能体的快速发展

### 智能体的基本概念

#### 智能体是什么？

一句话总结，Langchain这个开发框架，是为了让我们更容易更低成本的构建大语言模型的智能应用，其中有自主行动能力，能够思考跟外部环境/工具交互的叫Agent，智能体。

AI Agent业界定义是具有环境感知、决策制定和行动执行能力的智能实体，并且能够通过独立思考和工具调用来逐步实现既定目标。随着大型语言模型（LLM）的出现，AI Agent又被定义为基于LLM驱动的Agent实现对通用问题的自动化处理。当AI Agent被赋予一个目标时，它能独立地进行思考和行动，详细规划出完成任务所需的每一个步骤，并通过外部反馈与自我思考来创建解决问题的prompt。例如，当要求ChatGPT购买咖啡时，它可能会回应“无法购买咖啡，因为它仅是一个文字型AI助手”。AI Agent的关键特征包括自治性、知觉、反应能力、推理与决策能力、学习能力、通信能力以及目标导向性，这些特性使得智能体能成为真正释放LLM潜能的关键，它能为LLM核心提供强大的行动能力。

#### 智能体的发展方向

智能体（AI Agent）的发展可谓是人工智能领域的一个重要里程碑。大语言模型不再局限于处理文本信息，它们的能力正在扩展到与世界各种软件工具的直接交互中。通过调用APIs，这些模型现在可以获取信息、执行分析、生成报告、发送通知，甚至访问网络，访问数据库，使其功能变得无比强大。这种变化，让这些模型从单纯的文本处理者转变为真正的数字助理，能够理解用户的需求，并使用正确的工具为用户提供服务。

随着技术的发展，大语言模型使用工具能力与日俱增。早期的模型可能需要明确的、结构化的指令才能正确调用几十个工具，而现在，部分模型可以根据目标自由的调用上万个工具，并采取相应的行动。想象一下，仅通过简单的对话，你的智能代理就能为你预订餐厅、安排行程、购物，甚至编程。这种灵活性和智能度的提升，极大地增强了用户的体验。

另一个领域的进步是智能体正在从单一的智能代理到多代理系统的转变。初期，一个代理只能单一地执行任务，而现在，多个代理能够同时工作，协同完成更加复杂的任务。例如，一个代理可以负责数据收集，而另一个代理同时进行数据分析，第三个代理则负责与用户沟通结果。这些代理之间的协同工作像是一个高效的团队，每个成员都在其擅长的领域发挥作用。

同时，智能代理与人类用户之间交互也在往更自然化的方向发展，多代理系统工作过程中，可以引入人类的决策。这种人机交互的深度，使得智能代理不仅是工具的操作者，更是人类的合作者。

正是这些技术进步，塑造了我们今天所见证的智能体技术景观，大语言模型在工具使用能力上的显著提升以及智能代理的发展，为未来的可能性打下了坚实的基础。全球范围内，新兴的智能体技术如OpenAI的WebGPT为模型赋予了利用网页信息的能力，Adept培养的ACT-1能独立于网站操作并使用Excel、Salesforce等软件，谷歌的PaLM项目旗下的SayCan和PaLM-E尝试将LLM与机器人相结合，Meta的Toolformer探索使LLM能够自主调用API，而普林斯顿的Shunyu Yao所做的ReAct工作则结合了思维链prompting技术和“手臂”概念，使LLM能够搜索并利用维基百科信息。随着这些技术的不断完善和创新，我们有望完成更多曾经难以想象的任务，开启智能体技术的崭新篇章。

#### 智能体的分类

![](https://oss-ata.alibaba.com/article/2024/01/2751b0b0-c847-4be7-b515-0e1306efa154.jpeg?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

### 增强智能体的工具使用能力

智能代理和工具之间的关系可以类比为人类使用工具来完成任务的方式。就像人类使用锤子敲打钉子一样，代理可以调用一个API来获取数据、使用翻译服务来翻译文本或者执行其他功能以协助或完成它们的任务。通过增强代理的工具使用能力，它们能够执行更复杂、更精细的任务，并在更广泛的场景中提供帮助。

最近一些开源的大语言模型能够自由地与各种外部工具交互，比如Toolformer、Gorilla、ToolLLama等模型，它们是一类设计为优化和改进代理工具使用能力的模型，使代理更有效地与工具集成，完成任务，从而扩展LLMs的能力范围。

#### Gorilla：![](https://oss-ata.alibaba.com/article/2024/01/d3154588-d9b2-42fe-a5cf-cb738b8a48fc.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)精准调用1600+ API的智能体进步

Gorilla是一个基于检索感知的LLaMA-7B大型语言模型，也是一种基础的智能体，它能够使用各种API工具。这个模型通过分析自然语言查询，精准地找出并调用合适、语义语法均正确的API，从而提升了大型语言模型执行任务的能力和准确性。

Gorilla的一个主要特点是它能够准确地调用超过1600个API，并且这个数量还在增长。这一成就展示了如何利用语言模型的理解和生成能力，来扩展其在自动化工具使用上的潜力。为了进一步提高Gorilla的性能，开发团队通过模拟聊天式对话，对LLaMA-7B模型进行了微调，让其能够更自然地与用户进行交流，并生成相应的API调用。

此外，Gorilla也能够处理带有约束条件的API调用，这要求模型除了理解API的基本功能外，还必须能够识别和考虑各种参数约束。这一能力让Gorilla在处理特定要求的任务时显得更加智能和可靠。

在训练过程中，Gorilla不仅在无检索器的情况下学习，还在有检索器的环境中进行训练，以提升其适应和理解不断更新的API文档的能力。这种训练方式使得Gorilla不仅能响应用户的直接指令，还能够针对检索到的相关API文档生成精确的调用指令，减少了错误幻觉的发生。

![](https://oss-ata.alibaba.com/article/2024/01/016a13f8-d718-438b-97f8-ace4625d2a2c.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

总的来说，Gorilla不仅增强了语言模型在API调用和工具使用上的能力，还提高了处理带约束任务的复杂性，展现了智能体在自动化和人机交互方面的巨大潜力。

##### Gorilla-CLI：提升命令行互动体验

Gorilla-CLI是一个由加州大学伯克利分校开发，基于Gorilla模型的提升命令行交互体验的工具，它通过智能化的命令预测和补全，使得命令行操作更加直观和高效。当开发者在终端中输入命令时，Gorilla-CLI能够根据上下文提示可能的命令补全，甚至可以根据过去的操作模式预测下一步可能的命令，从而加速开发流程。[https://github.com/gorilla-llm/gorilla-cli](https://github.com/gorilla-llm/gorilla-cli)

###### 安装步骤：

###### 实验效果：

![](https://oss-ata.alibaba.com/article/2024/01/2def71f9-3abd-4c38-a32a-d875a3c63669.gif)

![](https://oss-ata.alibaba.com/article/2024/01/5afbf40d-3859-4094-bde6-208d8ab3b1ba.gif)

![](https://oss-ata.alibaba.com/article/2024/01/86e07fd3-812d-4797-b554-8ac65d8b7daa.gif)

#### ToolLLaMa：实现16000+ API的精准协同调用

ToolLLaMA也是一个基于开源LLaMA-7B语言模型的框架，旨在增强模型执行复杂任务的能力，特别是遵循指令使用外部工具API。通过扩展传统LLMs的功能，ToolLLaMA可以处理真实世界的应用场景，这些场景需要结合多个API工具来完成任务。（gorilla5月份刚发布， ToolLLaMa 8月份就紧跟着发布了，卷）

ToolLLaMA的关键特点在于支持大量的真实世界API，共16464个，覆盖49个类别。这种丰富的API支持为用户提供了更多的工具选项，以满足各种应用需求。ToolLLaMA使用ChatGPT生成的指令调整数据集ToolBench，这些数据集包含单工具和多工具使用场景的指令，使得模型能够学习如何解析和执行包含多个API调用的指令。

为了提高在这些复杂任务中的效率，ToolLLaMA采用了DFSDT算法，它是一种基于深度优先搜索的决策树，能够帮助模型在多个潜在解决方案中做出更好的选择。此算法增强了模型规划任务路径和推理的能力。

ToolLLaMA训练了一个API检索器，能够为给定的用户指令推荐合适的API，从而省去了手动筛选API的步骤，使得整个使用流程更加高效。

在性能评估方面，ToolEval结果表明，ToolLLaMA在执行复杂指令及泛化到未见APIs方面的效果与封闭源码的高级模型ChatGPT相似。这一发现表明，通过适当的训练方法和数据集，开源LLMs能够实现类似于封闭源码LLMs的工具使用能力。ToolLLaMA项目的代码、训练模型和演示都已在GitHub公开，以促进社区的进一步发展和应用。

![](https://oss-ata.alibaba.com/article/2024/01/1869f151-35c1-4eb3-adf2-ca18a8770406.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

###### 安装步骤：

###### 实验效果：

如果你正在计划一个给最好朋友的惊喜派对，并希望为每位参加聚会的人提供一些鼓舞人心的话语，那么可以使用toolLLama这样的语言模型，它能够让你轻松地调用一个工具来生成或查找各种名人的励志名言，特别是关于爱情、梦想和成功的话语。例如，其中一个例子返回了：“成功不是终点，失败也不是致命的：真正重要的是继续前进的勇气。”--丘吉尔

![](https://oss-ata.alibaba.com/article/2024/01/7d7b54ca-9015-4f66-a827-fa9fdce76847.gif)

### 智能体的发展：从单任务到多代理协同与人代理交互

随着人工智能技术的不断进化，我们见证了智能体（AI Agent）的发展：从只能执行单一任务的简单代理，到如今能够进行多代理协同与人类代理交互的复杂系统。这种进步不仅拓宽了智能应用的边界，使其能够在更加复杂的环境中同时处理多种任务，还提升了与用户合作的能力，共同做出更加精细化的决策。

我们正步入一个新纪元，其中最新的开源大型语言模型（LLMs）能够自由地与多样化的外部工具交互，完成更加丰富和复杂的任务。这不仅推动了AI技术的民主化，还为社区驱动的创新和发展打开了新的大门。

尽管LLMs的智能和精准的提示输入提供了巨大优势，但有效利用这些模型仍然需要用户掌握相应的技巧，这已导致培训市场的出现。然而，prompt工程的复杂性也对普通用户的体验造成了挑战。AI智能体，作为能够感知环境、做出决策和执行动作的独立实体，可能是解决这一挑战的关键。AI智能体不仅能够自主完成任务，也能够主动与环境交互。随着LLMs的发展，AI智能体为这些模型提供了实际行动力，不仅仅是作为工具，而是作为能够自动化处理通用问题的智能实体。通过释放LLMs的潜能，AI智能体将成为未来技术的关键驱动力。例如，AutoGPT将复杂任务分解为更易管理的子任务，并生成相应的提示（prompts）。MetaGPT将高级人类流程管理经验编码到智能体的提示中，促进了多智能体之间的结构化合作。ChatDev受到软件开发的经典瀑布模型的启发，通过模拟一个虚拟软件公司的环境，展示了智能体在专业功能研讨会中的合作潜力。在这个环境中，多个智能体扮演不同的角色，遵循开发流程，通过聊天进行协作。

#### MetaGPT

MetaGPT是由Deep Wisdom联合几个大学发布的一个基于大型语言模型（LLMs）专门为高效整合人类工作流程而设计的多智能体合作框架。通过将标准化操作程序（SOPs）编码到智能体的提示序列中，MetaGPT简化了工作流程，使智能体能够以类似于人类专家的方式来校验中间成果，这有助于减少错误的发生。

在MetaGPT系统中，智能体根据装配线原则被分配不同的角色，以协同完成复杂任务。任务被分解为多个子任务，每个子任务由相应的智能体负责。这种方法不仅提高了任务执行的一致性，还提升了解决方案的质量。例如，在软件工程的协作任务中，MetaGPT展现出了相较于传统基于聊天的多智能体系统更一致的解决方案生成能力。

广泛接受的SOPs在任务分解和有效协调中扮演了关键角色，尤其是在确定团队成员职责和中间产物标准方面。在软件开发领域，产品经理通常依据SOP来创建产品需求文档（PRD），这有助于指导整个开发过程。

MetaGPT框架吸取了SOPs的重要经验，并允许智能体生成结构化且高质量的需求文档、设计文档、流程图和界面规格。这种结构化的中间输出能够显著提升目标代码生成的成功率。MetaGPT模拟了一个高度规范化的公司流程环境，在这个环境中，所有智能体必须严格遵守已确立的标准和工作流程。在角色扮演构架中，智能体被分配了各种各样的角色，以高效协同工作、分解复杂任务。这种角色扮演的设计有助于减少无效交流，并降低大模型幻觉风险。

MetaGPT通过"编程促进编程"（programming to program）的方法，提供了一个有前景的元编程框架。智能体不仅是代码的执行者，还主动参与到需求分析、系统设计、代码生成-修改-执行、以及运行时调试的全过程。每个智能体都拥有特定的角色和专业知识，并遵循既定的标准。如此一来，MetaGPT成为了一种独特的解决方案，在自动化编程任务中展现出巨大的潜力，并推动了元编程的高效实现。

![](https://oss-ata.alibaba.com/article/2024/01/94b7d222-6992-4505-bd76-34ae844c9e22.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

MetaGPT接受单行需求作为输入，并输出用户故事、竞争分析、需求、数据结构、API、文档等。 在内部，MetaGPT包括产品经理、架构师、项目经理和工程师。它提供了一个软件公司的整个流程，以及精心编排的标准操作程序(SOP)。 代码 = SOP(团队) 是其核心理念。我们将SOP具体化，并将其应用到由大型语言模型(LLMs)组成的团队中。

![](https://oss-ata.alibaba.com/article/2024/01/51b02945-7732-47ca-8639-6d9c1bac611d.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

在通信协议中，智能体通过共享消息池发布和订阅结构化消息，以此来协调工作和交换信息。这允许智能体根据自己的角色和任务需求，获取相关信息并执行任务。

![](https://oss-ata.alibaba.com/article/2024/01/d52d2ab5-cf30-4093-8951-42eda12a4d63.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

MetaGPT中的工程师智能体可以生成代码，运行代码检查错误。如果遇到错误，智能体会查阅存储在记忆中的消息，并将它们与产品需求文档、系统设计和代码文件进行对比，以识别问题并进行修正。这一过程涉及迭代编程和可执行反馈，使得智能体可以不断优化其解决方案。

整个软件开发过程图强调了MetaGPT对SOPs的依赖性。这些SOPs规定了从项目开始到完成的每一步，确保智能体可以高效、系统地完成任务。

![](https://oss-ata.alibaba.com/article/2024/01/cf1f2195-692e-4526-91b3-a3c03723caf0.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

##### MetaGPT实验流程

###### 安装步骤：

###### 运行过程：

![](https://oss-ata.alibaba.com/article/2024/01/811b6407-d76e-4e1f-9b44-cb7a96a1cf8a.gif)

###### 实验效果：

![](https://oss-ata.alibaba.com/article/2024/01/bef8e5fa-1f72-4642-a46b-8058e6623ab2.gif)

#### ChatDev

ChatDev是OpenBMB联合清华大学NLP实验室共同开发的大模型全流程自动化软件开发框架，它模拟了一家虚拟软件公司，由担任不同职能的多个智能代理运作，包括首席执行官（CEO）、首席产品官（CPO）、首席技术官（CTO）、程序员、审查员、测试员和设计师。这些智能代理构成了一个多代理组织架构，并共同致力于一个使命："通过编程革新数字世界。" 在ChatDev中，代理们通过聊天参与研讨会协作，涵盖设计、编码、测试以及文档撰写等多种专业任务。

![](https://oss-ata.alibaba.com/article/2024/01/859b8d11-833f-4b24-975c-73d7d802cf1c.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

ChatDev通过模拟软件开发的瀑布模型，实现了智能的分阶段、分聊天的协作。每个阶段包含多个原子聊天，而在每个聊天中，两个扮演不同角色的智能体通过任务导向的对话来协同完成子任务。这个流程不仅包括了智能体之间基于指令的互动，还包括了角色专业化、记忆流、自省等机制，以确保智能体能够高效、准确地执行任务，并持续优化决策过程。

![](https://oss-ata.alibaba.com/article/2024/01/f208577b-d2db-451c-8e25-6e81cb108d64.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

角色专业化使每个智能体都能在对话中有效地扮演其指定的角色，比如程序员、审查员等。记忆流记录了聊天中的对话历史，使智能体在做决策时有足够的上下文信息。自省机制则是在达成共识的情况下，让智能体反思并验证决策，确保没有违反终止条件。

![](https://oss-ata.alibaba.com/article/2024/01/f95226c5-c550-4fcf-b2a9-9c31185a09dc.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

在编码和测试阶段，为了减少代码幻觉——即智能体生成与现有代码库不一致的代码——ChatDev引入了思维指令机制。智能体通过角色交换，明确询问或解释代码中的具体问题，这样可以更精确地定位问题所在，并通过更具体的指令指导程序员修复问题。这种机制加强了智能体对代码的理解，提高了编程和测试的准确性。![](https://oss-ata.alibaba.com/article/2024/01/3bd94d3b-e965-451a-a3ac-bde04b07d465.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

##### ChatDev实验流程

###### 安装步骤：

###### 运行过程：

![](https://oss-ata.alibaba.com/article/2024/01/076342a1-9712-4dd9-a465-ec9ed7db57ae.gif)

ChatDev包含一个仓库（warehouse）目录，上面的命令会先在该目录下创建一个名为puzzle的项目目录。

###### 游戏效果：

![](https://oss-ata.alibaba.com/article/2024/01/6189d9e6-b46b-4b52-bfb9-b05764d81774.gif)

###### 可视化游戏生成过程：

ChatDev中，项目的创建和开发过程涉及多个团队成员或"角色"之间的协作，他们通过对话的方式来生成语言模型的prompts，促进项目的进展。团队成员通过聊天界面编写代码、讨论问题、想法和解决方案。这个项目的创建过程可以通过visualizer进行回放。

![](https://oss-ata.alibaba.com/article/2024/01/42e92816-cdd4-449a-8c8f-30d1c9908914.gif)

#### MetaGPT和ChatDev的异同

MetaGPT和ChatDev都支持自动化软件开发，但在架构设计、技术实现、支持功能等方面存在一些差异。

①MetaGPT通过序列流程显式设计架构；而ChatDev的架构设计是通过生成性基础模型隐式实现的。 ②截至2023年9月19日，MetaGPT的官方代码库目前不支持软件开发的自动化测试。

#### 各种智能体在快速发展

![](https://oss-ata.alibaba.com/article/2024/01/16a0b879-6ed0-4d89-944a-1a81494a5b0d.png?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1600/quality,Q_80/format,webp)

全球范围内，多个AI智能体产品如AiAgent.app和GPT Researcher已被推出，并在媒体报道、行业分析、研究助理等领域获得成功应用。这些智能体设计得足够灵活，能够调用软件应用和硬件设备，大大提升了工作效率和便利性。尽管AI智能体的发展时间短暂，它们迅速在各行业中得到认可。随着大型语言模型（LLMs）的多模态能力和计算力的增强，早年提出的智能体理念得以迅速实现，并广泛应用于多个领域。各种开源AI智能体的出现，加速了技术供应商和创业团队引入智能体的步伐，并帮助更多组织认识到并接受了AI智能体的概念，这可能成为LLMs落地的主要模式，并助力多个行业更好地利用LLMs。

## 结语

LangChain为大型语言模型提供了一种全新的搭建和集成方式，正如乐高积木提供了无尽的创造可能。通过这个强大的框架，我们可以将复杂的技术任务简化，让创意和创新更加易于实现。在第一篇的内容中，我们穿越了LangChain的世界，体验了如同搭建乐高积木般构建语言模型应用的乐趣。从LangChain的核心概念到其在现实世界中人脸问题的智能排查应用，我们见证了这一框架如何助力智能体的创新与成长。

在第二篇的内容中，我们讨论了智能体的发展，目前主要呈现两大方向。首先，我们看到了诸如Gorilla和ToolLLaMa这样的进步，它们通过增强大型语言模型（LLMs）本身的工具使用能力，为我们带来直观、高效的互动体验。这些工具的发展将大语言模型的潜力发挥到极致，为智能体提供了更为强大的支持功能。

另一方向是多代理协同，像MetaGPT和ChatDev这样的系统展示了通过多智能体的合作可以如何高效解决问题。这种多代理模式模拟了人类团队工作的方式，每个智能体扮演特定的角色，共同完成任务。这不仅提高了任务执行的效率，也开启了智能代理未来无限的可能性。

随着技术的不断进化，智能代理正在从单一任务执行者转变为能够协同工作的团队成员。这一转变不仅扩大了智能体在各行各业中的应用范围，也为未来出现的人与智能体之间的互动提供了基础。让我们携手前进，共同迎接智能体技术带来的充满惊喜的新时代。



```





























-----------------------------------------------------------------------------------------------------------------------------------------------------------------

编辑页面： [editor on GitHub](https://github.com/DaemonforY/yongbin.github.io/edit/master/README.md) 

Markdown编辑提示：
```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)

# 数据分析4层次DDPP

*历经20余年，我们似乎终于进入一个真正的数据时代。但当我们在讨论数据分析时，我们究竟在讨论什么？*、
- 凡客当年很高调：我们做的不是电子商务，我们做的是数据分析。Google也吹牛：我们已不需要模型，我们只要数据
- 但Tableau近期和IDC联合对10个国家的1100多位企业管理者做了调查，调研结果表明，有83%的CEO都希望自己的企业能够做到更多的数据驱动。但只有33%能明确的讲清楚业务KPI和数据分析之间的链条。
- 数据分析到底是什么？什么是算法？是工具？是方法论？是业务解决方案？还是某种价值观？
```

