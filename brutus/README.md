

<p align="center">
<img src="https://www.rodrigoantunes.me/bruto.png" alt="Alt text" title="a title" width="120" />
</p>

<h1 align="center">
brutus
</h1>

**por que usar muitos token quando poucos servir?**

Skill de agente IA que comprime respostas em português do Brasil removendo artigos, preposições e convertendo verbos ao infinitivo — sem perder substância técnica.

---

## 💰 Economia de tokens

| Tarefa | Original | brutus | Redução |
|--------|----------|-------|---------|
| Explicar bug de autenticação | 312 tokens | 89 tokens | **71%** |
| Descrever arquitetura de microsserviços | 480 tokens | 143 tokens | **70%** |
| Instruções de deploy | 260 tokens | 74 tokens | **72%** |
| Revisão de código | 390 tokens | 118 tokens | **70%** |

Média: **~70% redução** sem perda de informação técnica.

---

## Exemplo

**sem brutus** (47 tokens):
> "Claro! O erro que você está vendo ocorre porque a função de autenticação não está verificando corretamente o tempo de expiração do token."

**com brutus** (14 tokens):
> "Bug: função autenticação não verificar expiração token."

---

## Instalar

**Claude Code**

```
/skills install https://github.com/rodrigoant/agent-skills --skill brutus
```

**Cursor / Windsurf / Cline / Copilot**

```bash
npx skills add https://github.com/rodrigoant/agent-skills --skill brutus
```

**Global (todos agentes)**

```bash
npx skills add -g https://github.com/rodrigoant/agent-skills --skill brutus
```

---

## Usar

```
/brutus           → ativa modo full (padrão)
/brutus lite      → sem enchimento, mantém gramática completa
/brutus full      → remove artigos/preposições, verbos no infinitivo
/brutus ultra     → compressão máxima, abreviações, setas pra causalidade

modo normal      → desativar
```

---

## Níveis

| Nível | O que muda | Exemplo |
|-------|-----------|---------|
| **lite** | Remove enchimento, mantém artigos | "Servidor está falhando na validação" |
| **full** | Remove artigos, preposições, infinitivo | "Servidor falhar validação" |
| **ultra** | Abreviações + setas causais | "srv falhar valid → checar schema" |

---

## Regras de compressão

remove → artigos (`o a os as um uma`), preposições de ligação (`da do das dos na no`), enchimento (`apenas realmente basicamente`), formalidades (`claro certamente com prazer`)

transforma → verbos conjugados pro infinitivo, sinonímia curta

preserva → termos técnicos, nomes de variáveis/funções, blocos de código, erros exatos

---

## Segurança automática

brutus desativa sozinho pra: avisos de segurança, ações irreversíveis, sequências onde ordem importa. Retoma depois.

---

## Por que funciona?

Português carrega ~30–40% de tokens estruturais que não transmitem informação nova em contexto técnico. Comprimir output significa:

- menor custo por sessão
- mais espaço no contexto pra código e dados
- respostas mais rápidas
- menos ruído cognitivo

---

## Licença

MIT — [rodrigoant/agent-skills](https://github.com/rodrigoant/agent-skills)