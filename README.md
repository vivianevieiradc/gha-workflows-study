# GitHub Actions Study

<div align="center">

  <img src="https://img.shields.io/badge/GitHub%20Actions-Study-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions Study" />
  <img src="https://img.shields.io/badge/YAML-Workflow-3178C6?style=for-the-badge&logo=yaml&logoColor=white" alt="YAML Workflow" />
  <img src="https://img.shields.io/badge/Status-Learning-34D399?style=for-the-badge" alt="Status Learning" />

</div>

Repositório de estudo para aprender GitHub Actions na prática, com workflows simples, gatilhos, execução de jobs e observação do ambiente do runner.

## 🚀 Visão geral

Este projeto foi pensado como um laboratório para entender como funcionam fluxos de automação em GitHub, desde a criação do primeiro workflow até a análise dos eventos que o disparam.

### O que está sendo praticado

- criação de workflows em YAML
- uso de gatilhos como `push`, `pull_request` e `workflow_dispatch`
- execução de `jobs` e `steps`
- uso do runner `ubuntu-latest`
- observação do ambiente do build
- depuração básica de automações

---

## 📁 Estrutura do projeto

```text
.
├── .github/
│   └── workflows/
│       ├── ga-01-first-workflow.yml
│       ├── ga-02-investigate-runner.yml
│       └── ga-03-triggers.yml
├── README.md
└── .gitignore
```

---

## 🧩 Workflows do repositório

### GA-01 — First Workflow
Arquivo: [.github/workflows/ga-01-first-workflow.yml](.github/workflows/ga-01-first-workflow.yml)

- Trigger: `workflow_dispatch`
- Objetivo: validar a estrutura mínima de um workflow
- Comportamento:
  - faz checkout do código
  - executa comandos simples com `echo`

### GA-02 — Investigate Runner
Arquivo: [.github/workflows/ga-02-investigate-runner.yml](.github/workflows/ga-02-investigate-runner.yml)

- Trigger: `workflow_dispatch`
- Objetivo: explorar o ambiente da máquina que executa o job
- Comportamento:
  - mostra usuário atual
  - exibe diretório atual
  - verifica o sistema operacional
  - lista arquivos
  - mostra uso de disco
  - cria um arquivo de teste dentro do job

### GA-03 — Triggers
Arquivo: [.github/workflows/ga-03-triggers.yml](.github/workflows/ga-03-triggers.yml)

- Trigger: `workflow_dispatch`, `push`, `pull_request`
- Objetivo: entender como diferentes eventos disparam a automação
- Comportamento:
  - imprime o nome do evento que iniciou o workflow com `${{ github.event_name }}`

---

## 🧠 Conceitos estudados

### Workflow
É um arquivo YAML dentro de `.github/workflows` que define a automação.

### Job
Um job representa um conjunto de passos executados em um runner.

### Step
Cada step é uma etapa da execução, como executar um comando shell ou usar uma ação do marketplace.

### Runner
É o ambiente de execução do job. Neste projeto, o runner usado foi `ubuntu-latest`.

### Eventos
São gatilhos que iniciam o workflow, como:

- `push`
- `pull_request`
- `workflow_dispatch`

---

## ▶️ Como executar

1. Acesse o GitHub e abra o repositório.
2. Vá até a aba `Actions`.
3. Escolha o workflow que deseja rodar.
4. Se o gatilho for manual, clique em `Run workflow`.

---

## 📌 Objetivo do estudo

Este repositório funciona como um laboratório prático para aprender:

- sintaxe de workflows em YAML
- gatilhos e eventos do GitHub
- configuração de jobs e steps
- debug básico de automações
- estrutura de pipelines simples

---

## 🔜 Próximos passos

- adicionar condições com `if`
- trabalhar com `matrix` e múltiplos jobs
- usar `env` e `secrets`
- criar workflows de teste e build
- evoluir para deploy automático

---

## 🛠️ Tecnologias envolvidas

- GitHub Actions
- YAML
- Shell Script
- Linux / Ubuntu runner

---

## 👤 Autor

Projeto pessoal para estudo e prática de automação com GitHub Actions.
