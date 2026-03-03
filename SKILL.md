---
name: research-knowledge-super-skill
description: Comprehensive research and knowledge management skill merging Perplexity Computer's research, data exploration, statistical analysis, and visualization skills with Claude Code's tapestry knowledge graphs, article extraction, content research, brainstorming, RAG system building, and prompt engineering. Covers deep research workflows, knowledge graph construction, academic research, data analysis, statistical methods, content synthesis, and AI-powered information retrieval. Use for research projects, literature reviews, data analysis, knowledge management, competitive research, or any investigation requiring deep synthesis.
license: MIT
metadata:
  author: get-zeked
  version: '1.0'
---

# Research & Knowledge Super-Skill

A unified research and knowledge management system merging deep research workflows, data profiling, statistical methods, visualization, knowledge graph construction, content extraction, RAG systems, brainstorming, and iterative learning into a single actionable playbook.

---

## Table of Contents

1. [Gap Analysis: Perplexity Computer vs Claude Code Skills](#1-gap-analysis-perplexity-computer-vs-claude-code-skills)
2. [Research Methodology & Workflows](#2-research-methodology--workflows)
3. [Knowledge Graph Construction](#3-knowledge-graph-construction)
4. [Content Extraction & Synthesis](#4-content-extraction--synthesis)
5. [Data Exploration & Profiling](#5-data-exploration--profiling)
6. [Statistical Analysis & Methods](#6-statistical-analysis--methods)
7. [Data Visualization & Communication](#7-data-visualization--communication)
8. [Data Validation & Quality Assurance](#8-data-validation--quality-assurance)
9. [Creative Ideation & Brainstorming](#9-creative-ideation--brainstorming)
10. [RAG Systems & AI-Powered Research](#10-rag-systems--ai-powered-research)
11. [Iterative Learning & Feedback](#11-iterative-learning--feedback)
12. [Unique Perplexity Computer Capabilities](#12-unique-perplexity-computer-capabilities)
13. [Research Templates & Frameworks](#13-research-templates--frameworks)

---

## 1. Gap Analysis: Perplexity Computer vs Claude Code Skills

Understanding where each platform excels helps route tasks to the right approach.

| Capability | Perplexity Computer | Claude Code (Tapestry ecosystem) | Combined Advantage |
|---|---|---|---|
| **Live web search** | Native, real-time, multi-source | None (static training data) | Perplexity for current facts |
| **Academic search** | Dedicated academic vertical | None natively | Perplexity for papers/citations |
| **Social media search** | X/Twitter search built-in | None | Perplexity for trend monitoring |
| **Knowledge graph construction** | Not native | Tapestry skill (linked entities from docs) | Claude for local doc synthesis |
| **Article extraction** | fetch_url with LLM processing | article-extractor + reader/trafilatura tools | Both; Claude tools for batch processing |
| **YouTube transcript extraction** | No yt-dlp; fetch transcript endpoint | yt-dlp + VTT deduplication pipeline | Claude for video corpus |
| **Data exploration (CSV/SQL)** | Full Python/SQL environment | Bash tools | Perplexity for live analysis |
| **Statistical analysis** | Full scipy/statsmodels/numpy | Limited to scripting | Perplexity for serious stats |
| **Data visualization** | matplotlib/seaborn/plotly | Bash + Python scripts | Perplexity produces rendered charts |
| **Brainstorming/design** | Can brainstorm; no hard-gate | Hard-gate design-before-code discipline | Claude for disciplined ideation |
| **RAG evaluation** | Can build/evaluate RAG pipelines | rag_evaluator.py scripts | Both; different strengths |
| **Prompt engineering** | Inline; no dedicated optimizer | prompt_optimizer.py scripts | Claude for systematic optimization |
| **Iterative learning plans** | Not native | Ship-Learn-Next planner | Claude for action plan generation |
| **External integrations** | 400+ connected services | File system / local tools | Perplexity for live external data |
| **Multi-agent parallelism** | Subagent spawning | Single conversation | Perplexity for parallel research |
| **Memory across sessions** | memory_search tool | CLAUDE.md / project context | Perplexity for persistent memory |
| **Content calendar / SEO** | Not native | content-creator skill | Claude for content workflows |
| **PDF processing** | pdf skill (extract, merge, OCR) | pdftotext via bash | Perplexity for richer PDF manipulation |

**Routing Decision Rule**:
- Current information, live data, external APIs → **Perplexity Computer**
- Local file corpus, video transcripts, iterative plans, prompt tuning → **Claude Code**
- Statistical analysis, visualization, data validation → **Perplexity Computer** (full Python env)
- Knowledge graph from your documents, action planning, RAG evaluation → **Claude Code**

---

## 2. Research Methodology & Workflows

### 2.1 The Research Hierarchy

Before launching any research task, establish the question tier:

| Tier | Question Type | Approach |
|---|---|---|
| **Tier 1** | Single verifiable fact | One search; cite source |
| **Tier 2** | Comparative analysis | Parallel searches; synthesis table |
| **Tier 3** | Investigative / exploratory | Iterative search; subagent parallelism |
| **Tier 4** | Literature review / meta-analysis | Academic search; citation network |
| **Tier 5** | Strategic intelligence | Competitive research; 400+ integrations |

### 2.2 Deep Research Workflow (Perplexity Computer)

This workflow applies to Tier 3–5 questions requiring synthesis across many sources.

#### Phase 1: Orientation (5–10 minutes)
1. **Formulate 3 seed queries** — broad, medium, and specific versions of the question
2. **Run parallel searches** — use `search_web` with all three queries simultaneously
3. **Identify authoritative sources** — note publishers, institutions, primary data owners
4. **Map the knowledge landscape** — what is known, disputed, unknown, or recent?

#### Phase 2: Deep Dive (15–45 minutes)
1. **Fetch primary sources** — use `fetch_url` on authoritative URLs (not aggregators)
2. **Cross-reference claims** — any fact cited by only one source is provisional
3. **Academic layer** — use `search_vertical(vertical="academic")` for peer-reviewed material
4. **Social layer** — use `search_social` for real-time discourse and emerging viewpoints
5. **Save intermediate findings** — write structured notes with source URLs to workspace

#### Phase 3: Synthesis (10–20 minutes)
1. **Build a claims registry** — list all factual assertions with their source strength
2. **Identify consensus vs. contested areas** — where do sources agree vs. diverge?
3. **Flag recency of information** — is this 2024 data or 2020 data?
4. **Draft the research brief** using the template in §13.1

#### Phase 4: Quality Check
1. Verify every quantitative claim against its source
2. Check that primary sources (not aggregators) are cited for key data
3. Apply the survivorship bias check: who is NOT in these sources?
4. Rate confidence: High (multiple primary sources) / Medium (one primary) / Low (secondary only)

### 2.3 Parallelized Subagent Research

For large research tasks (10+ entities, multiple regions, multi-faceted topics):

```
Master Agent Plan:
├── Subagent A: Topic domain X (searches + saves findings to workspace/research-A.json)
├── Subagent B: Topic domain Y (searches + saves findings to workspace/research-B.json)
├── Subagent C: Collect verified image/media URLs
└── Master Agent: Reads all workspace files, synthesizes, builds final artifact
```

**Rules for parallelization:**
- Each subagent writes to a unique filename (never overwrite)
- Subagents include source URLs for every fact
- Master agent does NOT re-research; only synthesizes
- Never build the final asset before all research files are complete

### 2.4 Research Continuity Across Sessions

At the start of any research-heavy task:
1. Search memory for prior work on the same topic
2. Read relevant workspace files from previous sessions
3. Build on prior findings rather than starting fresh
4. Note what changed since the last research run (date-sensitive facts)

### 2.5 Content Research Workflow (SEO-Aware)

When research feeds into content creation:

**Step 1: Keyword research**
- Identify primary keyword (target 500–5,000 monthly searches)
- Find 3–5 secondary keywords
- Compile 10–15 LSI (latent semantic indexing) terms

**Step 2: Competitive content audit**
- Search for top-ranking articles on the primary keyword
- Identify: what they cover, what they miss, what angle is uncontested
- Map the content gap your piece will fill

**Step 3: Authoritative source collection**
- For each major claim, identify at least one primary source
- Prefer: government data, peer-reviewed studies, official reports, primary news

**Step 4: Content brief**
- Target word count: 1,500–2,500 for comprehensive coverage
- Outline: intro → problem/context → 3–5 key sections → conclusion with CTA
- Include keyword in title, first paragraph, 2–3 H2 headings

### 2.6 Competitive Research Framework

| Step | Action | Tool |
|---|---|---|
| 1. Identify competitors | Search for market participants | `search_web` |
| 2. Profile each competitor | Fetch their about, pricing, features pages | `fetch_url` |
| 3. Sentiment monitoring | Search social for brand mentions | `search_social` |
| 4. Academic / patent scan | Search for IP, research publications | `search_vertical(academic)` |
| 5. Synthesize battlecard | Compare features, pricing, positioning | Write to workspace |

---

## 3. Knowledge Graph Construction

*(From Tapestry — transforms documents into linked knowledge networks)*

### 3.1 What Is a Knowledge Graph in This Context?

A knowledge graph connects entities (people, concepts, events, places, products) extracted from content — articles, PDFs, videos, research papers — into a structured network of relationships. Unlike a flat summary, a knowledge graph lets you:
- See which concepts are central vs. peripheral
- Trace evidence chains from claims back to sources
- Identify gaps in your research coverage
- Merge knowledge from multiple documents

### 3.2 Tapestry Workflow: Extract → Link → Plan

The Tapestry skill orchestrates the full knowledge extraction pipeline:

```
Input URL (YouTube / Article / PDF)
        ↓
   [Detect Content Type]
        ↓
   [Extract Content]
   ├── YouTube → yt-dlp + VTT deduplication
   ├── Article → reader / trafilatura / curl fallback
   └── PDF → pdftotext / poppler
        ↓
   [Save Clean Text to File]
        ↓
   [Create Ship-Learn-Next Action Plan]
        ↓
   Output: content_file.txt + action_plan.md
```

**Trigger phrases**: "tapestry [URL]", "weave [URL]", "make this actionable", "extract and plan [URL]"

### 3.3 Entity Extraction Protocol

When building a knowledge graph from a document corpus:

**Step 1: Identify entity types**
```
Person      → researchers, authors, executives, historical figures
Organization → companies, institutions, government bodies
Concept     → theories, methodologies, frameworks, products
Event       → conferences, publications, incidents, milestones
Place       → countries, cities, labs, markets
Claim       → factual assertions with confidence levels
```

**Step 2: Extract relationships**
```
X AUTHORED Y         (Person → Document)
X FOUNDED Y          (Person → Organization)
X INTRODUCED Y       (Organization → Concept)
X CONTRADICTS Y      (Claim → Claim)
X CITES Y            (Document → Document)
X APPLIES_TO Y       (Concept → Domain)
X PRECEDED Y         (Event → Event)
```

**Step 3: Assign source provenance**
Every entity and relationship must carry:
- Source document
- Page / timestamp reference
- Confidence level (High / Medium / Low)
- Date of information

**Step 4: Identify clusters and gaps**
- Clusters = densely connected subgraphs (core topics)
- Isolated nodes = unexplored areas
- Missing links = research questions for the next iteration

### 3.4 Knowledge Graph Output Format

```markdown
## Knowledge Graph: [Topic]

### Core Entities
| Entity | Type | Connections | Key Source |
|--------|------|-------------|------------|
| [Name] | Person | 14 | [URL] |
| [Name] | Concept | 22 | [URL] |

### Key Relationships
- [Entity A] **DEVELOPED** [Entity B] (Source: [doc], confidence: High)
- [Entity C] **CONTRADICTS** [Entity D] (Source: [doc], confidence: Medium)

### Clusters
1. **Cluster 1: [Label]** — entities: A, B, C, D
2. **Cluster 2: [Label]** — entities: E, F, G

### Research Gaps
- [ ] No sources on the relationship between X and Y
- [ ] Only one low-confidence source for claim Z
```

### 3.5 Multi-Document Synthesis

When merging knowledge from 5+ documents:

1. **Extract entity lists** from each document independently
2. **Deduplicate entities** — resolve synonyms (e.g., "ML" = "machine learning")
3. **Merge relationship graphs** — note when documents agree, conflict, or are silent
4. **Weight by source authority** — peer-reviewed > primary news > blog > forum
5. **Build the unified graph** — write to a structured workspace file
6. **Identify the consensus view** vs. the contested frontier

---

## 4. Content Extraction & Synthesis

### 4.1 Article Extraction

**Tool priority order:**
1. `reader` (Mozilla Readability CLI) — best all-around
2. `trafilatura` (Python) — best for blogs, news, non-English
3. `fetch_url` with LLM prompt — best for Perplexity Computer context
4. `curl` + HTMLParser — fallback, less accurate

**Installation:**
```bash
# Option 1: reader (npm)
npm install -g @mozilla/readability-cli

# Option 2: trafilatura (pip)
pip3 install trafilatura
```

**Extraction workflow:**
```bash
# With reader
reader "https://example.com/article" > temp_article.txt
TITLE=$(head -n 1 temp_article.txt | sed 's/^# //')

# With trafilatura
TITLE=$(trafilatura --URL "$URL" --json | python3 -c "import json, sys; print(json.load(sys.stdin).get('title', 'Article'))")
trafilatura --URL "$URL" --output-format txt --no-comments > temp_article.txt

# Clean filename
FILENAME=$(echo "$TITLE" | tr '/' '-' | tr ':' '-' | tr '?' '' | cut -c 1-80 | sed 's/ *$//')
mv temp_article.txt "${FILENAME}.txt"
```

**What gets removed by article extractors:**
- Navigation menus and headers/footers
- Ads and promotional banners
- Newsletter signup forms
- Related-articles sidebars
- Social media sharing buttons
- Cookie consent overlays

### 4.2 YouTube Transcript Extraction

**Full workflow:**
```bash
VIDEO_URL="https://www.youtube.com/watch?v=XXXXX"

# 1. Get video title for filename
VIDEO_TITLE=$(yt-dlp --print "%(title)s" "$VIDEO_URL" | tr '/' '_' | tr ':' '-')

# 2. Check available subtitles
yt-dlp --list-subs "$VIDEO_URL"

# 3. Try manual subtitles first (highest quality)
yt-dlp --write-sub --skip-download --output "transcript_temp" "$VIDEO_URL"

# 4. Fallback: auto-generated subtitles
yt-dlp --write-auto-sub --skip-download --sub-langs en --output "transcript_temp" "$VIDEO_URL"

# 5. Deduplicate and clean VTT → plain text
python3 -c "
import sys, re
seen = set()
vtt_file = 'transcript_temp.en.vtt'
with open(vtt_file, 'r') as f:
    for line in f:
        line = line.strip()
        if line and not line.startswith('WEBVTT') and '-->' not in line:
            clean = re.sub('<[^>]*>', '', line)
            clean = clean.replace('&amp;', '&').replace('&gt;', '>').replace('&lt;', '<')
            if clean and clean not in seen:
                print(clean)
                seen.add(clean)
" > "${VIDEO_TITLE}.txt"

# 6. Cleanup
rm -f transcript_temp.en.vtt
```

**Fallback: Whisper transcription** (no subtitles available)
```bash
# Download audio only
yt-dlp -x --audio-format mp3 --output "audio_%(id)s.%(ext)s" "$VIDEO_URL"

# Transcribe
whisper audio_XXXXX.mp3 --model base --output_format vtt

# Convert to text using deduplication script above
```

Whisper models: `tiny` (fastest), `base` (recommended), `small`, `medium`, `large` (best accuracy, ~10GB)

### 4.3 PDF Content Extraction

```bash
# Method 1: pdftotext (poppler)
pdftotext research-paper.pdf research-paper.txt

# Install on macOS
brew install poppler

# Install on Linux
apt install poppler-utils

# Method 2: Python pdfminer (handles complex layouts)
pip3 install pdfminer.six
python3 -m pdfminer.tools.pdf2txt research-paper.pdf > research-paper.txt
```

### 4.4 Content Synthesis Pipeline

After extracting content from multiple sources, apply this synthesis workflow:

**Step 1: Segment by claim type**
- Background/context
- Core argument / thesis
- Evidence / data points
- Counterarguments
- Conclusions / recommendations

**Step 2: Merge across sources**
- Group claims by topic cluster
- Note source agreement / disagreement
- Rank sources by authority

**Step 3: Write the synthesis**
- Lead with the strongest consensus claim
- Surface genuine disagreement honestly
- Quantify where possible (percentages, dates, magnitudes)
- Tag every factual claim with its source inline

**Step 4: Gap analysis**
- What questions remain unanswered?
- Which claims lack primary source support?
- What would strengthen the analysis?

### 4.5 Source Quality Tiers

| Tier | Type | Trust Level | Example |
|---|---|---|---|
| 1 | Peer-reviewed meta-analysis | Highest | Cochrane reviews, IPCC reports |
| 2 | Primary peer-reviewed study | Very high | Nature, NEJM, NBER working papers |
| 3 | Government / institutional data | High | BLS, Census, WHO statistics |
| 4 | Primary news reporting | Medium-high | NYT, FT, Reuters original reporting |
| 5 | Industry reports | Medium | Gartner, McKinsey, analyst reports |
| 6 | Expert blog / newsletter | Medium-low | Substack experts, trade publications |
| 7 | General blog / forum | Low | Reddit, Medium, general blogs |
| 8 | Social media post | Very low | Twitter/X, Facebook, TikTok |

**Rule**: Never cite Tier 6–8 sources as the sole basis for a factual claim. Always cross-reference to Tier 1–5.

---

## 5. Data Exploration & Profiling

### 5.1 Structural Understanding Phase

Before analyzing any dataset, map its structure:

**Table-level questions:**
- Row count and column count
- Grain: one row per what? (user, event, transaction, session)
- Primary key: is it unique? (test with `COUNT(*) vs COUNT(DISTINCT pk)`)
- Time range: earliest and latest records
- Update frequency: real-time, daily, weekly

**Column classification:**
| Type | Description | Examples |
|---|---|---|
| **Identifier** | Unique keys, foreign keys | user_id, order_id |
| **Dimension** | Categorical for grouping | status, region, plan_type |
| **Metric** | Quantitative for measurement | revenue, duration, count |
| **Temporal** | Dates and timestamps | created_at, event_date |
| **Text** | Free-form fields | description, comment, notes |
| **Boolean** | True/false flags | is_active, has_purchased |
| **Structural** | JSON, arrays, nested | metadata, tags, attributes |

### 5.2 Column-Level Profiling

**All columns:**
```python
import pandas as pd

def profile_column(series):
    profile = {
        'dtype': series.dtype,
        'null_count': series.isnull().sum(),
        'null_rate': series.isnull().mean(),
        'distinct_count': series.nunique(),
        'cardinality_ratio': series.nunique() / len(series),
        'top_5_values': series.value_counts().head(5).to_dict(),
    }
    return profile
```

**Numeric columns:**
```python
def profile_numeric(series):
    return series.describe(percentiles=[.01, .05, .25, .5, .75, .95, .99]).to_dict()
    # Returns: count, mean, std, min, p1, p5, p25, p50, p75, p95, p99, max
```

**String columns:**
```python
def profile_string(series):
    lengths = series.dropna().str.len()
    return {
        'min_length': lengths.min(),
        'max_length': lengths.max(),
        'avg_length': lengths.mean(),
        'empty_count': (series == '').sum(),
        'whitespace_issues': series.str.strip().ne(series).sum(),
    }
```

**Date columns:**
```python
def profile_dates(series):
    s = pd.to_datetime(series, errors='coerce')
    return {
        'min_date': s.min(),
        'max_date': s.max(),
        'null_dates': s.isnull().sum(),
        'future_dates': (s > pd.Timestamp.now()).sum(),
        'monthly_distribution': s.dt.to_period('M').value_counts().sort_index().to_dict(),
    }
```

### 5.3 Data Quality Assessment Framework

**Completeness scoring:**
| Rate | Status | Action |
|---|---|---|
| >99% non-null | Green / Complete | No action needed |
| 95–99% non-null | Yellow / Mostly complete | Investigate the nulls |
| 80–95% non-null | Orange / Incomplete | Understand why; assess impact |
| <80% non-null | Red / Sparse | May need imputation or exclusion |

**Consistency checks:**
- Value format inconsistency: "USA" vs "US" vs "United States"
- Type inconsistency: numbers stored as strings
- Referential integrity: foreign keys with no matching parent
- Business rule violations: end_date < start_date, percentage > 100
- Cross-column logic: status = "completed" but completed_at is null

**Accuracy red flags:**
- Placeholder values: 0, -1, 999999, "N/A", "TBD", "test", "xxx"
- Suspiciously high frequency of a single value (may be a default)
- Impossible values: ages > 150, timestamps in 1970
- Round number bias: all values ending in 0 or 5 (suggests estimation)

### 5.4 Pattern Discovery

**Distribution types:**
| Shape | Description | Common in |
|---|---|---|
| Normal | Bell-shaped, mean ≈ median | Heights, measurement errors |
| Right-skewed | Long high-value tail | Revenue, session duration |
| Left-skewed | Long low-value tail | Rare |
| Bimodal | Two peaks | Mixed populations |
| Power law | Few large, many small | User activity, word frequency |
| Uniform | Equal frequency | Random data, IDs |

**Temporal patterns to check:**
- Trend: sustained directional movement
- Seasonality: weekly, monthly, annual cycles
- Day-of-week effect: weekday vs. weekend differences
- Holiday spikes/drops
- Change points: abrupt level shifts

**Segmentation discovery:**
- Find categorical columns with 3–20 distinct values
- Compare metric distributions across each segment
- Look for segments with significantly different behavior
- Test whether segments are internally homogeneous

### 5.5 Schema Documentation Template

```markdown
## Table: [schema.table_name]

**Description**: [What this table represents]
**Grain**: [One row per...]
**Primary Key**: [column(s)]
**Row Count**: [approximate, as of date]
**Update Frequency**: [real-time / hourly / daily / weekly]
**Owner**: [team or person responsible]

### Key Columns

| Column | Type | Description | Example Values | Notes |
|--------|------|-------------|----------------|-------|
| user_id | STRING | Unique user identifier | "usr_abc123" | FK to users.id |
| event_type | STRING | Type of event | "click", "view" | 15 distinct values |
| revenue | DECIMAL | Transaction revenue USD | 29.99, 149.00 | Null for non-purchase |
| created_at | TIMESTAMP | When event occurred | 2024-01-15 14:23:01 | Partitioned column |

### Relationships
- Joins to `users` on `user_id`
- Joins to `products` on `product_id`

### Known Issues
- [List data quality issues]

### Common Query Patterns
- [Typical use cases]
```

### 5.6 SQL-Based Exploration

```sql
-- Row and column count
SELECT COUNT(*) as row_count FROM my_table;

-- Null rates for all columns (PostgreSQL)
SELECT
  column_name,
  COUNT(*) FILTER (WHERE column_name IS NULL) as null_count,
  ROUND(COUNT(*) FILTER (WHERE column_name IS NULL)::numeric / COUNT(*), 4) as null_rate
FROM my_table;

-- Cardinality check
SELECT
  COUNT(*) as total_rows,
  COUNT(DISTINCT primary_key) as distinct_keys
FROM my_table;

-- Distribution of a categorical column
SELECT category, COUNT(*) as n, ROUND(COUNT(*)::numeric / SUM(COUNT(*)) OVER (), 4) as pct
FROM my_table
GROUP BY category
ORDER BY n DESC;

-- Numeric percentiles (PostgreSQL)
SELECT
  PERCENTILE_CONT(0.01) WITHIN GROUP (ORDER BY value) as p1,
  PERCENTILE_CONT(0.25) WITHIN GROUP (ORDER BY value) as p25,
  PERCENTILE_CONT(0.50) WITHIN GROUP (ORDER BY value) as p50,
  PERCENTILE_CONT(0.75) WITHIN GROUP (ORDER BY value) as p75,
  PERCENTILE_CONT(0.99) WITHIN GROUP (ORDER BY value) as p99
FROM my_table;
```

---

## 6. Statistical Analysis & Methods

### 6.1 Choosing the Right Measure of Center

| Situation | Use | Why |
|---|---|---|
| Symmetric distribution, no outliers | Mean | Most efficient estimator |
| Skewed distribution | Median | Robust to outliers |
| Categorical or ordinal data | Mode | Only option for non-numeric |
| Skewed with outliers (revenue, time) | Median + mean both | Gap shows skew magnitude |

**Always report mean AND median together for business metrics.** If they diverge significantly, the data is skewed and the mean alone misleads.

### 6.2 Percentile Storytelling Framework

```
p1:  Bottom 1% — floor / minimum typical
p5:  Low end of normal range
p25: First quartile
p50: Median — the typical user/entity
p75: Third quartile
p90: Top 10% — power users / high performers
p95: High end of normal range
p99: Top 1% — extreme cases
```

**Example narrative**: "The median session duration is 4.2 minutes, but the top 10% of users spend over 22 minutes, pulling the mean up to 7.8 minutes."

### 6.3 Trend Analysis

**Moving averages (Python):**
```python
# 7-day moving average — smooth daily data with weekly seasonality
df['ma_7d'] = df['metric'].rolling(window=7, min_periods=1).mean()

# 28-day moving average — smooth weekly + monthly patterns
df['ma_28d'] = df['metric'].rolling(window=28, min_periods=1).mean()
```

**Growth rates:**
```python
# Simple period-over-period growth
growth = (current - previous) / previous

# CAGR (compound annual growth rate)
cagr = (ending / beginning) ** (1 / years) - 1

# Log growth — better for volatile series
import numpy as np
log_growth = np.log(current / previous)
```

**Period comparison best practices:**
- Week-over-week (WoW): compare same day last week
- Month-over-month (MoM): compare same month prior year
- Year-over-year (YoY): gold standard for seasonal businesses
- Always use same-length time windows (partial periods mislead)

### 6.4 Outlier Detection

**Z-score method** (normal distributions):
```python
z_scores = (df['value'] - df['value'].mean()) / df['value'].std()
outliers = df[abs(z_scores) > 3]  # Beyond 3 standard deviations
```

**IQR method** (robust; works on skewed data):
```python
Q1 = df['value'].quantile(0.25)
Q3 = df['value'].quantile(0.75)
IQR = Q3 - Q1
lower = Q1 - 1.5 * IQR
upper = Q3 + 1.5 * IQR
outliers = df[(df['value'] < lower) | (df['value'] > upper)]
```

**Time series anomaly detection:**
1. Compute expected value (moving average or same-period-last-year)
2. Compute residual (actual − expected)
3. Flag residuals beyond 2–3 standard deviations
4. Distinguish: point anomaly (single spike) vs. change point (sustained shift)

**Handling outliers — do NOT auto-remove. Instead:**
1. Investigate: data error, genuine extreme, or different population?
2. Data errors → fix or exclude with documentation
3. Genuine extremes → keep; use robust statistics (median, IQR)
4. Different population → segment separately for analysis
5. Always document: "We excluded N records (X%) with [reason]"

### 6.5 Hypothesis Testing

**The framework:**
1. **H₀ (null hypothesis)**: No difference exists (default assumption)
2. **H₁ (alternative)**: A difference exists
3. **Alpha**: Significance threshold, typically 0.05
4. **Compute test statistic + p-value**
5. **Interpret**: p < alpha → reject H₀ → evidence of real difference

**Common tests:**

| Scenario | Test | Python Method |
|---|---|---|
| Compare two group means | Independent t-test | `scipy.stats.ttest_ind` |
| Compare conversion rates | Z-test for proportions | `statsmodels.stats.proportion.proportions_ztest` |
| Before/after on same entities | Paired t-test | `scipy.stats.ttest_rel` |
| Compare 3+ group means | ANOVA | `scipy.stats.f_oneway` |
| Non-normal data, two groups | Mann-Whitney U | `scipy.stats.mannwhitneyu` |
| Two categorical variables | Chi-squared test | `scipy.stats.chi2_contingency` |

**Statistical vs. practical significance:**
- Statistical significance: difference unlikely to be chance
- Practical significance: difference large enough to matter
- Always report BOTH the p-value AND the effect size + confidence interval
- With large samples, tiny meaningless differences become statistically significant

### 6.6 Correlation Analysis

```python
# Pearson correlation matrix
corr_matrix = df[numeric_cols].corr()

# Flag strong correlations
strong = corr_matrix.abs() > 0.7
print(strong[strong].stack().index.tolist())

# Visualize
import seaborn as sns
import matplotlib.pyplot as plt
fig, ax = plt.subplots(figsize=(10, 8))
sns.heatmap(corr_matrix, annot=True, cmap='RdBu_r', center=0, ax=ax)
plt.tight_layout()
```

**Correlation ≠ causation.** When you find a correlation, explicitly consider:
- Reverse causation (B causes A, not A → B)
- Confounding variable (C causes both A and B)
- Coincidence (spurious with enough variables)

### 6.7 Statistical Pitfalls Checklist

| Pitfall | Warning Sign | Prevention |
|---|---|---|
| Correlation ≠ causation | Found a r > 0.7 | State explicitly; consider confounders |
| Multiple comparisons | Tested 20+ metrics | Apply Bonferroni correction (α / n tests) |
| Simpson's paradox | Aggregate trend reverses in segments | Always check segment-level results |
| Survivorship bias | Dataset only has "survivors" | Ask: who is missing? |
| Ecological fallacy | Group-level patterns applied to individuals | Avoid individual-level conclusions from aggregates |
| Anchoring on false precision | "Churn will be 4.73%" | Use ranges: "4–6% churn expected" |
| Small sample unreliability | N < 30 per group | Report N; caveat conclusions |

---

## 7. Data Visualization & Communication

### 7.1 Chart Selection Guide

| What You're Showing | Best Chart | Avoid |
|---|---|---|
| Trend over time | Line chart | Bar chart for long time series |
| Comparison across categories | Horizontal bar (many) / Vertical bar (few) | Pie chart |
| Ranking | Horizontal bar (sorted by value) | Alphabetical sort |
| Part-to-whole | Stacked bar; treemap (hierarchy) | Pie/donut (>6 slices) |
| Composition over time | Stacked area; 100% stacked bar | Multiple pie charts |
| Distribution | Histogram; box plot (compare groups) | Mean-only bar chart |
| Correlation (2 variables) | Scatter plot | Line chart |
| Correlation (many variables) | Heatmap correlation matrix | Pair plot (>8 vars) |
| Geographic patterns | Choropleth; bubble map | Table |
| Process/flow | Sankey diagram; funnel chart | Text only |
| Performance vs. target | Bullet chart | Gauge (single KPI) |
| Multiple KPIs | Small multiples | Dual-axis chart |

**Never use**: 3D charts, pie charts with >6 slices, dual-axis without explicit justification, bar charts not starting at zero.

### 7.2 Python Setup (Professional Style)

```python
import matplotlib.pyplot as plt
import matplotlib.ticker as mticker
import seaborn as sns
import pandas as pd
import numpy as np

# Professional style
plt.style.use('seaborn-v0_8-whitegrid')
plt.rcParams.update({
    'figure.figsize': (10, 6),
    'figure.dpi': 150,
    'font.size': 11,
    'axes.titlesize': 14,
    'axes.titleweight': 'bold',
    'axes.labelsize': 11,
    'xtick.labelsize': 10,
    'ytick.labelsize': 10,
    'legend.fontsize': 10,
})

# Colorblind-friendly palettes
PALETTE_CATEGORICAL = ['#4C72B0', '#DD8452', '#55A868', '#C44E52', '#8172B3', '#937860']
PALETTE_SEQUENTIAL = 'YlOrRd'
PALETTE_DIVERGING = 'RdBu_r'
```

### 7.3 Core Chart Templates

**Line chart (time series):**
```python
fig, ax = plt.subplots(figsize=(10, 6))
for label, group in df.groupby('category'):
    ax.plot(group['date'], group['value'], label=label, linewidth=2)
ax.set_title('Metric Trend by Category', fontweight='bold')
ax.set_xlabel('Date')
ax.set_ylabel('Value')
ax.legend(loc='upper left', frameon=True)
ax.spines['top'].set_visible(False)
ax.spines['right'].set_visible(False)
fig.autofmt_xdate()
plt.tight_layout()
plt.savefig('trend_chart.png', dpi=150, bbox_inches='tight')
```

**Horizontal bar chart (ranking):**
```python
fig, ax = plt.subplots(figsize=(10, 6))
df_sorted = df.sort_values('metric', ascending=True)
bars = ax.barh(df_sorted['category'], df_sorted['metric'], color=PALETTE_CATEGORICAL[0])
for bar in bars:
    width = bar.get_width()
    ax.text(width + 0.5, bar.get_y() + bar.get_height()/2,
            f'{width:,.0f}', ha='left', va='center', fontsize=10)
ax.set_title('Metric by Category (Ranked)', fontweight='bold')
ax.spines['top'].set_visible(False)
ax.spines['right'].set_visible(False)
plt.tight_layout()
plt.savefig('bar_chart.png', dpi=150, bbox_inches='tight')
```

**Histogram (distribution):**
```python
fig, ax = plt.subplots(figsize=(10, 6))
ax.hist(df['value'], bins=30, color=PALETTE_CATEGORICAL[0], edgecolor='white', alpha=0.8)
ax.axvline(df['value'].mean(), color='red', linestyle='--', linewidth=1.5,
           label=f'Mean: {df["value"].mean():,.1f}')
ax.axvline(df['value'].median(), color='green', linestyle='--', linewidth=1.5,
           label=f'Median: {df["value"].median():,.1f}')
ax.set_title('Distribution of Values', fontweight='bold')
ax.legend()
ax.spines['top'].set_visible(False)
ax.spines['right'].set_visible(False)
plt.tight_layout()
plt.savefig('histogram.png', dpi=150, bbox_inches='tight')
```

**Heatmap (correlation or cross-tab):**
```python
fig, ax = plt.subplots(figsize=(10, 8))
pivot = df.pivot_table(index='row_dim', columns='col_dim', values='metric', aggfunc='sum')
sns.heatmap(pivot, annot=True, fmt=',.0f', cmap='YlOrRd',
            linewidths=0.5, ax=ax, cbar_kws={'label': 'Value'})
ax.set_title('Cross-Tab Heatmap', fontweight='bold')
plt.tight_layout()
plt.savefig('heatmap.png', dpi=150, bbox_inches='tight')
```

**Small multiples:**
```python
categories = df['category'].unique()
n_cols = min(3, len(categories))
n_rows = (len(categories) + n_cols - 1) // n_cols
fig, axes = plt.subplots(n_rows, n_cols, figsize=(5*n_cols, 4*n_rows),
                          sharex=True, sharey=True)
axes = axes.flatten()
for i, cat in enumerate(categories):
    ax = axes[i]
    subset = df[df['category'] == cat]
    ax.plot(subset['date'], subset['value'],
            color=PALETTE_CATEGORICAL[i % len(PALETTE_CATEGORICAL)])
    ax.set_title(cat, fontsize=12)
    ax.spines['top'].set_visible(False)
    ax.spines['right'].set_visible(False)
for j in range(i+1, len(axes)):
    axes[j].set_visible(False)
fig.suptitle('Trends by Category', fontsize=14, fontweight='bold')
plt.tight_layout()
plt.savefig('small_multiples.png', dpi=150, bbox_inches='tight')
```

**Interactive Plotly charts:**
```python
import plotly.express as px

# Interactive line chart
fig = px.line(df, x='date', y='value', color='category',
              title='Interactive Metric Trend')
fig.update_layout(hovermode='x unified')
fig.write_html('interactive_chart.html')

# Interactive scatter
fig = px.scatter(df, x='metric_a', y='metric_b', color='category',
                 size='size_metric', hover_data=['name'],
                 title='Correlation Analysis')
fig.show()
```

### 7.4 Number Formatting

```python
def format_number(val, format_type='number'):
    if format_type == 'currency':
        if abs(val) >= 1e9: return f'${val/1e9:.1f}B'
        elif abs(val) >= 1e6: return f'${val/1e6:.1f}M'
        elif abs(val) >= 1e3: return f'${val/1e3:.1f}K'
        else: return f'${val:,.0f}'
    elif format_type == 'percent':
        return f'{val:.1f}%'
    elif format_type == 'number':
        if abs(val) >= 1e9: return f'{val/1e9:.1f}B'
        elif abs(val) >= 1e6: return f'{val/1e6:.1f}M'
        elif abs(val) >= 1e3: return f'{val/1e3:.1f}K'
        else: return f'{val:,.0f}'
    return str(val)

# Apply to axis
ax.yaxis.set_major_formatter(mticker.FuncFormatter(
    lambda x, p: format_number(x, 'currency')))
```

### 7.5 Design Principles

**Color:**
- Use color to encode data, not decorate
- Highlight the insight with a bright accent; grey everything else
- Sequential: single-hue gradient (light→dark) for ordered values
- Diverging: two-hue gradient with neutral midpoint for data centered on zero
- Categorical: max 6–8 distinct hues before confusion sets in
- Never rely only on red/green; 8% of men are red-green colorblind

**Typography:**
- Title states the insight: "Revenue grew 23% YoY" > "Revenue by Month"
- Subtitle adds context: date range, filters, data source
- Axis labels: readable, with units, never rotated 90° if avoidable

**Layout:**
- Remove chart junk: unnecessary gridlines, borders, background colors
- Sort categories by value (not alphabetically) unless natural order exists
- Bar charts must start at zero — always
- Line charts can have non-zero baselines when the range of variation matters

### 7.6 Accessibility Checklist

Before sharing any visualization:
- [ ] Chart works without color (patterns, labels, or line styles differentiate series)
- [ ] Text is readable at standard zoom (min 10pt labels, 12pt titles)
- [ ] Title describes the insight, not just the data
- [ ] Axes are labeled with units
- [ ] Legend is clear; does not obscure data
- [ ] Data source and date range are noted
- [ ] Chart works in black and white

---

## 8. Data Validation & Quality Assurance

### 8.1 Pre-Delivery QA Checklist

Run every check before sharing analysis with stakeholders.

**Data quality:**
- [ ] Source verification: correct tables/files for this question
- [ ] Freshness: data is current; "as of" date is noted
- [ ] Completeness: no unexpected gaps in time series or segments
- [ ] Null handling: null rates checked; nulls handled appropriately
- [ ] Deduplication: no double-counting from joins or duplicates
- [ ] Filter verification: all WHERE clauses correct; no unintended exclusions

**Calculation checks:**
- [ ] Aggregation logic: GROUP BY includes all non-aggregated columns
- [ ] Denominator correctness: rates/percentages use the right denominator; non-zero
- [ ] Date alignment: comparisons use same time-period length; partial periods excluded
- [ ] Join correctness: INNER vs LEFT chosen appropriately; no M:M join explosion
- [ ] Metric definitions: match how stakeholders define the metric
- [ ] Subtotals sum: parts add up to whole (explain if they don't)

**Reasonableness checks:**
- [ ] Magnitude: revenue not negative; percentages between 0–100%
- [ ] Trend continuity: no unexplained jumps or drops
- [ ] Cross-reference: key numbers match dashboards and prior reports
- [ ] Order of magnitude: totals are in the right ballpark
- [ ] Edge cases: checked boundaries (empty segments, zero-activity periods)

**Presentation checks:**
- [ ] Bar charts start at zero
- [ ] Axes labeled with units
- [ ] Number formatting consistent (currency, percentage, thousands separators)
- [ ] Titles state the insight; date ranges specified
- [ ] Caveats and assumptions explicitly stated
- [ ] Reproducibility: documented enough to recreate from scratch

### 8.2 Common Analysis Pitfalls

**Join explosion:**
```sql
-- Check BEFORE and AFTER the join
SELECT COUNT(*) FROM table_a;                         -- 1,000
SELECT COUNT(*) FROM table_a a JOIN table_b b ON ...; -- 3,500 (problem!)
-- Fix: use COUNT(DISTINCT a.id) when counting through joins
```

**Survivorship bias:**
- Analyzing "current users" misses churned users
- Ask: "Who is NOT in this dataset, and would they change my conclusion?"

**Incomplete period comparison:**
- "January is down vs December" — but January isn't over yet
- Fix: always filter to complete periods, or compare equal-length windows

**Denominator shifting:**
- Conversion rate "improved" because you changed how eligible users are counted
- Fix: use consistent metric definitions; document any definition changes

**Average of averages:**
```python
# WRONG: (50 + 200) / 2 = 125 when groups are unequal size
# RIGHT: (100*50 + 10*200) / 110 = 63.64
# Always aggregate from raw data, not pre-aggregated summaries
```

**Timezone mismatches:**
- Different sources may use different timezones
- Fix: standardize all timestamps to UTC before any joins or aggregations

**Selection bias in segmentation:**
- "Users who completed onboarding have higher retention" — circular; they self-selected
- Fix: define segments on pre-treatment characteristics, not outcomes

### 8.3 Result Sanity Checks

| Metric Type | Sanity Check |
|---|---|
| User counts | Matches known MAU/DAU figures? |
| Revenue | Correct order of magnitude vs. known ARR? |
| Conversion rates | Between 0–100%? Matches dashboard? |
| Growth rates | Is >50% MoM realistic, or is there a data error? |
| Averages | Reasonable given distribution shape? |
| Percentages | Segment percentages sum to ~100%? |

**Cross-validation techniques:**
1. Calculate the same metric two different ways and verify agreement
2. Spot-check individual records manually
3. Compare to known benchmarks (dashboards, finance reports)
4. Reverse engineer: if total revenue is X, does per-user × user count ≈ X?
5. Boundary checks: filter to one day, one user — does it make sense?

### 8.4 Analysis Documentation Template

```markdown
## Analysis: [Title]

### Question
[The specific question being answered]

### Data Sources
- Table: [schema.table_name] (as of [date])
- File: [filename] (source: [origin])

### Definitions
- [Metric A]: [Exactly how it's calculated]
- [Segment X]: [Exactly how membership is determined]
- [Time period]: [Start date] to [end date], [timezone]

### Methodology
1. [Step 1]
2. [Step 2]
3. [Step 3]

### Assumptions and Limitations
- [Assumption 1 and justification]
- [Limitation 1 and potential impact]

### Key Findings
1. [Finding 1 with supporting evidence]
2. [Finding 2 with supporting evidence]

### Caveats
- [Things the reader should know before acting on this]

### Reproducibility
[SQL / Python code or reference to workspace file]
```

---

## 9. Creative Ideation & Brainstorming

### 9.1 The Hard Gate: Design Before Implementation

**HARD GATE**: Do NOT write code, scaffold projects, or take implementation action until:
1. A design has been presented
2. The user has explicitly approved it

This applies to EVERY project regardless of perceived simplicity. "Simple" projects are where unexamined assumptions cause the most wasted work.

### 9.2 Brainstorming Process Flow

```
1. Explore project context
        ↓
2. Ask clarifying questions (one at a time)
        ↓
3. Propose 2–3 approaches with trade-offs
        ↓
4. Present design sections (get approval after each)
        ↓
5. Write design doc → docs/plans/YYYY-MM-DD-<topic>-design.md
        ↓
6. Transition to implementation plan
```

### 9.3 Clarifying Question Framework

Ask questions **one at a time**. Prefer multiple-choice when possible. Focus on:

**Purpose questions:**
- What problem does this solve?
- Who is the primary user/beneficiary?
- What does success look like in concrete terms?

**Constraint questions:**
- Are there time, budget, or technical constraints?
- What must NOT change (existing integrations, data formats)?
- What has been tried before that didn't work?

**Success criteria questions:**
- How will we measure whether this worked?
- What's the minimum acceptable outcome?
- What's the ideal outcome?

### 9.4 Proposing Approaches

Always offer 2–3 distinct approaches:

```markdown
## Approach A: [Label] — RECOMMENDED
**Description**: [1–2 sentences]
**Pros**: [2–3 bullet points]
**Cons**: [1–2 bullet points]
**Best when**: [conditions that favor this approach]

## Approach B: [Label]
**Description**: [1–2 sentences]
**Pros**: [2–3 bullet points]
**Cons**: [1–2 bullet points]

## Approach C: [Label — simpler/fallback]
**Description**: [1–2 sentences]
**Pros**: [faster/simpler]
**Cons**: [limitations]
```

### 9.5 Creative Research Brainstorming Techniques

**Lateral thinking prompts** for research topic expansion:
- "What if the opposite were true?"
- "What would an expert from a completely different field say?"
- "What data would disprove this hypothesis?"
- "Who benefits most from the current state of knowledge?"
- "What is the smallest possible test of this idea?"

**Analogical reasoning:**
- Find a parallel problem in a different domain
- Ask: how did that domain solve it?
- Map the solution back to your context

**Assumption challenging:**
1. List the 5 biggest assumptions in your current research framing
2. For each assumption, ask: "What if this is wrong?"
3. If that assumption were false, what would you research instead?

**Pre-mortem analysis:**
- Imagine it is 12 months from now and the research project failed
- What went wrong? (generates risk list)
- Now: design the research to prevent each failure mode

### 9.6 Design Document Format

```markdown
# Design: [Topic]
Date: YYYY-MM-DD

## Problem Statement
[What problem are we solving and why it matters]

## Goals
- Primary: [Must achieve]
- Secondary: [Nice to have]
- Out of scope: [Explicitly excluded]

## Proposed Architecture / Approach
[Description, diagram, or pseudocode — scale to complexity]

## Components
1. [Component A]: [description]
2. [Component B]: [description]

## Data Flow
[How data moves through the system]

## Error Handling
[How edge cases and failures are handled]

## Testing Strategy
[How we'll verify this works]

## Open Questions
- [ ] [Question 1]
- [ ] [Question 2]
```

### 9.7 YAGNI and Scope Management

Apply YAGNI (You Ain't Gonna Need It) ruthlessly to all designs:
- Remove any feature not required by the current stated need
- Challenge every "we might need this later" addition
- Prefer the simplest solution that solves the stated problem
- Document deferred features explicitly (not silently included)

---

## 10. RAG Systems & AI-Powered Research

### 10.1 RAG System Architecture

Retrieval-Augmented Generation (RAG) improves LLM answers by retrieving relevant context from your document corpus before generating a response.

```
User Query
    ↓
[Query Embedding]
    ↓
[Vector Store Search] ← (pre-built from your document corpus)
    ↓
[Retrieved Contexts (top-k)]
    ↓
[LLM Prompt = System + Retrieved Context + User Query]
    ↓
[Generated Answer]
    ↓
[Faithfulness Check: answer grounded in retrieved context?]
```

### 10.2 RAG Building Blocks

**Step 1: Document ingestion**
```python
# Chunk documents for embedding
def chunk_document(text, chunk_size=512, overlap=64):
    tokens = text.split()
    chunks = []
    for i in range(0, len(tokens), chunk_size - overlap):
        chunk = ' '.join(tokens[i:i+chunk_size])
        chunks.append(chunk)
    return chunks
```

**Step 2: Embedding and indexing**
```python
# Using sentence-transformers (local, free)
from sentence_transformers import SentenceTransformer
import numpy as np

model = SentenceTransformer('all-MiniLM-L6-v2')
embeddings = model.encode(chunks)

# Store with metadata
import faiss
index = faiss.IndexFlatIP(embeddings.shape[1])
index.add(embeddings.astype(np.float32))
```

**Step 3: Retrieval**
```python
def retrieve(query, index, chunks, model, top_k=5):
    query_embedding = model.encode([query]).astype(np.float32)
    scores, indices = index.search(query_embedding, top_k)
    return [(chunks[i], scores[0][j]) for j, i in enumerate(indices[0])]
```

**Step 4: Generation with context**
```python
def generate_answer(query, contexts):
    context_text = '\n\n'.join([ctx for ctx, score in contexts])
    prompt = f"""Answer the question based only on the context below.

Context:
{context_text}

Question: {query}

Answer:"""
    # Pass to your LLM of choice
    return llm_call(prompt)
```

### 10.3 RAG Evaluation Framework

**Evaluate with three metrics:**

| Metric | Definition | Target |
|---|---|---|
| Context Relevance | Retrieved chunks relevant to the query | > 0.80 |
| Answer Faithfulness | Answer claims supported by retrieved context | > 0.90 |
| Retrieval Coverage | Query answerable from top-5 retrieved chunks | > 0.85 |
| Answer Correctness | Answer matches ground truth (if available) | > 0.75 |

**Evaluation script pattern:**
```bash
python scripts/rag_evaluator.py \
  --contexts retrieved.json \
  --questions eval_set.json \
  --metrics relevance,faithfulness,coverage \
  --output report.json --verbose
```

**Common RAG failure modes:**

| Problem | Symptom | Fix |
|---|---|---|
| Poor chunking | Relevant info split across chunks | Semantic chunking; increase overlap |
| Irrelevant retrieval | Context chunks don't match query | Better embeddings; metadata filtering |
| Hallucination | Answer contradicts context | Add faithfulness check; temperature=0 |
| Missing context | Answer says "I don't know" too often | Expand corpus; increase top-k |
| Date-sensitivity failures | Outdated retrieved info | Add metadata date filters |

### 10.4 Prompt Engineering Patterns

**Core patterns:**

| Pattern | When to Use | Example |
|---|---|---|
| **Zero-shot** | Simple, well-defined tasks | "Classify this email as spam or not spam" |
| **Few-shot** | Complex tasks needing consistent format | 3–5 examples before the task |
| **Chain-of-Thought** | Reasoning, math, multi-step logic | "Think step by step..." |
| **Role Prompting** | Expertise or specific perspective needed | "You are an expert tax accountant..." |
| **Structured Output** | Need parseable JSON/XML | Include schema + format enforcement |
| **Self-Consistency** | High-stakes reasoning | Run multiple times; take majority vote |
| **ReAct** | Tool-using agents | Think → Act → Observe loop |

**Prompt optimization workflow:**

```bash
# Step 1: Baseline analysis
python scripts/prompt_optimizer.py current_prompt.txt --analyze --output baseline.json

# Step 2: Apply patterns based on issues found
# Ambiguous output → add explicit format specification
# Too verbose → extract to few-shot examples
# Inconsistent results → add role/persona framing
# Missing edge cases → add constraint boundaries

# Step 3: Generate optimized version
python scripts/prompt_optimizer.py current_prompt.txt --optimize --output optimized.txt

# Step 4: Compare
python scripts/prompt_optimizer.py optimized.txt --analyze --compare baseline.json
```

### 10.5 Few-Shot Example Design

**Selection criteria for examples (3–5 recommended):**

| Example Type | Purpose |
|---|---|
| Simple case | Shows basic pattern |
| Edge case | Handles ambiguity |
| Complex case | Multiple entities or steps |
| Negative case | What NOT to do/extract |

**Format template:**
```
Example 1:
Input: "Love my new iPhone 15, the camera is amazing!"
Output: {"product_name": "iPhone 15", "sentiment": "positive", "features": ["camera"]}

Example 2:
Input: "The laptop was okay but battery life is terrible."
Output: {"product_name": "laptop", "sentiment": "mixed", "features": ["battery life"]}
```

### 10.6 Structured Output Design

**Step 1: Define schema:**
```json
{
  "type": "object",
  "properties": {
    "summary": {"type": "string", "maxLength": 200},
    "sentiment": {"enum": ["positive", "negative", "neutral"]},
    "confidence": {"type": "number", "minimum": 0, "maximum": 1}
  },
  "required": ["summary", "sentiment"]
}
```

**Step 2: Include schema in prompt:**
```
Respond with JSON matching this schema:
- summary (string, max 200 chars): Brief summary
- sentiment (enum): "positive", "negative", or "neutral"
- confidence (number 0–1): Your confidence level
```

**Step 3: Format enforcement:**
```
IMPORTANT: Respond ONLY with valid JSON. No markdown, no explanation.
Start your response with { and end with }
```

### 10.7 Agent Architecture Patterns

**ReAct (Reasoning + Acting) — most common:**
```
User Query → Think → Select Tool → Observe → Think → ... → Final Answer
```

**Plan-Execute:**
```
User Query → Generate Plan (steps) → Execute Each Step → Synthesize
```

**Multi-Agent:**
```
Orchestrator → Spawn Subagents → Each researches in parallel → Orchestrator synthesizes
```

**Tool Use validation:**
```bash
python scripts/agent_orchestrator.py agent.yaml --validate
# Checks: tool availability, API keys, allowed paths, max iteration depth
```

---

## 11. Iterative Learning & Feedback

### 11.1 The Ship-Learn-Next Framework

Transform passive learning into active building using the Ship-Learn-Next cycle:

```
SHIP  → Create something real (code, content, product, analysis)
LEARN → Honest reflection on what happened
NEXT  → Plan the next iteration based on learnings
```

**Core principle**: 100 reps beats 100 hours of study. Learning = doing better, not knowing more.

**Trigger phrases**: "turn [content] into a plan", "make this actionable", "I watched/read X — now what?"

### 11.2 Quest Definition

A good quest is specific, time-boxed, and produces a real artifact.

**Bad quest**: "Learn machine learning" (too vague, no end state)
**Good quest**: "Build and deploy a regression model on the Titanic dataset by [date]"

**Quest definition questions:**
1. What do you want to achieve in 4–8 weeks?
2. What would success look like in concrete terms?
3. What is something real you could build/create/ship?
4. What's the minimum acceptable version?

### 11.3 Rep Structure

Each rep (iteration) follows this structure:

```markdown
## Rep N: [Specific, Shippable Goal]

**Ship Goal**: [Concrete deliverable]
**Timeline**: [Specific deadline — this week / by date]
**Success Criteria**:
- [ ] [Specific measurable outcome 1]
- [ ] [Specific measurable outcome 2]

**What You'll Practice** (from source content):
- [Skill/concept 1]
- [Skill/concept 2]

**Action Steps**:
1. [Concrete step]
2. [Concrete step]
3. [Concrete step]
4. Ship it (publish/deploy/share/demonstrate)

**Minimal Resources** (only what's needed for this rep):
- [Link or reference if truly needed]

**After Shipping — Reflection**:
- What actually happened?
- What worked? What didn't?
- What surprised you?
- Rate this rep: __/10
- One thing to try differently next time?
```

### 11.4 Progression Design (Reps 2–5)

Each subsequent rep adds ONE new element and builds on the previous rep's learnings:

```markdown
## Rep 2: [Next level]
**Builds on**: What you learned in Rep 1
**New challenge**: One new thing to try or improve
**Expected difficulty**: Harder (because you've mastered Rep 1)

## Rep 3: [Continue progression]
**Builds on**: Reps 1–2
**New challenge**: [...]

## Reps 4–5: Future Path
(Details evolve based on what you actually learn in Reps 1–3)
```

**Progression principles:**
- Each rep adds exactly one new element (not multiple)
- Increase difficulty based on demonstrated success
- Keep reps shippable (always produce a real artifact)
- Small enough to start today; big enough to learn something real

### 11.5 Learning from Research

**After completing a research project:**

1. **Document what worked** — which search strategies were most productive?
2. **Document what didn't** — which sources were unreliable? Which search terms returned junk?
3. **Update your source quality map** — add new reliable sources to your known-good list
4. **Capture reusable templates** — save any analysis frameworks that proved useful
5. **Log open questions** — what did this research surface that warrants future investigation?

**Retrospective template:**
```markdown
## Research Retrospective: [Topic]
Date: [date]

### What worked well
- [search strategy / source / approach]

### What didn't work
- [approach and why it failed]

### Surprising findings
- [unexpected discoveries]

### Open questions for next time
- [ ] [question 1]
- [ ] [question 2]

### Reusable assets created
- [template / framework / source list]
```

### 11.6 What NOT to Do (Anti-Patterns)

- Do NOT create a study plan — create a SHIP plan
- Do NOT list all resources to consume — pick the minimum for the current rep
- Do NOT let perfect be the enemy of shipped
- Do NOT accept vague goals — push for "ship Y by Z date"
- Do NOT plan more than 2 reps ahead without shipping first
- Do NOT skip the reflection step — it's where the learning lives

---

## 12. Unique Perplexity Computer Capabilities

These capabilities are exclusive to Perplexity Computer and unavailable or limited in standard LLM environments.

### 12.1 Live Web Search

```python
# search_web: General web search with real-time results
# Best practices:
# - Use 2–5 word queries (not full sentences)
# - Split multi-faceted questions into parallel queries
# - Max 3 queries per call for efficiency
search_web(queries=["inflation rate Canada 2025", "Bank of Canada rate decision"])

# search_vertical: Specialized verticals
search_vertical(vertical="academic", query="transformer attention mechanism")
search_vertical(vertical="image", query="San Francisco skyline")
search_vertical(vertical="shopping", query="ergonomic standing desk")
search_vertical(vertical="people", query="CEO OpenAI")
search_vertical(vertical="video", query="deep learning tutorial")
```

### 12.2 Academic Search

Use `search_vertical(vertical="academic")` for:
- Peer-reviewed publications
- Research papers with DOIs
- Citation information
- Author and institution data

**Workflow for literature review:**
1. Start with 3–5 broad academic queries on your topic
2. Note highly-cited papers and their authors
3. Fetch primary source URLs to extract abstracts and methodology
4. Trace citation networks (who cites these papers? what do they cite?)
5. Map the theoretical landscape: founding papers → refinements → current state

### 12.3 Social Media Research

```python
# X/Twitter search with operators
search_social(query="from:elonmusk -is:retweet", start_time="2024-01-01T00:00:00Z")
search_social(query="#ArtificialIntelligence is:reply", only_recent=True)
search_social(query="tesla from:elonmusk -is:retweet -is:reply")

# Supported operators:
# from:username      Posts from a specific user
# to:username        Replies to a specific user
# #hashtag           Posts containing hashtag
# @username          Posts mentioning username
# is:retweet         Include/exclude retweets with -is:retweet
# is:reply           Include/exclude replies
# is:quote           Include/exclude quote tweets
```

**Use cases:**
- Monitor brand mentions in real time
- Track emerging trends before they hit mainstream media
- Analyze public sentiment on announcements
- Find domain experts by topic engagement

### 12.4 400+ External Integrations

Perplexity Computer can connect to external services via `list_external_tools`:

```python
# Discovery pattern
tools = list_external_tools(queries=["CRM", "email", "calendar", "database"])

# For any connected service:
describe_external_tools(source_id="gmail", tool_names=["search_email"])
call_external_tool(tool_name="search_email", source_id="gmail",
                   arguments={"query": "invoice", "max_results": 10})
```

**Common integration categories:**
| Category | Examples |
|---|---|
| Communication | Gmail, Slack, Outlook, Teams |
| CRM | Salesforce, HubSpot, Pipedrive |
| Productivity | Notion, Airtable, Asana, Jira |
| Data / Analytics | BigQuery, Snowflake, PostgreSQL |
| Cloud storage | Google Drive, Dropbox, OneDrive |
| E-commerce | Shopify, Stripe, WooCommerce |
| Social | LinkedIn, Twitter/X, Facebook |
| Finance | QuickBooks, Xero, Plaid |

### 12.5 Parallelized Subagent Research

Perplexity Computer can spawn multiple research subagents simultaneously, each focused on a different angle of a problem:

```
Research Request: "Analyze the EV market landscape"
    ↓
Orchestrator spawns:
├── Subagent 1: "Tesla competitive position 2025"
├── Subagent 2: "BYD market share and growth"
├── Subagent 3: "EV battery technology trends"
├── Subagent 4: "EV charging infrastructure investment"
└── Subagent 5: "Government EV policy changes 2025"
    ↓
Each saves findings to workspace/ev-market-[topic].json
    ↓
Orchestrator reads all files and synthesizes final report
```

**Rules:**
- Each subagent writes to a unique workspace file
- Subagents never overwrite each other
- Master agent synthesizes only after ALL subagents complete
- Include source URLs in every subagent finding

### 12.6 Memory Across Sessions

```python
# At the start of any research task:
memory_search("prior research on [topic]")

# If prior work found:
# - Read the workspace file from the previous session
# - Build on it rather than re-researching
# - Note what may have changed (date-sensitive facts)
```

**Memory best practices:**
- Save key findings to workspace with descriptive filenames: `research-topic-YYYYMMDD.json`
- Include "as of [date]" markers on all time-sensitive data
- Create a running `research-index.md` that maps topics to their workspace files

### 12.7 Screenshot & Visual Analysis

```python
# Capture a live webpage for visual analysis
screenshot_page(url="https://competitor.com/pricing",
                user_description="Capturing competitor pricing page")

# Use cases:
# - Competitive pricing capture
# - UI/UX benchmarking
# - Verifying live web content matches claims
# - Archiving web evidence for research reports
```

---

## 13. Research Templates & Frameworks

### 13.1 Research Brief Template

```markdown
# Research Brief: [Topic]
**Date**: [date]
**Researcher**: [name]
**Confidence Level**: High / Medium / Low

## Executive Summary
[2–3 sentences: key finding, evidence quality, recommended action]

## Background & Context
[Why this question matters; what was known before this research]

## Key Findings

### Finding 1: [Label]
**Claim**: [Precise factual statement]
**Evidence**: [Source 1](URL), [Source 2](URL)
**Confidence**: High / Medium / Low
**Caveat**: [Any limitations on this finding]

### Finding 2: [Label]
[Same structure]

## Contested Areas
[Where sources disagree — present both sides with evidence]

## Data Points
| Metric | Value | Source | Date |
|--------|-------|--------|------|
| [Label] | [Value] | [Source](URL) | [date] |

## Sources
| Source | Authority Tier | URL | Accessed |
|--------|---------------|-----|---------|
| [Name] | 1–Primary | [URL] | [date] |

## Open Questions
- [ ] [Question that warrants further research]
- [ ] [Question]

## Recommended Actions
1. [Action based on findings]
2. [Action]
```

### 13.2 Literature Review Template

```markdown
# Literature Review: [Research Topic]
**Scope**: [Date range, domains, exclusion criteria]
**Sources reviewed**: [N papers/articles]

## Theoretical Foundations
[The foundational papers/frameworks — Tier 1–2 sources only]

## Current State of Knowledge
[What is well-established (high consensus, multiple replication studies)]

## Active Debates
[Where researchers currently disagree — cite both camps with primary sources]

## Methodological Landscape
[Common research methods used in this field; strengths and weaknesses]

## Research Gaps
[What has not been studied; where primary evidence is lacking]

## Synthesis
[Your integrated interpretation of the literature]

## Citation Network
[Highly-cited papers; seminal works; recent breakout papers]

## Bibliography
[Full citations with DOIs where available]
```

### 13.3 Competitive Analysis Framework

```markdown
# Competitive Analysis: [Your Product] vs Market

## Market Map
[Visual/table of all relevant players by segment]

## Competitor Profiles

### Competitor A: [Name]
**Founded**: [year]
**Funding / Revenue**: [if public]
**Target Customer**: [segment]
**Core Value Proposition**: [one sentence]
**Pricing**: [model and range]
**Key Features**: [bullet list]
**Weaknesses**: [bullet list]
**Recent Activity**: [last 6 months]
**Sources**: [URLs]

## Feature Comparison Matrix

| Feature | Your Product | Comp A | Comp B | Comp C |
|---------|-------------|--------|--------|--------|
| [Feature 1] | ✓ | ✓ | ✗ | ✓ |
| [Feature 2] | ✗ | ✓ | ✓ | ✗ |

## Positioning Map
[2×2 or narrative description of positioning space]

## Competitive Opportunities
[Segments / features where competitors are weak]

## Competitive Threats
[Segments / trends where competitors are strengthening]
```

### 13.4 Dataset Exploration Report Template

```markdown
# Dataset Exploration Report: [Dataset Name]

## Overview
**Source**: [where data came from]
**Time Range**: [earliest to latest record]
**Row Count**: [N rows]
**Column Count**: [N columns]
**Primary Key**: [column name] — [unique / not unique]

## Column Profiles

| Column | Type | Null Rate | Distinct | Min | Max | Notes |
|--------|------|-----------|----------|-----|-----|-------|
| [name] | STRING | 0.02% | 150 | — | — | [notes] |
| [name] | NUMERIC | 0.0% | 8,432 | 0 | 9,999 | Right-skewed |

## Data Quality Issues

| Issue | Column | Severity | Recommendation |
|-------|--------|----------|----------------|
| [issue] | [col] | High/Med/Low | [fix] |

## Key Distributions
[Histograms or description for key numeric columns]

## Temporal Patterns
[Time series shape, seasonality, change points]

## Relationships Discovered
[Foreign keys, correlations, hierarchies]

## Recommended Analysis Paths
1. [Suggested analysis 1]
2. [Suggested analysis 2]
```

### 13.5 A/B Test Analysis Template

```markdown
# A/B Test Analysis: [Test Name]

## Test Setup
**Hypothesis**: [If we do X, Y metric will improve because Z]
**Control**: [Description]
**Variant**: [Description]
**Test Period**: [Start date] to [End date]
**Sample Size**: Control: N=[x], Variant: N=[y]
**Randomization**: [How users were assigned]

## Results

| Metric | Control | Variant | Absolute Diff | Relative Diff | p-value | Significant? |
|--------|---------|---------|---------------|---------------|---------|-------------|
| Primary metric | X% | Y% | +Z pp | +A% | 0.023 | Yes |
| Secondary metric | | | | | | |

## Statistical Details
**Test Used**: [t-test / z-test for proportions / etc.]
**Alpha**: 0.05
**Confidence Interval**: [primary metric CI]
**Power**: [if calculated]

## Segment Analysis
[Does the effect hold across key segments?]

## Practical Significance
[Business impact translation: X% improvement = $Y revenue / N users]

## Decision
**Recommendation**: Ship / Don't Ship / Run longer / Iterate
**Rationale**: [Evidence-based justification]

## Caveats
- [Novelty effect risk]
- [Sample ratio mismatch check]
- [Multiple comparison correction applied / not applied]
```

### 13.6 Ship-Learn-Next Plan Template

```markdown
# Ship-Learn-Next Quest: [Title]

## Quest Overview
**Goal**: [Specific achievement in 4–8 weeks]
**Source Content**: [URL or title of article/video that inspired this]
**Core Lessons** (from source):
1. [Actionable lesson 1]
2. [Actionable lesson 2]
3. [Actionable lesson 3]

---

## Rep 1: [Specific Shippable Goal]

**Ship Goal**: [Concrete deliverable]
**Timeline**: By [specific date]
**Success Criteria**:
- [ ] [Measurable outcome 1]
- [ ] [Measurable outcome 2]
- [ ] [Measurable outcome 3]

**What You'll Practice**:
- [Skill from source content]
- [Skill from source content]

**Action Steps**:
1. [Step]
2. [Step]
3. [Step]
4. Ship it (publish / deploy / share / demonstrate)

**Resources** (minimal — only for this rep):
- [Link if truly needed]

**After Shipping — Reflection**:
- What actually happened?
- What worked / didn't?
- What surprised you?
- Rate: __/10
- One thing differently next time?

---

## Rep 2: [Next Iteration]
**Builds on**: Rep 1 + [learning]
**New challenge**: [Single new element]

## Rep 3: [Continue Progression]
...

## Reps 4–5: Future Path
*(Evolve based on learnings from Reps 1–3)*

---
Remember: 100 reps beats 100 hours of study. Ship it, then improve it.
```

### 13.7 Knowledge Graph Workspace File Format

Save as JSON for programmatic access:

```json
{
  "graph_name": "Research Topic Knowledge Graph",
  "created": "2025-03-03",
  "version": 1,
  "entities": [
    {
      "id": "e001",
      "name": "Entity Name",
      "type": "Person|Organization|Concept|Event|Place|Claim",
      "description": "Brief description",
      "sources": ["https://source-url.com"],
      "confidence": "High|Medium|Low",
      "date_of_info": "2024-Q4"
    }
  ],
  "relationships": [
    {
      "from": "e001",
      "to": "e002",
      "type": "AUTHORED|FOUNDED|CITES|CONTRADICTS|APPLIES_TO|PRECEDED",
      "description": "Optional context",
      "source": "https://source-url.com",
      "confidence": "High|Medium|Low"
    }
  ],
  "clusters": [
    {
      "id": "c001",
      "label": "Cluster Name",
      "entities": ["e001", "e002", "e003"],
      "description": "What this cluster represents"
    }
  ],
  "research_gaps": [
    "No sources on the relationship between X and Y",
    "Only one low-confidence source for claim Z"
  ]
}
```

---

## Quick Reference Card

### When to use which search tool

| Need | Tool | Notes |
|---|---|---|
| Current news / events | `search_web` | Use date in query for recency |
| Research papers | `search_vertical(academic)` | Returns DOIs; fetch primary source |
| Brand sentiment | `search_social` | Use `from:`, `#hashtag`, `-is:retweet` operators |
| Product research | `search_vertical(shopping)` | Returns price + source URL |
| Professional profiles | `search_vertical(people)` | LinkedIn-based |
| Specific page content | `fetch_url` with prompt | Always fetch primary; not aggregators |
| Live webpage visual | `screenshot_page` | For UI capture, competitive analysis |

### Statistical test quick-reference

| Data Type | Two Groups | Three+ Groups | Paired | Association |
|---|---|---|---|---|
| Normal, continuous | t-test | ANOVA | Paired t-test | Pearson r |
| Non-normal, continuous | Mann-Whitney U | Kruskal-Wallis | Wilcoxon | Spearman r |
| Binary / proportion | z-test for proportions | Chi-square | McNemar | Phi coefficient |

### Chart selection (one line)

- **Over time** → Line chart
- **Comparison** → Horizontal bar (sorted by value)
- **Distribution** → Histogram + mean/median lines
- **Correlation** → Scatter plot (2 vars) or heatmap (many vars)
- **Composition** → Stacked bar (few cats) or treemap (hierarchy)
- **Segments** → Small multiples

### Confidence levels for claims

| Level | Criteria |
|---|---|
| **High** | Multiple independent primary sources agree; peer-reviewed or official data |
| **Medium** | Single primary source; or multiple secondary sources in agreement |
| **Low** | Single secondary source; unverified; or sources conflict |
| **Unverified** | Claimed but not yet sourced; needs follow-up |
