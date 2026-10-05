# CircularQA: design v0.1

## 1. Problem
<!-- Teams need the CURRENT RBI rule with a citation; old circulars get superseded. -->

## 2. Users
<!-- Bank/NBFC/fintech compliance staff; RBI Grade B and JAIIB/CAIIB aspirants. -->

## 3. Scope
### By day 90
<!-- Ingestion, cited answers, superseded-rule filtering, evals, deployed API + simple UI. -->
### Later
<!-- MCP server, "what changed" view. -->

## 4. Architecture
### Ingestion path
<!-- crawl -> parse -> link supersessions -> chunk -> embed -> Postgres -->
### Query path
<!-- FastAPI -> retrieve -> rerank -> LLM -> citation check -->

## 5. Metrics
| Metric | Baseline | Target |
|---|---|---|
| Recall@5 | TBD | TBD |
| MRR@10 | TBD | TBD |
| Citation precision | TBD | TBD |
| Stale-rule rate | TBD | TBD |
| Refusal accuracy | TBD | TBD |
| p95 latency | TBD | TBD |
| Cost per 100 queries | TBD | TBD |

## 6. Risks
<!-- Messy PDFs/tables, missed supersession links, LLM cost, site rate limits. -->

## 7. Decisions
- - Retrieval: v0 = vector-only baseline (pgvector). v1 = hybrid: Postgres full-text
  search + vector, merged with reciprocal rank fusion. Keep v1 only if it beats v0
  on Recall@5 and MRR@10 on the golden set. Expected gain: queries often contain
  exact circular numbers and acronyms that embeddings handle poorly.
- Corpus scope: (Day 2, corpus exploration)
