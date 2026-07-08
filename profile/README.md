# SARU

SARU e um ecossistema de software para motorsport que conecta telemetria real,
simulacao e decisao tecnica rastreavel.

## Repos

- `saru-app`: produto e plataforma.
- `saru-physics-py`: fisica Python rapida.
- `saru-physics-jl`: fisica Julia de alta fidelidade.
- `saru-docs`: documentacao viva.
- `saru-research`: arquivo historico.

## Processo

Usamos GitHub Flow: `main` protegida, branches curtas, PRs pequenos, CI verde,
CODEOWNERS e Conventional Commits.

## MVP

O primeiro recorte comercial e SA + Sim Reference: importar telemetria real,
normalizar canais, comparar voltas e gerar uma referencia simulada com lastro.
