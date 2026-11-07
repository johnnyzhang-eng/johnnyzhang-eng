<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,45:7c2d12,100:c2410c&height=120&section=header" />

# Johnny&nbsp;Zhang

**Data / AI engineering — pipelines, and the instruments that decide whether their output is real.**

<img src="https://img.shields.io/badge/ROLE-Data_%2F_AI_Engineering-1e293b?style=for-the-badge&labelColor=0f172a&color=c2410c" />
<img src="https://img.shields.io/badge/FOCUS-Measurement_Validity-1e293b?style=for-the-badge&labelColor=0f172a&color=b45309" />
<img src="https://img.shields.io/badge/GRAD-June_2027-1e293b?style=for-the-badge&labelColor=0f172a&color=475569" />
<img src="https://img.shields.io/badge/BASE-Shanghai_%2F_Hangzhou-1e293b?style=for-the-badge&labelColor=0f172a&color=475569" />

做数据 / AI 工程：搭数据管道，也做用来判断管道产出是否可信的检查工具。<br>
2027 年 6 月毕业，在找上海、杭州的数据开发 / 数仓岗位，实习和校招都考虑。<br>
在七牛云 1024 实训营的开源项目 Windup 里贡献排第二，合并了 99 个 PR。

</div>

---

<div align="center">

### PIPELINES & DATA

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/ClickHouse-FFCC01?style=for-the-badge&logo=clickhouse&logoColor=black" />
<img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white" />
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

### Mostly, I build the instruments

Most of what ships here exists because a number I trusted turned out to be wrong, and I wanted the next one
to fail loudly instead of quietly.

<table>
<tr><td width="50%" valign="top">

#### 🔬 [instrument-first](https://github.com/johnnyzhang-eng/instrument-first)

Verify the instrument before you charge the failure to the system under test. A measurement-validity
checklist for data/ML work. **Every entry is a real failure I first booked to the wrong cause.**

</td><td width="50%" valign="top">

#### 🛡️ [data-guardrails](https://github.com/johnnyzhang-eng/data-guardrails)

Five layers of checks for data work — raw-data quality, report-vs-raw integrity, analytical claims, code
recurrence, decisions. Each checker is locked by known-answer selftests that **run in CI**, so it can't drift
silently. Examples use synthetic food-delivery data.

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
[polypost](https://github.com/johnnyzhang-eng/polypost)

### Open source

#2 contributor to [Windup](https://github.com/1024XEngineer/Windup), a 2D game-character generator from
Qiniu's 1024 engineering camp: **99 merged PRs** (Aug–Sep 2026) across the generation pipeline, 3D-to-2D
rendering and job orchestration, through the v1.0.0 release.

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
