# Roadmap 2026 Q2-Q3-Q4 — geo-taxonomy

> Fonte: `.cto/review-2026-05-04-masterplan-15-repos.md` (documento interno, fora deste repo) e `planoCTO.html` (913 linhas).
> Próxima revisão CTO: **2026-08-01**.
> Owner: **Alexandre Caramaschi**.

## Estado em 30/09/2026

- A onda Q3-W6 (sincronização de 60 para 80 termos, janela de 15/09 a 30/09/2026) não foi entregue. `python scripts/taxonomy_tools.py check` confirma 61 termos em 7 categorias, com JSON, CSV e Markdown sincronizados, e a issue #2 continua aberta.
- A revisão CTO marcada para 01/08/2026 não deixou registro neste repositório. Replanejar a onda para o Q4 ou encerrá-la é decisão do owner.
- Desde 08/07/2026 o repositório recebeu apenas commits de documentação (diretriz editorial v2 em 23/07 e v4 em 11/08).

## Sumário

- **Categoria:** spec-publica
- **Criticidade:** baixa
- **Deadline principal do trimestre:** 2026-09-30 (60 → 80 termos)
- **Gates obrigatórios:** —

## Decisões pendentes do owner

_Nenhuma decisão pendente listada na auditoria CTO de 2026-05-04._

## Q2 2026 (mai-jun-jul) — janelas críticas

_Sem ondas planejadas para Q2 2026._

## Q3 2026 (ago-set-out) — consolidação e infraestrutura

| ID | Janela | Esforço (h) | Owner | Critical path | Saída esperada | Pré-requisitos |
|---|---|---|---|---|---|---|
| Q3-W6 | 15-09 a 30-09 | 10 | Alexandre | Não | Sincronizacao 60 → 80 termos | — |

## Q4 2026 (nov-dez-jan/27) — captação 2027.1 + colheita

_Sem ondas planejadas para Q4 2026._

## Observabilidade

Termos cobertos, downloads CSV/JSON, citacoes em papers.

## Política de qualidade

Toda mudança neste repo passa pelos gates transversais aplicáveis:

- **Quality gate canônico** (Next.js/TS): `tsc` + `lint` + `vitest` + `next build` antes de push.
- **Voice Guard** (conteúdo Alexandre): `python scripts/python/voice_guard.py check --file ...` antes de publicar.
- **Migration gate pt_br** (SQL): grep de acentos obrigatório antes de `apply` via Management API.
- **Pre-commit hook** (todo repo cliente): `secret_guard` ativo via `git config core.hooksPath .githooks`.
- **Snapshot Shopify** (mutations produto/variant): JSON em `data/raw/shopify-audit-logs/` antes de `productUpdate`/`variantsBulkUpdate`.
- **Browser MCP visual double-check** (mudanças de UI): `getComputedStyle` antes/depois em 1440x900 e 390x844.
- **Schema.org JSON-LD** (todo conteúdo público): validação com `validate_graphql_codeblocks` ou Rich Results.

## Disciplina de deploy

- `landing-page-geo`: teto de **6 deploys/dia**, elevado de 2 para 6 em 24/07/2026 como disciplina de agrupamento. Conferido contra a fatura em 31/08/2026, um push custa cerca de US$ 0,15, quase todo em minutos de GitHub Actions, que passaram a ser a métrica de controle.
- Pre-push hook roda `next build` localmente; falhar localmente = abortar push.
- Janelas com 2+ streams paralelos exigem revisão semanal de carga em segunda 09h BRT.

## FinOps

- LLM API spend rastreado em `geo-finops/calls.db` ([repositório geo-finops](https://github.com/alexandrebrt14-sys/geo-finops)).
- Build minutes Vercel monitorados; alertas WhatsApp/email em ≥80% da quota.
- Quebrar prompts no orchestrator: `< 5KB` input e `< 30KB` output (limite Gemini MAX_TOKENS).

## Política de revisão

- Toda decisão arquitetural significativa registrada como ADR em `docs/adr/`.
- Drift entre `adminalexandre` e `landing-page-geo`: pre-commit hook (deadline 20-05).
- Revisão CTO trimestral próxima: **2026-08-01**.

---

_Gerado automaticamente pela skill `/cto` em 2026-05-04 a partir do masterplan dos 15 repositórios._
