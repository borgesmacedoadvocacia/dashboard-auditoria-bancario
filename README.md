# Dashboard — Auditoria — Direito Bancário

Painel da planilha **Auditoria Completa - Direito Bancário** do escritório Borges Macedo Advocacia, lido em
tempo real (aba `Auditoria` e as abas derivadas `Painel`, `Painel - detalhe`, `Plano de ação`).
Ferramenta para extrair relatórios, olhar a carteira por recorte e decidir estratégia.

**Acesso exclusivo das lideranças.** Os perfis Administração e Lideranças têm cofre neste painel; entra-se pela
[Central de Dashboards](https://borgesmacedoadvocacia.github.io/).

## Como funciona

- Os indicadores são os da aba **Painel** da planilha. O painel lê as **fórmulas originais** (COUNTIF, COUNTIFS,
  SUMIFS, SUM, AVERAGE, COUNTA…) e as **recalcula no navegador** sobre a aba Auditoria. Por isso:
  - todo cartão abre a lista exata dos processos que compõem o número (com a coluna usada no critério);
  - todos os cartões respeitam o **recorte** escolhido (banco, status, fase, tribunal, grau, tese, faixa de
    probabilidade, prioridade, responsável, situação da liminar, resultado da sentença, busca por processo/cliente);
  - se você mudar uma fórmula ou acrescentar uma linha na aba Painel, o painel acompanha sem alteração de código.
    Fórmulas fora do subconjunto suportado mostram o valor calculado pela própria planilha (sem lista) e são apontadas em "Pontos de atenção".
- **Prioridades por processo** — os blocos da aba `Painel - detalhe` (urgentes, liminares aptas, maduros, caixa…), cada um exportável.
- **Plano de ação** — abertos / urgentes / prazo vencido / concluídos, ordenado por prioridade e prazo.
- **Carteira auditada** — uma linha por processo; o clique abre a ficha completa (todas as colunas da Auditoria, agrupadas como na planilha, com o plano de ação do processo e link para a linha na planilha).
- **Pontos de atenção** — as falhas com maior volume e a ação recomendada pela planilha, atos com prazo vencido e eventuais divergências com a aba Painel.

## Relatórios

- **Relatório completo (XLSX)** — abas Painel (indicador, valor, ação, processos), Prioridades, Plano de ação e Auditoria do recorte.
- **Painel (CSV)** — só os indicadores.
- Em qualquer lista aberta a partir de um cartão: **Exportar XLSX** / **CSV**.
- Blocos de prioridades, plano de ação e carteira têm botão próprio de XLSX.
- **Imprimir / PDF** — layout de impressão do painel inteiro.

Tudo respeita o recorte ativo no momento da exportação.

## Estrutura

- `index.html` — painel completo (cofres, guarda da central, Sheets API v4, Chart.js, SheetJS para XLSX).
- Publicação: GitHub Pages via Actions (`.github/workflows/pages.yml`), a cada push em `main`.
- Planilha: `https://docs.google.com/spreadsheets/d/1gjFYXYOmZyskANqlth9EVXwlTuNIujpF_xtF_OM5zO4/edit`
