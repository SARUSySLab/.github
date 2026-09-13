# Como contribuir

Este arquivo vale para todos os repositórios da organização SARU Systems Lab que não
tiverem um `CONTRIBUTING.md` próprio.

## Passo a passo

1. Abra uma issue nova ou pegue uma existente, com prefixo de família no título e no
   rótulo (`E`, `PIL`, `CAM`, `ENG`, `EQP`, `ALU`).
2. Crie a branch a partir da issue, já com o nome no padrão `<prefixo>/<numero>-<tema>`,
   em minúsculas e com hífen entre palavras, e mude para ela:
   `gh issue develop <numero> --name pil/42-corte-de-volta-por-gps --checkout`.
3. Confira com `git branch --show-current` que está na branch certa antes do primeiro commit.
4. Faça commits em Conventional Commits, em português, até 72 caracteres no título
   (exemplo: `feat: adiciona corte de volta por GPS`).
5. Abra o pull request com `Closes #<numero>` na descrição, para a issue fechar
   automaticamente quando o PR for mesclado.
6. Espere a CI ficar verde e a revisão de outra pessoa. Nenhum agente de IA aprova ou
   mescla pull request.
7. Mescle por squash: um commit só na `main` e histórico linear (decisão de 2026-09-13).
8. Apague a branch depois do merge.

## Definition of Ready

Uma issue entra em desenvolvimento quando, nesta ordem:

1. Tem id com prefixo e está no catálogo da família.
2. Tem fonte registrada.
3. Diz para quem e para quê, e aponta um objetivo.
4. Tem pelo menos um critério de aceitação em Dado, Quando, Então.
5. As dependências estão listadas e nenhuma está bloqueada.
6. Cabe em uma semana de sprint; senão, é quebrada antes de entrar.
7. Quem vai fazer entendeu o escopo; dúvida vira pergunta a Vitor antes de começar, não
   no meio.
8. Se toca física, calibração ou validação, a regra já foi validada com Vitor contra o
   acervo; se toca formato de arquivo, o arquivo real está anexado à issue.

## Definition of Done

Um item está pronto quando:

1. Cada critério de aceitação foi verificado por teste automatizado ou demonstração
   registrada.
2. Lint e testes estão verdes na CI.
3. O catálogo e a matriz de rastreabilidade da família foram atualizados no mesmo PR.
4. A documentação de uso foi atualizada, se a interface mudou.
5. O PR foi revisado por outra pessoa; nenhum push direto na `main`.
6. Se o item toca o núcleo compartilhado, o catálogo da empresa também foi atualizado.
7. O incremento foi demonstrado e aceito: o teste verde prova que funciona, não que é o
   que se queria.

## Uso de IA

Toda contribuição gerada majoritariamente por um agente de IA leva, na descrição do
pull request, a marca do agente e o nome de quem revisou (exemplo: gerado por Claude
Code, revisado por Vitor Toledo). Nenhum agente de IA aprova ou mescla pull request
sozinho. A revisão humana antes do merge é sempre obrigatória, sem exceção para
contribuição de agente.

## Segredo

Cada repositório lista suas variáveis de ambiente em `.env.example`, sem valor real.
O arquivo `.env` nunca é commitado; fica sempre em `.gitignore`. Segredo de produção
mora em GitHub Secrets, nunca em arquivo de configuração do repositório.
