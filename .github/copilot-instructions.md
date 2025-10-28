## Instruções rápidas para agentes de coding (Projeto HTML-CSS)

Essas instruções ajudam um agente AI a ser produtivo rapidamente neste repositório: um conjunto de exemplos e exercícios estáticos em HTML/CSS, organizados por pastas.

- Estrutura principal:
  - `ex001/` .. `ex028/` — exercícios individuais. Cada pasta normalmente contém um `index.html` (ou páginas nomeadas) e um `style.css` ou outro CSS local.
  - `cores/` — exemplos de layout/estilos compartilhados (ex: `cores/index.html`, `cores/style.css`).
  - `desafios/` — pastas com exercícios maiores e pacotes (veja `desafios/d009/` com vídeos e `desafios/d010/pacote-projeto-d010/`).
  - `projeto-cordel/` — projeto dedicado com sua própria estrutura.

- Padrões observados (importante):
  - Arquivos CSS frequentemente chamados `style.css` ao lado do HTML. Ex.: `ex028/style.css`, `ex015/style.css`.
  - Imagens e mídias se repetem em pastas com nomes `imagens/`, `img/` ou `midia/`. Prefira manter o mesmo diretório de imagens da página que você altera.
  - Arquivos de entrada têm nomes simples: `index.html`, `pag02.html`, `GRID.html` — não renomeie sem verificar links relativos.

- Workflow dev / como testar alterações localmente:
  - Não há build system. Abra os HTML diretamente no navegador para validar alterações.
  - No Windows PowerShell você pode abrir um arquivo com: `Start-Process 'e:\HTMLCSS\ex028\GRID.html'` ou usar a extensão Live Server no editor para reload ao salvar.
  - Validação recomendada: abrir o HTML modificado no navegador e inspecionar via DevTools (F12).

- Convenções específicas a este repo (para PRs/commits de um agente):
  - Faça mudanças pequenas e localizadas: alterar apenas os arquivos necessários (HTML/CSS/recursos) em uma pasta de exercício.
  - Preserve nomes de arquivos e links relativos. Se mover arquivos, atualize todos os links referenciando-os.
  - Não remova imagens duplicadas sem confirmar que não há referências cruzadas (há várias pastas `imagens/`/`img/`).

- Exemplos concretos para ações comuns:
  - Ajustar estilos do exercício 28: editar `ex028/style.css` (arquivo atualmente aberto pelo desenvolvedor).
  - Corrigir conteúdo de exemplo: editar `cores/index.html` ou `desafios/d009/Videosindex.html` conforme a página alvo.

- Integrações e dependências:
  - Repositório é estático — sem package.json, sem tasks de build, sem testes automatizados.
  - Existem alguns arquivos PHP (`ex025/cadastro.php`) e pastas com pacotes zipados; evite executar ou modificar arquivos server-side sem contexto adicional.

- Critérios de sucesso para mudanças feitas por um agente:
  - HTML continua aberto em browser sem erro 404 em recursos locais (imagens/CSS/js referenciados).
  - Alterações limitadas ao escopo do exercício/feature solicitada.
  - Mensagem de commit clara: ex: `fix(ex028): ajustar espaçamento do header`.

- Situações de bloqueio (quando perguntar ao humano):
  - Se a mudança requer reorganizar imagens entre pastas ou renomear arquivos.
  - Se for necessário adicionar um processo de build ou configurar ferramenta (o repo não tem one).
  - Quando houver arquivos server-side (PHP) relacionados a uma alteração de frontend.

Se alguma parte ficar ambígua, pergunte qual pasta/página específica editar (por exemplo: "Editar `ex010/index.html` ou `ex010/finaestampa.html`?").

-- Fim das instruções
