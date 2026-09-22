# Gagan Khanna

**Analytics and product — I build the analysis and then explain what it means for the decision.**

Computer science background plus MBA training, which mostly shows up as a habit:
I care as much about whether a number is *trustworthy* as about what it says.
Several of the projects below spend as much effort on what the data cannot
support as on what it can.

📍 Mumbai, India

---

## Projects

### [job-finder-ai](https://github.com/gagank87/job-finder-ai)
**An AI job-search pipeline that refuses to lie on your CV.**
Aggregates postings from 7 sources, scores each against a real CV, and drafts
tailored applications with Claude. The interesting part is the guardrail: a
mechanical verification step re-checks every generated claim against the source
CV and rejects fabrications, so the tailoring can rephrase but never invent.
Three front-ends (CLI, Tkinter GUI, headless) over one pipeline, with a
multi-provider LLM fallback chain and sources that degrade honestly — a blocked
scraper reports *why* it skipped instead of silently returning nothing.

`Python` · `Anthropic/Bedrock` · `Selenium` · `BeautifulSoup` · `openpyxl` — 34 modules, ~8,000 LOC

### [mea-passport-grievance-analysis](https://github.com/gagank87/mea-passport-grievance-analysis)
**Why India's passport office answers the wrong complaints.**
Field internship under the Ministry of External Affairs, RPO Mumbai.
Triangulates four evidence streams — social-media grievance mining across
Twitter/Reddit/Quora, a 245-respondent survey, field observation at 7 service
centres, and staff interviews — chosen because each corrects the others' bias.
Finding: the official handle replies to case-status complaints but not to
document questions or appointment-experience criticism, which are the two
cheapest and most *preventive* categories.
Published as methodology and aggregate findings only; no third-party data.

`BERTopic` · `sentence-transformers` · `UMAP` · `HDBSCAN` · `twscrape` · `NLTK`

### [revenue-forecast-diagnostics](https://github.com/gagank87/revenue-forecast-diagnostics)
**A consulting firm missed forecast for 5 straight quarters. It wasn't the model.**
Twelve quarters of forecast, pipeline, deal-outcome and incentive data reconciled
into one diagnostic. Accuracy sat in a 69–72% band nine quarters out of twelve —
too consistent to be variance. Traced to incentive design: the one partner
measured on forecast accuracy hit 92.0%, the seven who weren't averaged 70.2%.

`Excel` (pivots, regression) · `Python`/`openpyxl` — 15-slide deck + 15-sheet model

---

## Background

- **PGDM (MBA)** — Welingkar Institute of Management, Mumbai · 2024–2026
- **BCA, Information Technology** — VIPS, GGSIPU Delhi · 9.08/10
- **Research** — systematic review on the shift from search engines to
  conversational AI search, presented at NASMEI, December 2025 (paper in revision)
- **Certifications** — CS50 (Harvard) · Wipro AI · Bloomberg Finance & ESG · Cisco Cybersecurity

**Tools:** Python · SQL · Power BI · Excel · Pandas · scikit-learn · LangChain ·
Anthropic & OpenAI APIs · Selenium · survey design and statistical testing

---

## How I work

- **Report what the data supports, and say where it stops.** Every project here
  has a stated-limitations section, because a finding without its caveats is
  harder to act on, not easier.
- **Build the guardrail alongside the feature.** The anti-fabrication check in
  `job-finder-ai` and the sanitisation tooling behind
  `mea-passport-grievance-analysis` exist for the same reason.
- **Prefer the honest failure.** A pipeline that reports why a source was
  unavailable beats one that returns an empty result and looks fine.
