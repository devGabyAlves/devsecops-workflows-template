# Template de Workflow Semgrep (SAST)

Este repositório fornece um workflow pronto para uso no GitHub Actions utilizando o Semgrep para análise estática de código (SAST).

---

## Funcionalidades

- Análise SAST automatizada em push e pull requests
- Execução rápida (ideal para CI/CD)
- Uso de regras prontas (`security-audit`, `secrets`)
- Suporte a múltiplas linguagens
- Geração de relatório SARIF
- Integração com o dashboard de segurança do GitHub

---

## O que é o Semgrep?

O Semgrep é uma ferramenta de análise estática focada em velocidade e simplicidade, permitindo identificar vulnerabilidades com base em padrões de código.

---

## Como utilizar

1. Copie o arquivo de workflow para o seu repositório:
```bash
.github/workflows/semgrep-analysis.yml
```

2. Faça commit e push.

3. Visualize os resultados em: Security > Code scanning alerts

---

 ## Customizações

Alterar regras utilizadas
```bash
config: >-
  p/security-audit
  p/secrets
```

Adicionar regras customizadas
```bash
config: >-
  p/security-audit
  p/secrets
  path/to/custom-rules
```

Habilitar saída SARIF
```bash
generateSarif: "1"
```