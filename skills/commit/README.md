### Skill que gera mensagens de commit padronizadas com emoji e tipo semântico.

```
🐛 fix: corrigir bug no login

✨ feat: adicionar nova funcionalidade

🛠️ refactor: refatorar código existente

🎨 style: ajustar estilos da aplicação

📚 docs: atualizar documentação

🔧 chore: atualizar dependências

⚡ perf: otimizar performance
```

---

## Instalação

```bash
npx skills add https://github.com/rodrigoant/agent-skills --skill commit
```

Abra o Claude Code e confirme que a skill aparece na lista:

```
/skills
```

---

## Como usar

Após instalar, invoque a skill com o comando `/commit` dentro do Claude Code:

```
/commit
```

O Claude vai analisar as mudanças no repositório atual e gerar uma mensagem de commit no formato:

```
:emoji: tipo: descrição em português
```

### Exemplos de saída

| Situação | Mensagem gerada |
|---|---|
| Nova tela adicionada | `:sparkles: feat: criar tela de cadastro` |
| Bug corrigido | `:bug: fix: corrigir erro no login` |
| Ajuste de CSS | `:lipstick: style: ajustar espaçamento do header` |
| Refatoração | `:recycle: refactor: extrair hook de autenticação` |
| Dependência atualizada | `:package: build: atualizar next para v15` |

---

## Regras da skill

- Máximo de **7 palavras** na descrição
- Sempre em **Português (Brasil)**
- Sem corpo, sem explicações — apenas o *que* foi feito
- Gitmoji obrigatório no início

Veja o arquivo [SKILL.md](SKILL.md) para o mapeamento completo de tipos e anti-padrões.

---

## Requisitos

- [Claude Code](https://claude.ai/code) instalado
- Git inicializado no projeto

---

## Autor

Feito por [Rodrigo Antunes](https://github.com/rodrigoant).
