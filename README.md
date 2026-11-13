# amostras-data

Lista pública usada pelo app **Amostras Grátis** (Android, `com.trekmobi.amostras`): um guia de
programas oficiais de amostras, testes de produto e avaliação.

- `programs.json` — a lista. O app baixa
  `https://raw.githubusercontent.com/Trek-Mobi-Connect/amostras-data/main/programs.json` ao abrir,
  valida o arquivo inteiro (schema `schemaVersion: 1`), guarda em cache e, se algo falhar, usa a
  cópia salva ou a que vem dentro do app.
- Só dados públicos: nome do programa, empresa, países, como funciona, custos e condições, link
  oficial e a data em que a página oficial foi conferida. Nenhum segredo, nenhum dado de usuário.

## Regras da lista

1. Só entra programa que existe hoje, com página oficial no domínio da própria empresa, aberta e
   lida por uma pessoa (data em `verifiedAt`).
2. A forma de acesso é dita como é: `open`, `selection`, `invite`, `raffle`, `points`,
   `purchase`, `club`. Nada de "grátis garantido".
3. Programa encerrado sai da lista; o app o remove na abertura seguinte.

Este repositório é atualizado pelo script `npm run data:publish` do repositório do app (que roda
a validação e confere todos os links oficiais antes). Não editar à mão.

O guia é independente e não tem vínculo com as empresas citadas.
