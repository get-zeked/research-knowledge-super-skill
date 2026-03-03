---
name: research-knowledge-super-skill
description: Comprehensive research and knowledge management skill merging Perplexity Computer's research, data exploration, statistical analysis, and visualization skills with Claude Code's tapestry knowledge graphs, article extraction, content research, brainstorming, RAG system building, and prompt engineering. Covers deep research workflows, knowledge graph construction, academic research, data analysis, statistical methods, content synthesis, and AI-powered information retrieval. Use for research projects, literature reviews, data analysis, knowledge management, competitive research, or any investigation requiring deep synthesis.
license: MIT
metadata:
  author: get-zeked
  version: '1.0'
---

# Research & Knowledge Super-Skill

A unified research and knowledge management system merging deep research workflows, data profiling, statistical methods, visualization, knowledge graph construction, content extraction, RAG systems, brainstorming, and iterative learning.

---

## 1. Gap Analysis: Perplexity Computer vs Claude Code Skills

| Capability | Perplexity Computer | Claude Code | Combined Advantage |
|---|---|---|---|
| Live web search | Native, real-time | None (static) | Perplexity for current facts |
| Academic search | Dedicated vertical | None natively | Perplexity for papers/citations |
| Knowledge graph construction | Not native | Tapestry skill | Claude for local doc synthesis |
| Article extraction | fetch_url + LLM | article-extractor + trafilatura | Both; Claude for batch processing |
| YouTube transcript extraction | No yt-dlp | yt-dlp + VTT deduplication | Claude for video corpus |
| Data exploration (CSV/SQL) | Full Python/SQL | Bash tools | Perplexity for live analysis |
| Statistical analysis | Full scipy/statsmodels | Limited | Perplexity for serious stats |
| Data visualization | matplotlib/seaborn/plotly | Bash + Python | Perplexity produces rendered charts |
| RAG evaluation | Can build/evaluate | rag_evaluator.py scripts | Both; different strengths |
| Multi-agent parallelism | Subagent spawning | Single conversation | Perplexity for parallel research |
| External integrations | 400+ connected services | File system / local | Perplexity for live external data |

**Routing Decision Rule**:
- Current information, live data → **Perplexity Computer**
- Local file corpus, video transcripts, iterative plans → **Claude Code**
- Statistical analysis, visualization → **Perplexity Computer**
- Knowledge graph from documents, RAG evaluation → **Claude Code**

---

## 2. Research Methodology & Workflows

### Research Hierarchy

| Tier | Question Type | Approach |
|---|---|---|
| **Tier 1** | Single verifiable fact | One search; cite source |
| **Tier 2** | Comparative analysis | Parallel searches; synthesis table |
| **Tier 3** | Investigative / exploratory | Iterative search; subagent parallelism |
| **Tier 4** | Literature review / meta-analysis | Academic search; citation network |
| **Tier 5** | Strategic intelligence | Competitive research; 400+ integrations |

### Deep Research Workflow (4 Phases)

1. **Orientation** (5-10 min): 3 seed queries, parallel searches, map knowledge landscape
2. **Deep Dive** (15-45 min): Fetch primary sources, cross-reference claims, academic layer, save to workspace
3. **Synthesis** (10-20 min): Claims registry, consensus vs. contested, draft research brief
4. **Quality Check**: Verify quantitative claims, check primary sources, survivorship bias check

### Parallelized Subagent Research

```
Master Agent Plan:
├── Subagent A: Topic domain X → saves to workspace/research-A.json
├── Subagent B: Topic domain Y → saves to workspace/research-B.json
├── Subagent C: Collect verified image/media URLs
└── Master Agent: Reads all workspace files, synthesizes, builds final artifact
```

---

## 3. Knowledge Graph Construction

### Entity Types
```
Person, Organization, Concept, Event, Place, Claim
```

### Relationship Types
```
X AUTHORED Y, X FOUNDED Y, X INTRODUCED Y, X CONTRADICTS Y,
X CITES Y, X APPLIES_TO Y, X PRECEDED Y
```

### Tapestry Workflow
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
   [Create Ship-Learn-Next Action Plan]
        ↓
   Output: content_file.txt + action_plan.md
```

---

## 4. Content Extraction & Synthesis

### Article Extraction Tool Priority
1. `reader` (Mozilla Readability CLI) — best all-around
2. `trafilatura` (Python) — best for blogs, news, non-English
3. `fetch_url` with LLM prompt — best for Perplexity Computer
4. `curl` + HTMLParser — fallback

### Source Quality Tiers

| Tier | Type | Trust Level |
|---|---|---|
| 1 | Peer-reviewed meta-analysis | Highest |
| 2 | Primary peer-reviewed study | Very high |
| 3 | Government / institutional data | High |
| 4 | Primary news reporting | Medium-high |
| 5 | Industry reports | Medium |
| 6-7 | Expert blog / general blog | Low-Medium |
| 8 | Social media post | Very low |

---

## 5. Data Exploration & Profiling

### Column Classification
| Type | Description | Examples |
|---|---|---|
| Identifier | Unique keys | user_id, order_id |
| Dimension | Categorical | status, region, plan_type |
| Metric | Quantitative | revenue, duration, count |
| Temporal | Dates/timestamps | created_at, event_date |

### Data Quality Assessment
| Null Rate | Status | Action |
|---|---|---|
| >99% non-null | Green / Complete | No action |
| 95-99% non-null | Yellow / Mostly complete | Investigate |
| 80-95% non-null | Orange / Incomplete | Understand why |
| <80% non-null | Red / Sparse | Imputation or exclusion |

---

## 6. Statistical Analysis & Methods

### Common Statistical Tests
| Scenario | Test | Python |
|---|---|---|
| Compare two group means | Independent t-test | `scipy.stats.ttest_ind` |
| Compare conversion rates | Z-test for proportions | `statsmodels.stats.proportion.proportions_ztest` |
| Non-normal data | Mann-Whitney U | `scipy.stats.mannwhitneyu` |
| Two categorical variables | Chi-squared | `scipy.stats.chi2_contingency` |

### Statistical Pitfalls Checklist
| Pitfall | Prevention |
|---|---|
| Correlation ≠ causation | State explicitly; consider confounders |
| Multiple comparisons | Apply Bonferroni correction |
| Simpson's paradox | Always check segment-level results |
| Survivorship bias | Ask: who is missing? |

---

## 7. Data Visualization

### Chart Selection Guide
| What You're Showing | Best Chart |
|---|---|
| Trend over time | Line chart |
| Comparison across categories | Horizontal bar chart |
| Distribution | Histogram or box plot |
| Part-to-whole | Bar (stacked) or treemap |
| Correlation | Scatter plot |

---

## 8. Data Validation & QA

### Pre-Delivery Checklist (24 items)
- [ ] Row counts match expected ranges
- [ ] No duplicate primary keys
- [ ] All date ranges valid
- [ ] Null rates within acceptable thresholds
- [ ] Aggregations match source data
- [ ] Statistical claims verified against source
- [ ] No survivorship bias in dataset
- [ ] Correlation/causation clearly distinguished

---

## 9. Creative Ideation & Brainstorming

**Hard-gate rule**: Complete brainstorming before any implementation.

**Techniques**: Lateral thinking, SCAMPER, reverse brainstorming, random stimulation, constraint-based ideation.

---

## 10. RAG Systems & AI-Powered Research

### RAG Pipeline Architecture

```
Documents → [Loader] → [Chunker] → [Embedder] → [Vector Store]
                                                        ↓
Query → [Query Embed] → [Vector Search] → [Reranker] → [LLM]
```

### Chunking Strategies
- **Fixed-size**: 512 tokens with 64-token overlap (general text)
- **Sentence-boundary**: 5 sentences per chunk (structured prose)
- **Recursive**: Hierarchical, preserves section structure (long docs)

### RAG Evaluation Metrics
- Context Recall: % of answer evidence present in retrieved chunks
- Context Precision: % of retrieved chunks that are relevant
- Answer Faithfulness: answer grounded in retrieved context
- Answer Relevance: answer directly addresses the question

---

## 11. Iterative Learning (Ship-Learn-Next)

```
Ship: Define what you're releasing and its success criteria
Learn: What did you observe? What worked? What didn't?
Next: What's the highest-leverage next step based on learnings?
```

---

## 12. Unique Perplexity Computer Capabilities

- Real-time web search with source citations
- 400+ external service integrations
- Parallel subagent research coordination
- Academic paper search with DOI resolution
- Social media monitoring (X/Twitter)
- Memory across sessions via memory_search

---

*Research & Knowledge Super-Skill v1.0 — Merged from Perplexity Computer research-assistant, data-exploration, data-validation, data-visualization, statistical-analysis, and Claude Code Tapestry, article-extractor, YouTube-transcript, ship-learn-next, content-creator, brainstorming, prompt-engineer/RAG skills.*
