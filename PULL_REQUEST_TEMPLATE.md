## O que mudou

Descreva o que mudou e por quê.

## Requisito e issue

Closes #

## Como revisar

Comandos para rodar localmente e o que checar no resultado.

```bash

```

## Checklist do DoD

- [ ] Cada critério de aceitação foi verificado por teste automatizado ou demonstração registrada.
- [ ] Lint e testes estão verdes na CI.
- [ ] Catálogo e matriz de rastreabilidade da família atualizados no mesmo PR.
- [ ] Documentação de uso atualizada, se a interface mudou.
- [ ] Revisado por outra pessoa; nenhum push direto na `main`.
- [ ] Catálogo da empresa atualizado, se o PR toca o núcleo compartilhado.
- [ ] Incremento demonstrado e aceito.

## Gate de física

Preencher só quando o PR toca modelo físico, calibração ou leitor de formato de dado.
Deixar em branco quando não se aplica.

- [ ] Fixture ou oráculo atualizado.
- [ ] Unidades explícitas em cada canal.
- [ ] Nome de canal estável, sem canal solto sem mapa.
- [ ] Tempo de volta ou banda de erro sem mudança, ou decisão registrada em
      `docs/decisions.md` que justifica a mudança.

## Uso de IA

Se o PR foi gerado majoritariamente por um agente de IA, diga qual agente e quem
revisou.
