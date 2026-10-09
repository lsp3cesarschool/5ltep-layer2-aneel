# Signals in https://dadosabertos.aneel.gov.br

Plain-text summary of the latest run of Layer 2 (semantic policies), for readers that do not run
the JavaScript of the [dashboard](https://lsp3cesarschool.github.io/5ltep-layer2-aneel/).
Generated automatically by the publish job from the checked results; do not edit by hand. A signal is a record to review, never a verdict on the data. Only counts are
shown here: the record numbers are on the dashboard and in [`docs/data/rules/`](docs/data/rules/),
and no value read from the portals is published. Times are UTC.

- **Run:** [37937369381](https://github.com/lsp3cesarschool/5ltep-layer2-aneel/actions/runs/37937369381), finished 2026-10-09 13:32 UTC (github-actions)
- **Rules:** 13 (13 evaluated, 0 not evaluated)
- **Sources:** 6 CKAN resources (6 available)
- **Records flagged:** 553
- **L2 pass rate:** 100.0% (checks without a signal / 9,352,574 checks in scope; one check per record and rule)

Signal types: `mismatch` (the check failed), `key not found` (no matching record in the other
source), `missing value`, `invalid value` (unreadable as the declared type), `ambiguous key` (more
than one match). Records outside a rule's scope (`where`) are not signals.

## Rules (most signals first)

| Rule | Records read | Signals | Previous run | Signal types |
|---|---:|---:|---:|---|
| [Plant coordinates missing or outside Brazil](rules/generation/plant-coordinates-outside-brazil.yaml) | 25,045 | 465 | 465 | mismatch 465 |
| [Small hydropower plant (PCH) outside 5,000-30,000 kW](rules/generation/pch-outside-5000-30000-kw.yaml) | 25,045 | 77 | 77 | mismatch 77 |
| [Notice received before it was issued](rules/infraction/notice-received-before-issue.yaml) | 1,619 | 5 | 5 | mismatch 5 |
| [Physical guarantee above the granted power](rules/generation/physical-guarantee-above-granted-power.yaml) | 25,045 | 5 | 5 | mismatch 5 |
| [Fine after appeal higher than the original](rules/infraction/fine-after-appeal-above-original.yaml) | 1,619 | 1 | 1 | mismatch 1 |
| [Board decision dated before the appeal was received](rules/infraction/board-decision-before-appeal.yaml) | 1,619 | 0 | 0 | none |
| [Small hydro generating station (CGH) above 5,000 kW](rules/generation/cgh-above-5000-kw.yaml) | 25,045 | 0 | 0 | none |
| [Generation auction price above the ceiling price](rules/auctions/generation-price-above-ceiling.yaml) | 1,552 | 0 | 0 | none |
| [Microgeneration above 75 kW](rules/distributed-generation/microgeneration-above-75-kw.yaml) | 4,647,773 | 0 | 0 | none |
| [Minigeneration outside 75-5,000 kW](rules/distributed-generation/minigeneration-outside-range.yaml) | 4,647,773 | 0 | 0 | none |
| [Municipality code consistent with the state of the same place](rules/territory/municipality-state.yaml) | 4,647,773 | 0 | 0 | none |
| [Winning annual revenue (RAP) above the auction's ceiling](rules/auctions/transmission-rap-above-edital.yaml) | 488 | 0 | 0 | none |
| [Warning with a penalty amount](rules/infraction/warning-with-fine-value.yaml) | 1,619 | 0 | 0 | none |

## Source health

| Resource | Role | Status | Size | Download | Used by |
|---|---|---|---:|---:|---|
| dadosabertos.aneel.gov.br › resultado-de-leiloes › resultado-leiloes-geracao.csv | primary | available | 0.4 MB | 2.4 s | generation-price-above-ceiling |
| dadosabertos.aneel.gov.br › resultado-de-leiloes › resultado-leiloes-transmissao.csv | primary | available | 0.1 MB | 2.5 s | transmission-rap-above-edital |
| dadosabertos.aneel.gov.br › relacao-de-empreendimentos-de-geracao-distribuida › empreendimento-geracao-distribuida.zip | primary | available | 110.7 MB | 55.0 s | microgeneration-above-75-kw, minigeneration-outside-range, municipality-state |
| dadosabertos.aneel.gov.br › siga-sistema-de-informacoes-de-geracao-da-aneel › siga-empreendimentos-geracao.csv | primary | available | 8.4 MB | 4.8 s | cgh-above-5000-kw, pch-outside-5000-30000-kw, physical-guarantee-above-granted-power, plant-coordinates-outside-brazil |
| dadosabertos.aneel.gov.br › auto-de-infracao › auto-infracao.csv | primary | available | 0.7 MB | 0.5 s | board-decision-before-appeal, fine-after-appeal-above-original, notice-received-before-issue, warning-with-fine-value |
| dadosabertos.tse.jus.br › codigos-oficiais-de-uf-e-municipios-segundo-o-tse-e-o-ibge › Códigos oficiais de UF e municípios segundo o TSE e o IBGE | secondary | available | 0.1 MB | 0.2 s | municipality-state |
