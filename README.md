<div style="display: flex; flex-direction: column; justify-content: center; align-items: center">
  <div style="font-size: 22px; margin: 10px 0px"><strong>詹晓秋</strong></div>
  <div style="font-size: 16px;">📱15306598108 | 📧 289463414@qq.com</div>
</div>

### 教育经历

#### 浙江大学 | 机械制造及自动化 | 硕士 | 2018.09 - 2021.03

- GPA：3.38/4.00
- 荣誉/奖项：校一等奖学金

#### 中国计量大学 | 工业工程 | 本科 | 2013.09 - 2017.06

- 荣誉/奖项：院二等奖学金(2013-2016)

- 国际大学生数学建模竞赛二等奖(2016)

- 全国大学生数学建模竞赛省三等奖(2015)

- 英语（CET-6）

### 技术能力

- **语言**：JavaScript/TypeScript/ES6/CSS/HTML
- **框架工具** ：React/Webpack/Git/VSCode
- **工程能力**：模块化重构/代码设计/编码规范/性能优化/监控体系搭建/自动化测试

### 工作经历

#### 群核科技（酷家乐）| 杭州六小龙 | 软件高级开发工程师 | 2021 - 2025（3年）

**核心职责：**

- 负责棚拍影棚页、影棚详情页、镜头设置工具页和管理后台业务的功能迭代与稳定性建设
- 负责办公家具业务功能的开发与稳定性建设，完善办公三维监控体系，统一编码规范

### 项目经历

#### 1、办公易用性技术提升项目 | 2024.05 - 2024.12 | 主负责（P0级）| 预期收入1216万+

#### 项目价值

- 突破CET软件功能壁垒，促成震旦/圣奥千万级续约，完成中小企业市场渗透率提升35%
- 方案设计时长缩短50%，复杂场景操作成功率提升至95%以上，实施设计周期缩短50%
- 打通跨模式办公能力，解决办公工具在云图模式外因功能缺失导致的推广受阻问题

#### 主要技术成果

**主导模式外办公基础功能开发**，包括：

- 模型操作：模型挂载按钮（复制/删除/连续复制等）、场景交互（选中/框选/三轴控件/拖拽等）、参数面板（尺寸/位置/样式修改等）。
- 高级功能：模型快速旋转、文本标记、水平/垂直对齐分布、矩形/线性/环形阵列功能接入、装配连接样式改版。

**技术难点**：

- 需要迁移大量重复性功能代码，工作量极大，新增模式与原业务侵入严重，耦合性高
- 业务逻辑交叉导致故障频出，新业务需穿透多层冗余代码实现适配，产生双向逻辑污染
- 新功能开发依赖源数据层，但是数据无法共享，两种业务形态数据隔离导致无法调用
- 业务时序混乱，目前上游基架无稳定事务执行完成时机

**优化方案**：

##### 1 功能管道化&流式上下文，构建跨模型-场景统一功能总线

- 借鉴**洋葱模型和管道流模型**，将通用操作(复制/删除等)抽象为可插拔处理节点，通过FunctionType标识功能类型，形成功能处理链，构建上下文作为载体管道，实现处理链间数据流传递，实现核心逻辑与扩展处理的**正交解耦**，同时减少代码冗余

##### 2 核心模块重构——基于订阅-派发模式

- 设计**事件驱动的架构模式**，细化业务流程，**提出生命周期概念**，拆分执行时机为**订阅-派发链路**，解耦Application核心模块，**获团队推广**并应用于其他核心场景代码改造
- 引入**可插拔式hook配置**，按功能维度二次拆分代码

##### 3 跨模式数据治理——分层数据备份体系

- 引入**Promise.race+异步任务队列**的超时熔断策略，，保证了依赖的上游状态及时更新，异常拦截率提升至99.8%
- 模式外独立创建**装配数据备份层**，分离底层数据（负责核心数据的存储、转换和校验）与业务操作类（合并/复制/删除等）

#### 2、办公重点客户冲刺计划 | 2022.12 - 2023.08 | 主开发 （P0级）| 跨7敏捷组协同

#### 项目价值

性能优化突破2000㎡大型方案设计瓶颈，（设计+报价方案+一键下单）等一系列功能的落地，助力震旦六月份的成功推广，成功打造行业标杆解决方案，获百丽家居200万+新签合同。

#### 主要技术成果

主导通用性装配检测引擎设计：

**技术难点**：

- **多维度业务形态组合爆炸**：业务对象O(m)×核心处理逻辑O(n)×调用场景O(k)**笛卡尔积式扩展**
- **扩展性差**：每新增业务形态就必须新增一条多维度组合，开发周期长，且代码混乱
- **性能瓶颈**：3000㎡/2300万面片/3GB数据场景下，检测耗时50秒（LOD行为/保存接口占70%）

**优化方案**：

**1 建造者模式-工厂模式结合架构设计**

- **三大抽象工厂**：预处理（模式内外环境适配）/检测单元（按模型类型、检测方法生成检测逻辑）/后处理（按操作类型生成检测结果），解耦业务流程
- **动态调度引擎**：封装上述工厂实例，实现拓展接口(可支持业务模块插拔)，通过输入按需配置组合，引擎按序调度预处理→检测→后处理流程

**2 性能优化突破——基于脏更新过滤的检测前置与增量保存异步逻辑后置的分离优化方法**

- **脏数据标记与缓存**：基于哈希指纹标记脏数据，仅增量送检，将重复计算结果缓存至IndexDB
- **纯前端检测+增量保存**：不依赖后端的纯前端逻辑前置，将增量的保存逻辑后置异步，实现「检测—渲染—存储」结构，优化时间至6s

#### 3、办公稳定性保障项目 | 2023.10 - 2024.06 | 主负责 （P0级）

#### 主要技术成果

- 建立了办公**首个三维监控体系**错误监控、性能监控、业务监控
- 沿用**事件驱动架构模式**，重构退出/进入时机、方案加载等场景核心代码

#### 4、棚拍平台开发 | 2021.09 - 2022.06 | 千万级营收项目 | 软件开发培训生

#### 工作内容/个人职责

- **左侧素材栏改版**
- 主页面(选择影棚页、影棚详情页、镜头设置工具页改版)，负责管理后台系统开发

#### 主要技术方案

- 基于**垂直分层**与**功能隔离的架构思想**，组件分级体系为(原子组件—>业务组件—>页面组件)
- 基于**Redux状态管理更新机制**，将状态分割成不同的切面，进行模块化处理
- 针对动态内容加载场景，结合ResizeObserver和IntersectionObserver实现**精确的按需加载控制**，减少性能消耗
