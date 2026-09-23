# Gagan Khanna

**Analytics and product — I build the analysis and then explain what it means for the decision.**

Computer science background plus MBA training, which mostly shows up as a habit:
I care as much about whether a number is *trustworthy* as about what it says.
Several of the projects below spend as much effort on what the data cannot
support as on what it can.

📍 Currently in Mumbai but my heart lives in Pune

---

## Projects

### [job-finder-ai](https://github.com/gagank87/job-finder-ai)
**An AI job-search pipeline that refuses to lie on your CV.**
Aggregates postings from 7 sources, scores each against a real CV, and drafts
tailored applications with Claude. The interesting part is the guardrail: a
mechanical verification step re-checks every generated claim against the source
CV and rejects fabrications, so the tailoring can rephrase but never invent.
Four front-ends (CLI, Tkinter GUI, browser, headless) over one pipeline, with a
multi-provider LLM fallback chain and sources that degrade honestly — a blocked
scraper reports *why* it skipped instead of silently returning nothing. The web
front-end is multi-user: accounts, per-user data isolation, and bring-your-own
API keys that never fall back to a shared server credential.

`Python` · `Anthropic/Bedrock` · `FastAPI` · `SQLite` · `Selenium` · `BeautifulSoup` · `openpyxl` — 38 modules, ~9,200 LOC

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

### [operational-risk-frameworks](https://github.com/gagank87/operational-risk-frameworks)
**Two operational-risk frameworks where every control has a test that can fail.**
One for a credit-data platform under a T+3 regulatory SLA, one for a Salesforce
CRM ticketing operation with incident handling outsourced to a vendor. Risks are
placed on the operating flow before they're scored, controls are classified by
*when* they act rather than just described, and a traceability map ties all 15
risks to the tests that verify them. Detectability is scored as a third axis
beside likelihood and impact — two risks with the same score aren't equally
dangerous if one of them hides until the deadline has passed.

`Power BI` (4 dashboard pages) · `Figma` · `Excel` — 25pp of framework, 24 controls and tests

### [jiosaavn-review-sentiment](https://github.com/gagank87/jiosaavn-review-sentiment)
**A 100M-user music app has more unhappy reviewers than happy ones. Sentiment says
that much; clustering says what to fix.**
400 Indian app-store reviews scored with a multilingual model — because these
reviews are routinely Hinglish and an English-only classifier reads them as
neutral noise — then the 187 negative ones embedded and clustered. Monetisation
and reliability turn out to be 81% of the complaints; content gaps, the expensive
thing to fix, are the smallest cluster. The README argues *against* its own
headline number: the two stores were sampled with different sort orders, so the
46.8% negative rate is biased upward and the cluster proportions are the
defensible output.

`transformers` (XLM-R) · `sentence-transformers` · `KMeans` · `Figma` — 12-slide deck + 3 notebooks

---

## Background

- **PGDM (MBA)** — Welingkar Institute of Management, Mumbai · 2024–2026 · 8.19/10
- **BCA, Information Technology** — VIPS, GGSIPU Delhi · 2019-2022 · 9.08/10
- **Research** — systematic review on the shift from search engines to
  conversational AI search, presented at NASMEI, December 2025 (paper in revision)
- **Certifications** — CS50 (Harvard) · Wipro AI · Bloomberg Finance & ESG · Cisco Cybersecurity

**Tools:** Python · SQL · Power BI · Excel · Pandas · scikit-learn · MS Office · LangChain ·
Anthropic & OpenAI APIs · Selenium · survey design and statistical testing

---

## How I work

- **Report what the data supports, and say where it stops.** Every project here
  has a stated-limitations section, because a finding without its caveats is
  harder to act on, not easier.
- **Prefer the honest failure.** A pipeline that reports why a source was
  unavailable beats one that returns an empty result and looks fine.
