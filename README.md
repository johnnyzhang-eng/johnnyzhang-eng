<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,45:7c2d12,100:c2410c&height=200&section=header&text=Johnny%20Zhang&fontSize=62&fontColor=ffffff&fontAlignY=34&desc=DATA%20%2F%20AI%20ENGINEERING%20%E2%80%94%20PIPELINES%2C%20AND%20THE%20INSTRUMENTS%20THAT%20CHECK%20THEM&descSize=14&descAlignY=55&animation=fadeIn" />

<img src="https://img.shields.io/badge/ROLE-Data_%2F_AI_Engineering-1e293b?style=for-the-badge&labelColor=0f172a&color=c2410c" />
<img src="https://img.shields.io/badge/FOCUS-Measurement_Validity-1e293b?style=for-the-badge&labelColor=0f172a&color=b45309" />
<img src="https://img.shields.io/badge/GRAD-June_2027-1e293b?style=for-the-badge&labelColor=0f172a&color=475569" />
<img src="https://img.shields.io/badge/BASE-Shanghai_%2F_Hangzhou-1e293b?style=for-the-badge&labelColor=0f172a&color=475569" />

**[`English`](#i-mostly-build-the-second-kind) · [`中文`](#中文)**

</div>

---

<div align="center">

### PIPELINES & DATA

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/ClickHouse-FFCC01?style=for-the-badge&logo=clickhouse&logoColor=black" />
<img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/Apache_Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white" />
<img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=FF9900" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />

### EVALUATION & QUALITY

<img src="https://img.shields.io/badge/pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white" />
<img src="https://img.shields.io/badge/Semgrep-1B2B34?style=for-the-badge&logo=semgrep&logoColor=00C853" />
<img src="https://img.shields.io/badge/Soda-6C4EE3?style=for-the-badge&logo=databricks&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" />
<img src="https://img.shields.io/badge/LLM--as--Judge-c2410c?style=for-the-badge&logo=openaigym&logoColor=white" />

### MODELS & VISION

<img src="https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" />
<img src="https://img.shields.io/badge/Vertex_AI-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white" />
<img src="https://img.shields.io/badge/OpenRouter-1E293B?style=for-the-badge&logo=openai&logoColor=white" />
<img src="https://img.shields.io/badge/Qwen-615CED?style=for-the-badge&logo=alibabacloud&logoColor=white" />

### DELIVERY

<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/ECharts-AA344D?style=for-the-badge&logo=apacheecharts&logoColor=white" />
<img src="https://img.shields.io/badge/Cloudflare_Pages-F38020?style=for-the-badge&logo=cloudflare&logoColor=white" />

</div>

---

### I mostly build the second kind

Most of what ships here exists because a number I trusted turned out to be wrong, and I wanted the next one
to fail loudly instead of quietly.

<table>
<tr><td width="50%" valign="top">

#### 🔬 [instrument-first](https://github.com/johnnyzhang-eng/instrument-first)

Verify the instrument before you charge the failure to the system under test. A measurement-validity
checklist for data/ML work. **Every entry is a real failure I first booked to the wrong cause.**

</td><td width="50%" valign="top">

#### 🛡️ [guardrails-toolkit](https://github.com/johnnyzhang-eng/guardrails-toolkit)

Turn a lesson learned into a guardrail that cannot silently rot. Semgrep rules, Soda checks, and lint gates
locked by offline known-answer selftests — **the arbiter can't drift without CI noticing.**

</td></tr>
<tr><td width="50%" valign="top">

#### 📉 [bili_stock](https://github.com/johnnyzhang-eng/bili_stock)

A backtester that *refuses to run* an experiment with no random-control baseline, no out-of-sample split,
and no real two-sided costs. **It falsified six strategy families, including the ones I wanted to be true.**

</td><td width="50%" valign="top">

#### 📄 [resume-audit](https://github.com/johnnyzhang-eng/resume-audit)

Measures what's wrong with a résumé instead of opining about it — layout metrics, line-break calibration,
copy lint. **Every rule carries the measurement that justifies it.**

</td></tr>
</table>

Also here: [investment_research](https://github.com/johnnyzhang-eng/investment_research_2026_05_24) ·
[polypost](https://github.com/johnnyzhang-eng/polypost) ·
[windup-asset-lab](https://github.com/johnnyzhang-eng/windup-asset-lab)

### Day job, so far

**188 merged pull requests** across a production menu-OCR and data pipeline covering ten markets — extraction,
brand entity matching, warehouse write paths, and cost. The three I'd point at:

| | What it caught |
|---|---|
| **A CI gate** | Asserts a promote step *actually succeeded*. Five consecutive failed runs had reported green. |
| **A quality gate** | Found after a 16-hour run produced a 0% pair rate that nobody noticed for a month. Deliberately fail-open — halting a pipeline on a quality warning is a worse failure than the one it catches. |
| **A transport gate** | The batch API returned 404 on the pinned model while every read-only check — model list, capability flags, batch list — kept returning 200. Only the create call refused. |

**I care about the denominator.** Most coverage arguments I've been in were settled by finding out what was
actually in the denominator, not by improving the model.

### Now

Graduating **June 2027**. Looking for data / AI engineering roles — Shanghai, Hangzhou, or remote-friendly.
Comfortable working entirely in English.

<a href="mailto:jingheng_zhang@outlook.com"><img src="https://img.shields.io/badge/jingheng__zhang@outlook.com-c2410c?style=for-the-badge&logo=maildotru&logoColor=white" /></a>

---

## 中文

我做的大多是第二种。这里的东西基本都源于同一件事：**某个我信过的数字后来被证明是错的**，
于是我想让下一个错数响一点地失败，而不是安静地混过去。

<table>
<tr><td width="50%" valign="top">

#### 🔬 [instrument-first](https://github.com/johnnyzhang-eng/instrument-first)

先验仪器，再给被测系统记账。数据 / ML 工程的测量效度清单。
**每一条都是我先归错因、后来才查出真因的真实事故。**

</td><td width="50%" valign="top">

#### 🛡️ [guardrails-toolkit](https://github.com/johnnyzhang-eng/guardrails-toolkit)

把一次教训变成不会静默腐烂的闸口。semgrep 规则、Soda 质检、三个 lint 闸，
判定器被离线已知答案自测锁住 —— **判官自己漂移了 CI 会先叫。**

</td></tr>
<tr><td width="50%" valign="top">

#### 📉 [bili_stock](https://github.com/johnnyzhang-eng/bili_stock)

一个**拒绝运行**的回测框架：没声明随机对照基线、样本外切分和真实双边成本，就报错中止。
**它证伪了六类策略，包括我希望是真的那几类。**

</td><td width="50%" valign="top">

#### 📄 [resume-audit](https://github.com/johnnyzhang-eng/resume-audit)

量得出简历哪里有问题，而不只是给意见 —— 版面度量、折行标定、文案 lint。
**每条规则都带着支撑它的那次实测。**

</td></tr>
</table>

### 工作

在一条覆盖十个市场的生产菜单 OCR 与数据管道上合并了 **188 个 PR** —— 抽取、品牌实体匹配、数仓写入路径、成本。
最值得一提的三个：

| | 它拦住了什么 |
|---|---|
| **一个 CI 闸** | 断言 promote 步骤**真的成功了**。在此之前，连续五次失败的运行全部报绿。 |
| **一个质量闸** | 起因是一次 16 小时的运行产出 0% 配对率，一个月没人发现。它**故意 fail-open** —— 质量告警去中断管线，会造出一个比原问题更糟的失败模式。 |
| **一个传输资格闸** | batch 接口在钉住的模型上返回 404，而所有只读检查——模型列表、能力标记、batch 列表——**全部返回 200，只有 create 拒绝**。 |

**我在意分母。** 我经历过的覆盖率争论，绝大多数最后是靠搞清楚分母里到底装了什么解决的，不是靠把模型调好。

### 现在

**2027 年 6 月毕业**，找数据 / AI 工程方向的岗位 —— 上海、杭州，或可远程。全英文工作环境没问题。

<a href="mailto:jingheng_zhang@outlook.com"><img src="https://img.shields.io/badge/jingheng__zhang@outlook.com-c2410c?style=for-the-badge&logo=maildotru&logoColor=white" /></a>
