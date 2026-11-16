# Ongconecta

Repositório do projeto individual da disciplina **Gerência de Configuração e Processos de Software**
(Engenharia de Software, Turma B). Aplica, no meu próprio repositório, o roteiro da
[Aula 1 — Preparar o repositório do seu projeto](https://github.com/lzcamargo/ongconecta/blob/main/docs/aulas/aula-1-repositorio.md).

Autor: Eduardo Gabriel Macedo (`@Eduardo-Macedo07`).

## O que o repositório contém

| Caminho | Conteúdo |
|---|---|
| `docs/gcs/` | **Plano de GCS** (Avaliação N2 — Gerência, Configuração e Processos de Software), publicado como item de configuração. Ver [docs/README.md](docs/README.md) |
| `.github/pull_request_template.md` | Modelo de Pull Request (PGC 5.2) |
| `.github/CODEOWNERS` | Revisores automáticos por área |
| `.github/ISSUE_TEMPLATE/` | Modelos de Issue: funcionalidade e defeito |
| `.gitignore`, `.gitattributes` | Itens de configuração básicos (PGC 4.1) |
| `.env.example` | Nomes das variáveis de ambiente, sem valores reais |

> Este repositório ainda não tem código de aplicação. Por isso não há lockfile de dependências
> (`package-lock.json`, `requirements.txt` etc.); ele será adicionado junto com a primeira stack.

## Como rodar e testar

Não se aplica por enquanto: o conteúdo atual é documental. Quando houver código, esta seção
passa a descrever instalação, execução e testes.

## Fluxo de trabalho (PGC 3.3 e 5.2)

- A `main` é protegida: **só recebe alterações por Pull Request**, com 1 aprovação do par de
  revisão, histórico linear e sem exceções (nem para o dono).
- Merge somente por **squash**; o título do PR (Conventional Commits) vira a mensagem do commit.
- Branches: `feature/<issue>-<descricao>`.
- Ambientes (GitHub Environments): `staging` e `production`; o `production` exige aprovação do
  revisor obrigatório (o dono do repositório).

## Segredos

Nenhuma senha, token ou chave de API deve ser versionada. Use variáveis de ambiente
(`.env`, ignorado pelo Git) e, em pipelines, GitHub Secrets.
