<div style="display: flex; flex-direction: column; justify-content: center; align-items: center">
  <div style="font-size: 22px; margin: 10px 0px"><strong>Zhan Xiaoqiu</strong></div>
  <div style="font-size: 16px; margin: 2px 0px 27px 0">📱15306598108 | 📧 289463414@qq.com</div>
</div>

### Education

#### Zhejiang University - M.Eng., Mechanical Manufacturing and Automation | 2018.09 - 2021.03

- GPA：3.38/4.00
- First-Class Scholarship

#### China Jiliang University — B.Eng., Industrial Engineering | 2013.09 - 2017.06

- Second-Class Scholarship (2013–2016)
- International Mathematical Contest in Modeling, Second Prize (2016)
- National College Mathematical Modeling Contest, Provincial Third Prize (2015)
- English: CET-6

### Technical Skills

- **Programming Language**：JavaScript/TypeScript/CSS/HTML
- **Frameworks/Tools** ：React/Redux/Webpack

### Work Experience

#### Kujiale (Coohom) — Senior Frontend Engineer | 2021 – 2025 (3 yrs) | Hangzhou

- Led frontend architecture and complex problem solving for the office furniture business; solved core pain points via systematic design
- Owned feature iteration and stability for the Photo Studio Platform (studio pages/admin console)

### Projects

#### 1 Office Usability Technical Uplift | 2024.05 – 2024.12 | Owner (P0) | Expected revenue: ¥12.16M+

#### Business impact:

- Broke functional barriers vs. CET software; enabled 8-figure renewals with AURORA and SUNON
- Cut solution design time by 50%; raised success rate for complex scenarios to 95%+; halved implementation cycle

#### Key contributions

**1.1 Feature Parity with Competitors & Enhanced Extensibility for Office Workflows
Challenges**

**Challenges**

- Third-party business logic lacks clear separation of concerns, blurring modular boundaries and making third-party capability extensions difficult.
- Absence of a unified abstraction layer for operation logic leads to tight coupling between business logic and specific type implementations, causing significant code duplication.

**Technical Solution & Outcomes**

##### 1.1.1 Dynamic Layered Architecture Based on the Onion Model

- Designed an onion-model middleware mechanism to enable bidirectional processing and improve extensibility.
- Implemented dynamic initialization and on-demand creation via the Proxy pattern to reduce memory footprint and lower the barrier for third-party integration.
- Built end-to-end tracing to enhance framework stability and expedite issue diagnosis.

**Tech Stack**：Onion model / Proxy pattern / React / Redux

**1.2 Office System Stability Enhancement**

**Challenges**

- Office workflows heavily depend on complex lifecycle management, with extensive business logic embedded in each lifecycle stage, creating significant stability risks.

**Technical Solution & Outcomes**

##### 1.2.1 Lifecycle-Based Event-Driven Architecture

- Converted lifecycle stages into events and introduced function-signature-driven hook registration to standardize partner integrations, implementing a publish-subscribe model.
- Built a task scheduling container with asynchronous concurrency control, timeout retries, and unified error handling as defensive measures to maintain scheduling consistency.

**Tech Stack**：Publish-Subscribe / Async Concurrency Control

#### 2 Office Key Account Sprint | 2022.12 – 2023.08 | Lead Developer (P0) | Coordinated 7 Agile Squads

#### Business Impact

- Closed a ¥2M+ contract with Belle Home; weekly active users of the ordering feature rose from 200 to 8,000.
- Cracked large-plan (2,000㎡) design bottlenecks, cutting detection time from 45s to 12s.
- Kept scene interactions available during assembly checks, preserving a smooth user experience.

#### Key Technical Outcome – Generalized Assembly Inspection Engine

**Challenges**

- User mis-operations were not captured, leading to downstream data errors and financial risk.
- Detection on 2,000㎡ plans took up to 45 seconds, causing the interface to appear frozen and degrading user experience.

**Technical Solution & Outcomes**

##### 1.1 Assembly Inspection Engine

- Combined Strategy, Builder, and Factory patterns to construct a three-layer inspection pipeline (preprocessing / detection / merge) that supports dynamic logic swaps.
- Used the Strategy pattern to encapsulate variable algorithms, the Factory pattern to create standardized components, and the Builder pattern to orchestrate the pipeline.

##### 1.2 Incremental Detection Strategy

- Leveraged Decorator and Proxy patterns to track model property changes and aggregate a dirty set as detection targets.
- Applied time slicing with timeout circuit breakers to schedule detection tasks and prevent main-thread blocking.
  
**Tech Stack**：Strategy / Factory / Builder / Decorator / Time Slicing / Redux

#### 3 Photo Studio Platform Development | 2021.09 – 2022.06 | 8-figure Revenue Project

#### Responsibilities

- Revamped the left-hand asset panel
- Led redesigns for the main pages (studio selection, studio details, lens configuration) and built the admin console

#### Key Technical Outcomes

- Adopted Redux slice-based state management to isolate state by feature
- Implemented scroll-driven tiered loading with double buffering for rapid viewport loading and proactive prefetching

**Tech Stack**：React/React-Redux
