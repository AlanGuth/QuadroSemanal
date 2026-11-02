# Painel Pessoal — estrutura

Artifact único (HTML/CSS/JS) com duas abas, dados na capability `db` do artifact.

## Abas
- **Tasks**: post-its distribuídos de domingo a sábado + bandeja "A distribuir". Coleção `tasks`.
- **Projetos**: kanban (Second Brain, Backlog, Executando, Em espera, Finalizado), filtro por projeto, Histórico, gerenciar projetos. Coleções `cards`, `projetos`, `sprints`.

## Coleções
- `tasks`: {text, day (inbox|dom..sab), color 0-11, done, order, created}
- `cards`: {title, projeto, col, order, createdAt, doneAt?}
- `projetos`: {name, color 0-11, status ativo|concluido, order, createdAt, doneAt?}
- `sprints`: id = domingo AAAA-MM-DD, {goal, week}

## Identidade visual (unificada)
- Paleta única de 12 cores, ids 0-11 (tokens `--k0..--k11`, claro e escuro): Amarelo, Rosa, Verde, Azul, Lilás, Laranja, Turquesa, Vermelho, Céu, Lima, Marrom, Cinza.
- Mesma receita nos dois cartões (classe `.tinted`): fundo = cor misturada à superfície (`--tint` 28% claro / 24% escuro), borda `--edge` 55%.
- Post-it: botão de cor abre seletor com as 12 cores. Composer do Tasks e gerenciador de projetos também têm 12.
- Diferença restante: cabeçalho de coluna com faixa no Tasks, sem faixa no Projetos.

## Arquivos
- `claude/painel-pessoal.html`: backup do código publicado.
