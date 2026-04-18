---
name: commit 
description: Geração de mensagens de commit padronizadas com emoji e tipo semântico
author: Rodrigo Antunes
version: 1.0.0
---

# Commit

## Objetivo

Gerar mensagens de commit curtas e padronizadas, seguindo a convenção :emoji: tipo: descrição semântica.

---

## Regras obrigatórias

| Regra | Detalhe |
|---|---|
| **Formato** | `:emoji: tipo: descrição` |
| **Comprimento** | Máximo 7 palavras na descrição |
| **Escopo** | Apenas o *que* foi feito |
| **Proibições** | Sem corpo, sem explicações, sem bullets adicionais |

---

## Mapeamento de tipos

| Gitmoji | Tipo | Quando usar |
|---|---|---|
| `:sparkles:` | `feat` | Nova funcionalidade |
| `:bug:` | `fix` | Correção de bug |
| `:recycle:` | `refactor` | Reestruturação sem mudança de comportamento |
| `:lipstick:` | `style` | UI, CSS, formatação visual |
| `:memo:` | `docs` | Documentação |
| `:wrench:` | `chore` | Configuração e tarefas de rotina |
| `:rocket:` | `perf` | Melhoria de performance |
| `:white_check_mark:` | `test` | Testes adicionados ou ajustados |
| `:construction_worker:` | `ci` | Pipelines de CI/CD |
| `:package:` | `build` | Build, bundler ou dependências |
| `:rewind:` | `revert` | Reverter alterações anteriores |
| `:lock:` | `security` | Correções de segurança |
| `:tada:` | `init` | Início de projeto ou módulo |
| `:bookmark:` | `release` | Tag de versão |
| `:construction:` | `wip` | Trabalho em progresso (evitar em main) |

---

## Exemplos de aplicação

### Adicionando uma feature
```
:sparkles: feat: criar componente de busca
```

### Corrigindo um bug
```
:bug: fix: corrigir erro no logout
```

### Ajuste visual
```
:lipstick: style: ajustar padding do card
```

### Refatoração interna
```
:recycle: refactor: extrair lógica de validação
```

### Atualizar dependência
```
:package: build: atualizar react para v19
```

### Configuração de CI
```
:construction_worker: ci: adicionar job de lint no GitHub Actions
```

---

## Anti-padrões — nunca faça isso

```
# Muito longo
:sparkles: feat: criar novo componente de busca que permite filtrar por nome e categoria

# Sem gitmoji
feat: criar componente de busca

# Com corpo/explicação
:bug: fix: corrigir erro no logout

O erro ocorria porque o token não era invalidado corretamente no servidor.
```
