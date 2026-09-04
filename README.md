## Johnny Zhang

**Data / AI engineering — production pipelines, and the instruments that decide whether their output is real.**

数据 / AI 工程 —— 生产管道，以及判断管道输出是否可信的那套仪器。

`English` · [`中文`](#中文)

---

I mostly build the second kind. Most of what ships here exists because a number I trusted turned out to be
wrong, and I wanted the next one to fail loudly instead of quietly.

### Selected work

**[instrument-first](https://github.com/johnnyzhang-eng/instrument-first)** — Verify the instrument before you
charge the failure to the system under test. A measurement-validity checklist for data/ML work, written as a
Claude Code / Codex skill. Every entry is a real failure I booked to the wrong cause first.

**[guardrails-toolkit](https://github.com/johnnyzhang-eng/guardrails-toolkit)** — Turn a lesson learned into a
guardrail that cannot silently rot. Custom semgrep rules, Soda data-quality checks, and lint gates whose
classifiers are locked by offline known-answer selftests, so the arbiter can't drift without CI noticing.

**[bili_stock](https://github.com/johnnyzhang-eng/bili_stock)** — A backtesting framework that *refuses to run*
an experiment which hasn't declared a random-control baseline, an out-of-sample split, and real two-sided costs.
Built after my own results survived only because I hadn't imposed those. It falsified six strategy families,
including the ones I wanted to be true.

**[resume-audit](https://github.com/johnnyzhang-eng/resume-audit)** — Measures what's wrong with a résumé
instead of opining about it: layout metrics, line-break calibration, copy lint. Every rule carries the
measurement that justifies it.

Also here: [investment_research](https://github.com/johnnyzhang-eng/investment_research_2026_05_24) ·
[polypost](https://github.com/johnnyzhang-eng/polypost) ·
[windup-asset-lab](https://github.com/johnnyzhang-eng/windup-asset-lab)

### Day job, so far

**188 merged pull requests** across a production menu-OCR and data pipeline covering ten markets — extraction,
brand entity matching, warehouse write paths, and cost. The ones I'd point at:

- A CI gate that asserts a promote step *actually succeeded*. Five consecutive failed runs had reported green.
- A quality gate found after a 16-hour run produced a 0% pair rate that nobody noticed for a month. It is
  deliberately fail-open — halting the pipeline on a quality warning is a worse failure than the one it catches.
- A batch-transport eligibility gate. The batch API returned 404 on the pinned model, while every read-only
  availability check — model list, capability flags, batch list — kept returning 200. Only the create call refused.

I care about the denominator. Most coverage arguments I've been in were settled by finding out what was
actually in the denominator, not by improving the model.

### Now

Graduating June 2027. Looking for data / AI engineering roles — Shanghai, Hangzhou, or remote-friendly.
Comfortable working entirely in English.

**jingheng_zhang@outlook.com**

---

## 中文

我做的大多是第二种。这里的东西基本都源于同一件事：某个我信过的数字后来被证明是错的，
于是我想让下一个错数**响一点地失败**，而不是安静地混过去。

### 主要作品

**[instrument-first](https://github.com/johnnyzhang-eng/instrument-first)** —— 先验仪器，再给被测系统记账。
数据 / ML 工程的测量效度清单，写成 Claude Code / Codex skill。**每一条都是我先归错因、后来才查出真因的真实事故。**

**[guardrails-toolkit](https://github.com/johnnyzhang-eng/guardrails-toolkit)** —— 把一次教训变成不会静默腐烂的闸口。
自写的 semgrep 规则、Soda 数据质检、以及三个 lint 闸——它们的判定器被离线的已知答案自测锁住，
**判官自己漂移了 CI 会先叫。**

**[bili_stock](https://github.com/johnnyzhang-eng/bili_stock)** —— 一个**拒绝运行**的回测框架：
实验没声明随机对照基线、样本外切分和真实双边成本，它就报错中止。
起因是我自己的结果之所以「成立」，只是因为我没上这几条。**它证伪了六类策略，包括我希望是真的那几类。**

**[resume-audit](https://github.com/johnnyzhang-eng/resume-audit)** —— 量得出简历哪里有问题，而不只是给意见：
版面度量、折行标定、文案 lint。**每条规则都带着支撑它的那次实测。**

还有：[investment_research](https://github.com/johnnyzhang-eng/investment_research_2026_05_24)（A股多策略研究与实盘监控 Dashboard）·
[polypost](https://github.com/johnnyzhang-eng/polypost)（多平台发布 + 发布前合规预检）·
[windup-asset-lab](https://github.com/johnnyzhang-eng/windup-asset-lab)（2D 角色素材审核编辑器）

### 工作

在一条覆盖十个市场的生产菜单 OCR 与数据管道上合并了 **188 个 PR** —— 抽取、品牌实体匹配、数仓写入路径、成本。
最值得一提的三个：

- 一个断言 promote 步骤**真的成功了**的 CI 闸。在此之前，连续五次失败的运行全部报绿。
- 一个质量闸，起因是一次 16 小时的运行产出 0% 配对率，一个月没人发现。
  它**故意 fail-open** —— 因为质量告警去中断管线，会造出一个比原问题更糟的失败模式。
- 一个 batch 传输资格闸。batch 接口在钉住的模型上返回 404，
  而所有只读可用性检查——模型列表、能力标记、batch 列表——**全部返回 200，只有 create 拒绝**。

**我在意分母。** 我经历过的覆盖率争论，绝大多数最后是靠搞清楚分母里到底装了什么解决的，不是靠把模型调好。

### 现在

2027 年 6 月毕业，找数据 / AI 工程方向的岗位 —— 上海、杭州，或可远程。全英文工作环境没问题。

**jingheng_zhang@outlook.com**
