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
- Retrieval: (fill at 16:15 after reading ch. 6)
- Corpus scope: (Day 2, corpus exploration)
