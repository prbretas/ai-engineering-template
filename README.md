# {PROJECT_NAME}

> Breve descrição do projeto.

[![Issues](https://img.shields.io/github/issues/{OWNER}/{REPO})](https://github.com/{OWNER}/{REPO}/issues)
[![Last Commit](https://img.shields.io/github/last-commit/{OWNER}/{REPO})](https://github.com/{OWNER}/{REPO}/commits/main)

---

## Sobre o projeto

Descreva aqui o objetivo e contexto do projeto.

---

## Funcionalidades

| Funcionalidade | Status |
|---|---|
| Feature 1 | 🔵 Backlog |
| Feature 2 | 🔵 Backlog |

---

## Estrutura do projeto

\\\
{REPO}/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   ├── instructions/
│   ├── copilot-instructions.md
│   └── pull_request_template.md
├── docs/
│   ├── product.md
│   ├── meeting-notes.md
│   ├── backlog.md
│   └── templates/
├── scripts/
│   ├── create_issues.sh
│   ├── start_issue.sh
│   └── open_pr.sh
├── src/
└── CONTRIBUTING.md
\\\

---

## Como usar os scripts

### Iniciar trabalho em uma issue
\\\ash
bash scripts/start_issue.sh
\\\

### Abrir um Pull Request
\\\ash
bash scripts/open_pr.sh
\\\

### Criar issues em lote
\\\ash
bash scripts/create_issues.sh
\\\

---

## Fluxo de desenvolvimento

\\\
main
 └── feature/{issue-id}-{slug}
      └── commits
           └── PR → main
\\\

Padrão de branches: \eature/\, \ix/\, \docs/\
Padrão de commits: \eat:\, \ix:\, \docs:\, \chore:\

---

## Pré-requisitos

- [GitHub CLI](https://cli.github.com/) autenticado (\gh auth login\)
- Bash (Git Bash no Windows)

---

## Contribuindo

Leia o [CONTRIBUTING.md](./CONTRIBUTING.md) antes de abrir uma issue ou PR.

---

## Licença

MIT