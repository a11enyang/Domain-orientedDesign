大作业1：模板

基于众包的疫情监测与预报系统—需求分析

用于“软件体系结构”设计的资料

2020年2月10日星期一

 

**项目起源和背景：**

本项目的源于李文亮等8位太早的被训诫的医务工作者，所导致的没能及时判断和传递疫情消息，所导致的疫情迅猛扩大。作为事后诸葛，我们客观地要问：1）李文亮错了吗？2）训诫他的警察错了吗？3）当地的官员错了吗？….等等一系列的问题。

也许，人们总期望把某些重大错误或损失的原因，归结于某些人为的因素，让一些人为此而承担所有的责任。然而，我们应当记得“雪崩时，没有一片雪花是无辜的”。也就是说，我们应当建立一个体系或系统，能够让李文亮等8位医生的警告信息、以及更多的病人的信息被更多的专业人士看到，从而发挥作用。避免个别官僚错误的决策，弥补当前病理学(或病毒学)不能及时给出充分的疫情传播理论(例如，是否有人传人？病毒是否具有空气传播的能力等？)

从病人传播的机制看，无论是何种病毒？何种传播途径？只有在一定的时间(短期)和地区内，发生同类病例指数级的病人增长，就极有可能发展为快速传播的疫情。并不用等到所有的病毒机理和传播方式都被研究清楚。

计算机病毒、信息舆情也具有与疾病疫情同样的传播机制和机理。例如，互联网上，计算机病毒传递的速度也是指数级的，不能等到某种计算机病毒(病毒也是一段程序，接受者无法判断其是病毒或有益的程序，当且仅当发现该程序有害时)的特征分析清楚后，才发出警告（例如，不要开机、断网等）。

新闻舆情也是如此，监控某个信息的内容传播点指数级增长时，就说明其信息具有很大的杀伤力（或号召力），就有必要判断该信息的(正面或负面)影响，从而决定是阻断(负面信息)或放任(正面面信息)传播。单纯地，仅仅依赖信息安全警察，依据其内容(当前)对某个人或政府不利就进行删帖或训诫，可能会把实际客观的信息阻断，导致决策失误，因为个体的信息安全警察不能对所有的信息都能准确地判断其(正面或负面)影响力。

因此，无论是病理疫情、计算机病毒疫情、(新闻)信息等舆情，只要其具有自我复制和传播的机制，都不能依靠某个专业人员(例如，医生、疾控中心的专家、新闻检查者、计算机病毒检测软件)的个体专业知识或某个政府官员（例如，领导、警察等）的个人能力，对疫情和舆情做出完全的判断。及早识别(人和计算机)病毒或新闻消息的传播速度和加速度，可以有利于对疫情和舆情的判断和预报。

对此，需要的不仅仅是领域专家(例如，计算机病毒专家、医生或疾病控制专家)，更需要的是一线医生和病人，计算机用户和网管人员、新闻的普通大众接受者和转播者，对当前状态的判断信息。

如果能够以众包形式，及时收集一线人员的获得的这些状态数据，对这些数据进行综合分析，在结合专业（如病例、计算机病毒、新闻舆情等的）知识就可能及早地进行预报。

因此，希望以此病理疫情的众包监测和预报系统的需求分析入手，从非功能(或质量角度)抽象出软件体系结构需求，设计一种适用于多种场合的软件体系结构，可以支撑多种场景的软件部件、产品和系统。开发出“XXX(疫情/舆情)监测和预报系统”的软件生产线和配套的软件开发环境。

美好的愿望始于键盘，我们的第一步是以病毒疫情的数据监测与预报为项目支撑的基础。先写出需求文档(本文档)，为后续的体系结构设计提供一个基础和依据。

 

**项目目的:**

本资料结合2019-2020新冠病毒疫情的情况，提出建立一个基于病人和医生一手资料(简称为众包或众报)传染病人和病情检测，并根据数据判断是否会形成大规模传染，并向决策者和管理者提供预报的软件系统。从而改进现有的信息不同所导致的“李文亮”事件大发生，以及决策者对疫情传播的误判等。提高大疫情的早期快速预判和决策的支持能力。

 

**教学目标：**

本文档为软件工程本科高年级学生和研究生提供一个需求分析文档的样例，并由此，要求学生在此基础上，由学生设计一个“基于众包的疫情监测与预报系统”的体结构。这样的体系结构除了能满足功能需求外，更重要的是要满足非功能(质量)的要求，例如，该系统能否适用于一个地区、国家、国际组织？能否扩展更多的用户角色？是否便于功能扩展？系统在建造过程中的可集成性和可测试性如何？

进一步，作为系统的设计者，特别地要考虑：(1)从商业和公益角度，这类系统的盈利模式和公益作用，如何说服政府和投资者长期投资，如何保证系统长期的运行和升级？（2）该系统是否很容易地改造为类似的系统，例如，（信息）舆情的众包检测和早期预报，计算机病毒攻击众包检测和早期预报等。

由此，学生和老师可以把本资料作为(软件工程理论、软件需求分析、软件体系结构设计、软件过程改进、软件项目实践等)专业课的引导材料。

 

**鼓励创新创业的目标和途径：**

本材料可以用于老师、研究生、本科生进行创新创业项目开展或竞赛的原始参考材料。

北京邮电大学王安生教育基金项目和北京0/1成果转化服务平台分别出资支持，委托“北京邮电大学软件学院双创中心”组织软件学院师生，围绕疫情或紧急事件类型的众包数据收集、早期预报等方面内容，展开相关软件项目的需求分析、体结构设计、原型开发、创新与创业计划。并对项目进行评审，对优秀项目进行奖励。

北京0/1成果转化服务平台将针对优秀的项目中，进行孵化培育。

 



 

 

 

 

基于众包的疫情监测与预报系统

 

 

 

软件需求分析规格说明书

Software Requirements Specification

 

<0.1>

 

<2020/2/10>

 

 

 

<王安生>

 

 Requirements Analysis Engineer

 

 

 

 

为大三《软件体系结构》课程编写 

2020春

 

 



 

# 修订(Revision History)

 

| **日期**  **Date** | **描述**  **Description** | **作者**  **Author** | **注释**  **Comments** |
| ------------------ | ------------------------- | -------------------- | ---------------------- |
| 2020/2/10          | 版本0.1                   | 王安生               | 原始版本               |
|                    |                           |                      |                        |
|                    |                           |                      |                        |
|                    |                           |                      |                        |

 

 

# 文档批准(Document Approval)

 

本文档已经过下列人员和机构的批准：

| **签名**  **Signature** | **名字**  **Printed Name** | **职衔**  **Title** | **日期**  **Date** |
| ----------------------- | -------------------------- | ------------------- | ------------------ |
|                         | 王安生                     | Lead Software Eng.  |                    |
|                         |                            |                     |                    |
|                         |                            |                     |                    |

​                                                



**目录****(Table of Contents)**

 

修订(Revision History)......................................................................................................................... ii

文档批准(Document Approval)........................................................................................................ ii

\1. 引言(Introduction)............................................................................................................................... 1

1.1 目的(Purpose)........................................................................................................................................ 1

1.2 范围(Scope)............................................................................................................................................ 1

1.3 术语定义与缩列语(Definitions, Acronyms, and Abbreviations).............................................. 1

1.4 参考资料(References)......................................................................................................................... 1

1.5 文档概述(Overview)............................................................................................................................ 1

\2. 一般性描述(General Description)............................................................................................... 2

2.1 产品侧面(Product Perspective)....................................................................................................... 2

2.2产品功能( Product Functions).......................................................................................................... 2

2.3 用户特征(User Characteristics)...................................................................................................... 2

2.4一般约束条件(General Constraints).............................................................................................. 3

2.5 假设和依赖条件(Assumptions and Dependencies)........................................................................ 3

\3. 功能需求(Functional Requirements)...................................................................................... 3

3.1周境分析(Context Analysis)............................................................................................................. 3

3.1.1 周境图(Context Diagram)............................................................................................................. 3

3.1.2 第1层数据流(Data flow level 1)................................................................................................. 4

3.1.3 第2层数据流(Data flow level 2)................................................................................................. 4

3.2 功能需求(Functional Requirements).............................................................................................. 4

3.2.1 功能结构(Functional Structure)................................................................................................... 4

3.2.X 功能特征#X <Functional Requirement or Feature #X>............................................................ 4

3.3 用例(Use Cases).................................................................................................................................... 5

3.3.1 用户角色与权限(User Role and Authority )................................................................................ 5

3.3.2角色驱动的用例描述(Use Case Description with Role)............................................................. 6

3.4 类/对象(Classes/Objects)................................................................................................................... 6

3.4.1 <Class / Object #X>........................................................................................................................ 6

\4. 非功能需求(Non-Functional Requirements)....................................................................... 7

4.1 运行时质量需求(Quality Requirements)....................................................................................... 7

4.1.1 性能(Performance)......................................................................................................................... 7

4.1.2 可靠性 /可用性(Reliability/ Availability)................................................................................... 7

4.1.4 密安性(Security)............................................................................................................................. 7

4.2 工程需求(Engineering Requirements)............................................................................................ 7

4.2.1 可维护性(Maintainability)............................................................................................................ 7

4.2.2 可移植性(Portability).................................................................................................................... 7

4.2.3 易测试性(Testability)..................................................................................................................... 7

4.2.4 其它约束条件(other Constraints)............................................................................................... 7

5 数据库需求(Logical Database Requirements)................................................................... 8

5.1 数据库表(Database Tables)................................................................................................................... 8

5.1.X  数据表#X(Data table #X)......................................................................................................... 8

5.2 数据库表关联关系(Relationship of Database Tables)...................................................................... 8

5.3 数据库表与用户角色的关系(Relationship of Database Tables with Users).................................. 8

5.4 数据库规模与性能(Database Size and Performance)....................................................................... 8

附录A (Appendices A)............................................................................................................................... 9

A.1 基本术语和缩列语汇总....................................................................................................................... 9

A.2 文档中的图表目的................................................................................................................................ 9

附录B  附加的参考资料................................................................................................................................. 9

 

 



# 1. 引言(Introduction)

本需求规格说明书(Software Requirement Specification (SRS) )的目的是为系统开发提供一个全面的需求。书写的格式源于IEEE Guide to SRS，但已经进行较大的剪裁。

## 1.1 目的(Purpose)

为后续的软件体系结构设计或系统设计提供基本依据。

本文档的读者，包括：

1.软件系统开发人员

2.系统运维者(部署、运行和维护本系统的机构)

3.疫情监控的政府管理者(最终用户)

4.医生和病人（最终用户）

## 1.2 范围(Scope)

本需求企图定义出相关的软件产品，至少包括：

整体上作为一个系统，分为疫情监测和预报两个子系统。

1）疫情监测产品的目的是，采用众包形式，为病人提供APP，为医生提供APP和PC版软件，能够让医生和病人一旦意识到该病可能具有传染性，即可上报病情案例。

2）预报子系统的产品目的是：依据收集的病人数据，自动或半自动分析，其输出为：是否具有较大面积的 传染性？是否可能出现地区、全国、国际等。

3）与监测和预报相关的报告和图表生成系统。

4）最终用户（病人和医生等）的APP，以及相关联的注册、登陆等管理系统

5）对各医院、地区（市）、省（市）、国家等监测机构的角色和权限管理系统。

 

期望未来的软件系统的各部分（或子系统），可能成为独立的产品。产品间可以通过配置形成一个所期望的系统。系统的运营者可以根据自己的需求，剪裁出自己所需的系统，节约成本。

系统要具有可扩展性，包括对最终用户人数的扩充，以及组织结构的扩展。

系统具有可集成性或组合性，例如，为多个地(市)区的安装的系统，可以组合为一个省级系统；多个省级系统松散的集成为一个国家级的系统。

 

## 1.3 术语定义与缩列语(Definitions, Acronyms, and Abbreviations)

SRS:

 

## 1.4 参考资料(References)

 

*This information may be provided by reference to an appendix or to another document.*

## 1.5 文档概述(Overview)

本文档由  章组成。第2章是一般性的描述，第3章是系统的功能性描述，第4章。。。。

# 2. 一般性描述(General Description)

本项目源于武汉新冠状病毒疫情发展中，由于前期不能准确预报所导致疫情扩大，所带来的经济和社会损失。

本项目的最低目标是构造一个通过(病人和医生)众包的传染病数据收集系统，能够让决策机构(的专业人员)实时监察到实际数据，以实际数据和历史数据为依据，判断和预报是否会发生大的疫情，做的及早预报。

进一步，通过本项目，期望开发通用的众包数据上报APP产品、用户管理产品、预报模型和产品，报告自动生成产品等。从而可以构造出的类似于疫情上报和数据收集、预报等的软件产品部件、产品、以及和组合和集成的系统。

## 2.1 产品侧面(Product Perspective)

开发一个项目，不仅是开发一个可使用的系统。更重要的是要开发出相关的产品、部件，并能够通过对产品和部件的重新配置或集成，形成类似的系统。从而提高软件系统的开发能力、缩短新项目的开发时间。

因此，本项目的需求分析中，要着眼于对产品和模块化功能的描述。可能的产品(部件)有：

1） 通用的查询和图形化的报表自动生成部件；

2） 医务人员用的APP

3） 病人用的APP

4） 能够容纳多个不同的疫情预报模型的框架或模板，允许疫情预报专业人员随时添加其预报的数学模型，而不用改动系统的设计框架。

5） 与地理信息系统的接口；

6） 与政府决策机构所有软件的接口；

7） 为疫情科研人员和软件开发者提供的开发API，以便于以此系统为中心，开发更合理的应用或APP软件

8） 与微博、微信等舆论和通信系统的接口。

9） 其他产品化方面的考虑

## 2.2产品功能( Product Functions)

本软件起码包括：医生和病人的APP，预报模型的框架、疫情报告自动生成器、通用的数据查询接口，以及，可供二次开发人员使用的API等。这些产品功能，需要在设计中进步的抽象。

## 2.3 用户特征(User Characteristics)

本项目最终成果分为：可运行的疫情数据上报、监测和预测系统，以及，可供二次开发人员进行开发的API。对此，用户分为如下几类，且各自有其使用特征。

1） 可运行系统的最终用户，包括：

**医生和病人：**简单实用的移动端的APP，能够按格式化的方式上报数据，也能够按微博的形式发表信息。会用手机APP。

**疫情管理者**：具有适当的权限，能够抽取医生和病人上报的数据。并应有成熟的模型进行预测，并生成可供决策者使用的报告。对计算机使用较熟悉。

**决策者：**能够看到疫情管理者提供的报表，判断当前的疫情，提出应对的措施。并不这些记录在案。向公安等社会管理机构，下达对相关舆情管理的要求。

**疫情预测研究者**：提出不同的预报模型，能够用某种简单的公式描述其模型，并把这些模型容易地集成到系统中，或抽取数据后，用各种模型进行预测，对比分析预测准确度。

**系统运维者：**能够管理系统的日常运行，和错误报告，数据备份等能力。

2） 二次开发者：依据本项目提供的产品和部件，进行新系统的开发，或构造出新得系统，或增加新的产品部件。这类用户是软件开发者。

## 2.4一般约束条件(General Constraints)

本项目需要考虑两种工作方式：

1） 各省、地市可以独立安装和部署自己的系统；数据和管理仅限于管辖区域内使用，对外不公开。

2） 国家需要的数据需要从各省、地市的系统中获得。

3） 在全国范围内，部署一个云服务平台，供各省、地市使用。各省、地市的相互数据隔离。国家层面可以看到任何的数据。

## 2.5 假设和依赖条件(Assumptions and Dependencies)

系统对开发环境、编程语言、后台的数据库系统、操作系统暂时不做要求。

1）但是，设计者要考虑到尽可能使用国产的系统软件、基础软件、开发工具和环境。

2）不同软件开发公司，为各省、地市所开发出的系统之间，数据可以进行交换或转换。

3）疫情的报告数据、使用的名词术语等，要遵循国家卫生与健康委员会的相关标准。

4）数据的保密性和私密性，是需求分析和设计者必须充分考虑的问题。

# 3. 功能需求(Functional Requirements)

本章分析这类系统的功能需求，这些需求需要结合第二章的用户特征，才可能符合用户的实际要求。并进一步引出第4章的的非功能性需求。

功能需求为项目的设计、代码实现和功能测试提供基本的依据。每个功能尽可要：

l 准确(Correct)

l 可追踪(Traceable) (通过业务的分析而获得的，而不是随意添加或定义的额)

l 非歧义的(Unambiguous)：不能含糊不清

l 可验证(Verifiable) (即，能够进行测试)

l 重要性(Prioritized) (按重要性和功能的稳定性，进行区分)

l 完整(Complete)：描述的输入、输出、数据加工，以及出错处理等要完整

l 一致(Consistent)：同一个功能的前后描述不矛盾。

l 唯一标识每个功能要给一个唯一标识，不与其他功能的标识重复

总之，功能描述要注意质量，尽可能让读者完全理解，且没有遗漏。

## 3.1周境分析(Context Analysis)

周境分析的目的是，梳理清楚本系统的定义范围，与外部系统的接口。从业务处理角度提出系统的用户角色、业务加工过程(数据流)。

### 3.1.1 周境图(Context Diagram)



本节要给出周境图分析，表达出本系统的定义范围，与外部系统的接口，以及用户角色。

### 3.1.2 第1层数据流(Data flow level 1)

本节，要从业务处理角度出发，针对用户角色之间，系统和外部接口之间，画出业务加工(处理)过程(数据流)。

注意：作为一个系统，不是只处理一个（主体）业务，应当尽可能画出各种业务对数据的加工和加工顺序。

 

### 3.1.3 第2层数据流(Data flow level 2)

本节，是3.1.2节的细化。对数据流中的加工，进一步的细化。

注意：对于一个复杂的系统，一张细化的图是画不下的，可以分解为若干个“第2层数据流”图。分别按如下编号。

#### 3.1.3.Y第2层数据流--Y

分节，详细画出，第2层数据流中大的模块的细化的数据流。

注意：Y，从1开始编号

 

## 3.2 功能需求(Functional Requirements)

### 3.2.1 功能结构(Functional Structure)

画出功能结构图，该图是从3.1节获得的，是对3.1节的梳理。

注意1：结构图，给出第2层数据流的模块就行。

注意2：除了单纯的结构图，在该结构图上，可以标注出用户角色，这样就相当于全面的用例图。这样的用例图应当与3.3节是一致的。 3.3节的各种用例图应当是该图细化。

然后，分小节，阐述每个功能。

### 3.2.X 功能特征#X <Functional Requirement or Feature #X>

注意：X从1开始编号。X代表第1层的模块。

每个模块的信息如下（可以用表格形式表达）：

 

功能表——第#X项

| 编号                        | #X                           |      |          |                      |
| --------------------------- | ---------------------------- | ---- | -------- | -------------------- |
| (1) 简介(Introduction)      |                              |      |          |                      |
| (2)输入(Inputs)             | 数据形式                     |      | 获取方式 | 模块传递ð  手工输入ð |
| (3)处理(Processing)         |                              |      |          |                      |
| (4)输出(Outputs)            | 数据形式                     |      | 获取方式 | 模块传递ð  手工输入ð |
| (5)出错处理(Error Handling) |                              |      |          |                      |
| (6)相关接口                 | (提示：如果有外部接口，就写) |      |          |                      |

 

接下来，由于每个第1层的每个模块，可能包括若干个第2层的模块，因此，分小节，论述第2层模块的功能需求。每个(第2层数据种的)模块的信息如下（可以用表格形式表达），如下：

#### 3.2.X.Y 功能特征#X #Y<Functional Requirement or Feature #X#Y>

本节给出第#X#Y项的功能要求。

注意：Y从1开始编号。Y代表第2层的模块。

功能表——第#X#Y项

| 编号                        | #X                           |      |          |                            |
| --------------------------- | ---------------------------- | ---- | -------- | -------------------------- |
| (1) 简介(Introduction)      |                              |      |          |                            |
| (2)输入(Inputs)             | 数据形式                     |      | 获取方式 | 模块传递   ð  手工输入   ð |
| (3)处理(Processing)         |                              |      |          |                            |
| (4)输出(Outputs)            | 数据形式                     |      | 获取方式 | 模块传递  ð  手工输入  ð   |
| (5)出错处理(Error Handling) |                              |      |          |                            |
| (6)相关接口                 | (提示：如果有外部接口，就写) |      |          |                            |

 

## 3.3 用例(Use Cases)

用例图是功能与不同用户角色之间的交叉。本节以用户角色为线索，按角色重新梳理不同用例，即，哪种角色使用了哪个功能(见3.2节的)。

### 3.3.1 用户角色与权限(User Role and Authority ) 

在3.1节周境分析和3.2.1节功能结构分析的基础上，重新分析用户的角色，以及每种角色是否有不同的权限。如果一个角色有不同的权限，也要描述出来。

角色的分析与业务流是密切相关的，也可以采用泳道图的方式，通过分析角色之间业务处理关系，而确定出哪些角色是必须的？哪些角色是可以合并的？

例如，张三是一个医院的” 院长”，但他也给病人看病，因此，扮演两个角色“院长”和“医生”。

同一个角色，会有不同的权限，例如，医生分为：主任医师、副主任医生、主治医生和普通医生，掌握的信息是不一样的。

权限表达一个角色对信息的访问权利。信息又分为可写、可读、不可读。

最好是建立一个用角色与权限表。例如，一个病人的信息包括身份（如家庭情况）和病情。医院对病人的身份和病情信息分开进行管理。例如，医生可以不知道病人身份，疾控专家需要知道病人的身份(家庭和流动情况)信息。

因此，对任何一组信息或某项软件功能的操作权限，取决于用户的角色和权限。最好，对所有的功能建立如下的角色和权限表。



| 权限  角色 | 1  可写 | 2  可读 | 3  不可读 | 4    |
| ---------- | ------- | ------- | --------- | ---- |
| 院长       |         |         |           |      |
| 主任医生   |         |         |           |      |
| 主治医生   |         |         |           |      |
| 普通医生   |         |         |           |      |
| 疾控人员   |         |         |           |      |

 

 

### 3.3.2角色驱动的用例描述(Use Case Description with Role)

用例表达系统运行后，不同角色能使用该系统的主要功能的情况。在需求分析阶段，需要站在不同的用户角度，检验所需的功能和使用方式。对此，可以按角色，分类对功能进行关联，画出用例图。也可以按功能，对角色进行梳理。

我们这里给出按角色，对功能进行关联的目录。

#### 3.3.2.Z 用例#Z (Use Case Role#Z)

这里的#Z代表主要的角色，以此进行目录编号。#Z是角色集合(见3.3.1节)中的一个元素。

因此，本节主要画出与角色#Z为主的功能关联关系，也包括与这些功能相关的其他角色。

角色一律用人型符号表达，功能用矩形表达。角色与功能的表达用带箭头的线表达。

箭头表达信息的流向：例如，从角色到功能的单向箭头，表达角色可以向功能输入数据，相反的单向箭头表达功能只向角色输出(展示)数据或信息。自然，双向箭头表示，角色和功能之间的数据是交互的，例如，医生查询和修改一组信息。

 

## 3.4 类/对象(Classes/Objects)

类是是对数据结构以及相关算法的封装。类可以继承、重载，从而扩展和改变原先父类的功能。类内部的方法之间，可以用消息进行数据交换。类之间可以进行建立聚合、关联等关系。因此，产生了基于OO的分析、设计、以及编程、和测试的支持全生命周期的开发方法。

在需求阶段，主要的目的是，抽象出可以复用的基类。这些基类能够被扩展为新的子类。子类代表可以代表一组特定的功能，供各种不同的用户角色使用。

例如，可以把查询一组数据定义为一个基类(父类)，其没有特定的用户角色，或者说，是个通用的数据查询类。然后，可以针对不同的角色进行扩展（或继承），例如，医生用的病情数据查询、病人(家属)用的病情数据查询对象，官员用的，等等。

由此，本节可以依据3.1节给出的功能，对若干个类似功能进行抽象，获得基类，然后，在说明在基类的基础上，扩展出现的子类。下面分小节说明基类的定义，然后，说明其相关的功能需求和用例。

### 3.4.1 <Class / Object #X>

\#X代表类的编号，从#1开始。

#### 3.4.1.1 属性(Attributes)

说明该类中的变量、数据结构的定义。

#### 3.4.1.2 函数/方法(Functions/Methods)

说明对数据进行操作的函数或方法的定义，暂时可以不区分私有或公有函数。

#### 3.4.1.3 功能和用例(Functions/use cases)

对应与3.3节，说明这里所定义的类和其可能的为扩展(继承) 的类，所针对的用户场景或用例。即，哪些用户角色在何种业场景下，会使用这个 类定义的功能。

#### 3.4.1.4 功能组合用例(Use cases with more Objects)

如果一个业务用例或场景，需要多个类按一定的时序组合才能完成，那么，可以用消息顺序(时序)图进行表达。

 

# 4. 非功能需求(Non-Functional Requirements)

非功能需求，是功能之外的需求，也可以成为质量要求。包括系统运行时所表现出质量，工程质量、以及商业质量要求。

这些需求，是设计者选择和设计软件体系结构模式的基本依据。

## 4.1 运行时质量需求(Quality Requirements)

一般的质量要求是指系统运行时所表现出的质量。这是需求阶段最需要考虑的问题。主要包括：

### 4.1.1 性能(Performance)

通过调研用户数量(在线、高峰并发等)，估算出期望的响应时间。支持的并发用户数等。

### 4.1.2 可靠性 /可用性(Reliability/ Availability)

一般用系统的平均无故障时间，7X24小时不间断运行，修复时间、停机时间等表达。

### 4.1.4 密安性(Security)

结合3.3节的用户角色、权限，讨论数据、信息的保密方法，从而给出对系统保密的量化描述。例如，哪些用户角色和何种权限才能访问(查询、修改、删除等)哪些类型的数据。

该需求是数据库需求分析和设计的基本依据。因为只有数据库的数据得到合理的保护，才能达到密安性的要求。

此外，考虑，网络传输过程中对数据和（网页）脚本程序的加密程度的要求。

进一步，考虑系统的防病毒和防止外部进攻的等级要求。

综合上述因素，为设计时，对系统的密安性保护等级提出方案。

## 4.2 工程需求(Engineering Requirements)

一般指软件建造和维护过程中的工程要求，或称为非运行的质量要求。例如，软件是否好修改、好移植等，因为这些要求直接关系当前开发或后续运行、升级维护等成本和服务和质量。这里重点考虑：

### 4.2.1 可维护性(Maintainability)

如何降低软件开发和后续维护、升级的成本。对此，较好的做法是对中间产品，如需求文档、设计文档、代码卷宗、测试用例和报告等质量提出要求。

### 4.2.2 可移植性(Portability)

主要指软件代码向其它平台是否好迁移，如果客户或市场有要求的话。另一方面，指运行中的数据是否好迁移、或转换为用户所期望的形式，或改变用户界面中数据的呈现方式。

### 4.2.3 易测试性(Testability)

从软件体系结构上考虑，系统集成过程中，是否容易集成、测试和定位问题所在。

### 4.2.4 其它约束条件(other Constraints)

主要指，体系结构设计和代码开发中的一些要求，例如，方案必须采用XXX云平台，手机客户端用Java、后台用C++，Web Server用 IIS等。

也包括，是否要与哪些老系统兼容，或能直接使用哪些系统的数据，或与其它系统的接口定义等。

 

# 5 数据库需求(Logical Database Requirements)

本章主要结合第3章的分析，对本系统中所涉及到的数据进行梳理，整理出那些经常参与运算，或不同角色之间进行直接交换或加工后再交换的数据。例如，一个病人的信息，包括基本信息（姓名、年龄、身份证等），但是，如果要计算出其被传染的可能性，就必须知道其最近一段时间内活动的(地理)轨迹。这样，一个病人的信息就包括：基本信息和参与运算的信息。这些信息可以建立成表的形式，在5.1节中表述出来。

在5.1节表述的各种表的基础上，在5.2节，建立这种表之间的关联关系(或实体关系)。从而验证一下提出的信息表是否全面？

这些工作并不是数据库的设计，但是为设计阶段的数据库设计提供基础。关系型数据库设计的重点是消除数据的不一致性，降低数据的冗余等，从而提高数据库的运行效率，提升数据库的易修改、备份、容错等特征。

## 5.1 数据库表(Database Tables)

分小节，说明每个数据库表的属性定义和基本类型要求。

### 5.1.X  数据表#X(Data table #X)

\#X中的X从1开始编号。

## 5.2 数据库表关联关系(Relationship of Database Tables)

用实体关系图画出表与表之间的关联关系的初步要求。

这里不考虑，数据冗余、数据一致性等问题。推迟到设计阶段。

## 5.3 数据库表与用户角色的关系(Relationship of Database Tables with Users)

用实体关系图画出用户角色表与表之间的关联关系。目的是说明，哪些用户可能要从哪些表的哪些字段中取数据。从而验证当前数据库的要求是否能够满足用户用例和场景的要求。

## 5.4 数据库规模与性能(Database Size and Performance)

以及上面数据库表的情况，结合3.3 给出的用例情况，以及4.1.1节用户量和并发量的情况，估算出：

1） 系统运行时，每天可能产生的数据量；

2） 系统运行时，每月可能产生的数据量；

提出，

1） 数据转储备份的时间间隔要求，例如，每个星期进行一次数据转储，降低当前DBMS的压力。

2） 历史数据转储后，进行查询的原则和方法。例如，要查一年前某个病人的数据，而该数据已经转储到备份机器上，提出相应的处理策略要求。（例如，转储后的数据查询响应时间不大于正常情况的2倍）。

从而，一方面补充4.1.1节的性能要求。另一方面，为选择商业DBMS提出要求。

 

# 附录A (Appendices A)

## A.1 基本术语和缩列语汇总

## A.2 文档中的图表目的

 

# 附录B  附加的参考资料

（把用于的资料直接复制在这里，或超链接到相关的文件）

 