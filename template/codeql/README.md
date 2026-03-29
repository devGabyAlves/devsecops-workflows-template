# Template de Workflow CodeQL 

Este repositório fornece um workflow pronto para uso no GitHub Actions utilizando o CodeQL para análise estática de código (SAST).

O objetivo é facilitar a implementação de práticas de DevSecOps, integrando segurança diretamente no pipeline de CI/CD.

---

## Funcionalidades

- Análise automatizada com CodeQL em push e pull requests
- Execução agendada semanal (scan contínuo)
- Suporte a múltiplas linguagens (JavaScript, Python, etc.)
- Uso de queries avançadas (`security-extended`, `security-and-quality`)

---

##  O que é o CodeQL?

O CodeQL é uma ferramenta de análise estática desenvolvida pelo GitHub que trata o código como dados, permitindo identificar vulnerabilidades e problemas de qualidade.

---

## Como utilizar

1. Copie o arquivo de workflow para o seu repositório:
```bash
.github/workflows/codeql-advanced-analysis.yml
```

2. Faça commit e push.

3. Visualize os resultados em: Security > Code scanning alerts

---

## Customizações

Adicionar mais linguagens
```bash
matrix:
  language: [ 'javascript', 'python', 'java', 'go' ]
```

Alterar frequência de execução
```bash
schedule:
  - cron: '0 3 * * 1'
```

Alterar pacotes de queries
```bash
queries: security-extended,security-and-quality
```

