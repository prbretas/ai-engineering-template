# ai-engineering-template

> Template base para projetos de engenharia de software assistida por IA.
> Clone, adapte e comece a desenvolver com um fluxo profissional já configurado.

[![Use this template](https://img.shields.io/badge/Use%20this%20template-2ea44f?style=for-the-badge&logo=github)](https://github.com/prbretas/ai-engineering-template/generate)

---

## O que está incluído

Este template traz uma estrutura completa e pronta para uso:

| Recurso | Descrição |
|---|---|
| `.github/ISSUE_TEMPLATE/` | Template de User Story para novas issues |
| `.github/copilot-instructions.md` | Instruções de contexto para o GitHub Copilot |
| `.github/instructions/docs.instructions.md` | Instruções para geração de documentação |
| `.github/pull_request_template.md` | Template automático para Pull Requests |
| `scripts/start_issue.sh` | Cria branch a partir de uma issue |
| `scripts/open_pr.sh` | Abre PR vinculado à issue atual |
| `scripts/create_issues.sh` | Cria épico e stories em lote via GitHub CLI |
| `docs/` | Estrutura de documentação do produto |
| `src/` | Pasta para o código-fonte do projeto |

---

## Como usar este template em um novo projeto

### Passo 1 — Criar o repositório a partir do template

Clique no botão **"Use this template"** no topo desta página, ou via terminal:

```bash
gh repo create {seu-usuario}/{nome-do-projeto} \
  --template prbretas/ai-engineering-template \
  --public \
  --clone
```

Substitua `{seu-usuario}` e `{nome-do-projeto}` pelos valores reais.

---

### Passo 2 — Entrar na pasta do projeto

```bash
cd {nome-do-projeto}
```

---

### Passo 3 — Personalizar o README

Abra o `README.md` e substitua:

- `{PROJECT_NAME}` → nome do seu projeto
- `{OWNER}` → seu usuário do GitHub
- `{REPO}` → nome do repositório

Você pode usar o template em `docs/templates/README_TEMPLATE.md` como base.

---

### Passo 4 — Atualizar o product.md

Edite `docs/product.md` com a visão do seu produto:

- Objetivo do projeto
- Público-alvo
- Funcionalidades principais

---

### Passo 5 — Atualizar as instruções do Copilot

Edite `.github/copilot-instructions.md` com o contexto do seu projeto para que o GitHub Copilot entenda o domínio e as convenções adotadas.

---

### Passo 6 — Criar as labels no repositório

Execute o script abaixo para criar as labels padrão (`epic`, `story`, `priority:high`, etc.):

```bash
gh label create "epic"        --color "#6f42c1" --description "Epic"
gh label create "story"       --color "#0052cc" --description "User Story"
gh label create "priority:high"   --color "#e11d48" --description "Alta prioridade"
gh label create "priority:medium" --color "#f97316" --description "Media prioridade"
gh label create "frontend"    --color "#06b6d4" --description "Frontend"
gh label create "backend"     --color "#10b981" --description "Backend"
gh label create "ai"          --color "#8b5cf6" --description "Inteligencia Artificial"
```

---

### Passo 7 — Criar o épico e as issues

Edite o arquivo `scripts/create_issues.sh` com os épicos e stories do seu projeto, depois execute:

```bash
bash scripts/create_issues.sh
```

O script cria todas as issues no GitHub e vincula as stories ao épico automaticamente.

---

### Passo 8 — Criar o projeto Kanban

```bash
gh project create --owner {seu-usuario} --title "{Nome do Projeto}"
```

Configure as colunas: **Backlog → Refinamento → Doing → Code Review → Done**.

---

### Passo 9 — Começar a desenvolver

Para iniciar o trabalho em uma issue:

```bash
bash scripts/start_issue.sh
```

O script lista as issues abertas, você escolhe o número e ele cria a branch no padrão correto.

Quando terminar a implementação, abra o PR:

```bash
bash scripts/open_pr.sh
```

O PR já vem com título no padrão Conventional Commits e o template preenchido.

---

## Fluxo completo de desenvolvimento

```
1. gh repo create → a partir deste template
2. Personalizar README, product.md e copilot-instructions.md
3. bash scripts/create_issues.sh → criar épico e stories
4. gh project create → criar kanban
5. bash scripts/start_issue.sh → iniciar uma issue
6. Implementar + commits (feat:, fix:, docs:...)
7. bash scripts/open_pr.sh → abrir PR
8. Code review + merge
9. Deletar branch
10. Repetir a partir do passo 5
```

---

## Convenções

**Branches:**
```
feature/<issue-id>-descricao
fix/<issue-id>-descricao
docs/<issue-id>-descricao
```

**Commits (Conventional Commits):**
```
feat: implementa funcionalidade
fix: corrige comportamento
docs: atualiza documentacao
chore: ajusta configuracao
test: adiciona testes
refactor: refatora implementacao
```

---

## Pré-requisitos

- [GitHub CLI](https://cli.github.com/) instalado e autenticado (`gh auth login`)
- Bash (nativo no Linux/Mac, Git Bash no Windows)
- Permissão de escrita no repositório

---

## Projetos que usam este template

| Projeto | Descrição |
|---|---|
| [ai-software-engineering](https://github.com/prbretas/ai-software-engineering) | Shop4u — MVP mobile de e-commerce com IA |

---

## Licença

MIT