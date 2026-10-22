# 🎓 Professor Didático — Skill para o Claude

Uma skill que transforma o Claude em um **professor extremamente didático e acessível**, capaz de ensinar qualquer assunto — do básico ao avançado — com linguagem simples, exemplos do dia a dia e checagem de entendimento.

> "Se você não consegue explicar de forma simples, você não entendeu bem o suficiente."

## O que ela faz

Toda explicação segue o mesmo método:

1. **Técnica Feynman** — começa com "o que é isso?" em uma frase que uma criança de 12 anos entenderia.
2. **Analogia ou exemplo prático** — conceitos abstratos viram situações do cotidiano (restaurante, trânsito, velocímetro...).
3. **Andaime cognitivo (scaffolding)** em 3 níveis:
   - A ideia central
   - Como funciona na prática
   - Por que isso importa
4. **Aprendizagem ativa** — toda explicação termina com uma pergunta ou mini-desafio para checar se você entendeu.

Ela tem dois modos: **completo**, para conceitos novos, e **leve**, com uma frase, um exemplo e uma checagem, para dúvidas pontuais.

E segue regras firmes:
- ✅ Ideia primeiro, nome técnico depois.
- ✅ Frases curtas, parágrafos curtos, formatação limpa.
- ❌ Sem paredes de texto.
- ❌ Sem assumir que você já sabe conceitos avançados.
- ❌ Sem respostas robóticas ou de dicionário.

## Instalação

### Opção 1 — Claude Code (via plugin)

Dentro do Claude Code, rode:

```
/plugin marketplace add NicolasHian/professor-didatico
/plugin install professor-didatico@professor-didatico
```

### Opção 2 — Claude Code (manual)

Copie a pasta da skill para o seu diretório pessoal de skills:

```bash
git clone https://github.com/NicolasHian/professor-didatico.git
cp -r professor-didatico/skills/professor-didatico ~/.claude/skills/
```

### Opção 3 — Claude.ai (site ou app)

1. Baixe o arquivo `professor-didatico.zip` na [página de Releases](https://github.com/NicolasHian/professor-didatico/releases/latest). Se preferir, baixe o repositório e compacte só a pasta `skills/professor-didatico` em um `.zip`.
2. No Claude.ai, vá em **Configurações → Capacidades → Skills**.
3. Clique em **Enviar skill** e selecione o `.zip`.

### Opção 4 — Como System Prompt (qualquer IA)

Abra [`skills/professor-didatico/SKILL.md`](skills/professor-didatico/SKILL.md), copie tudo **abaixo** do bloco `---` inicial e cole como instrução de sistema / instruções personalizadas de um Projeto no Claude, um GPT personalizado, Gemini Gem etc.

## Como usar

Depois de instalada, é só pedir para aprender algo:

- "Me explica o que é uma API"
- "Não entendi derivada, tenho prova semana que vem"
- "Como funciona a inflação?"
- "Me ensina blockchain como se eu tivesse 12 anos"

Ela é ativada quando você quer **aprender** algo. Perguntas rápidas, correção de código e tarefas práticas continuam com respostas normais, sem aula.

No Claude Code você também pode chamar a skill direto:
- Instalada como plugin (opção 1): `/professor-didatico:professor-didatico`
- Instalada manualmente (opção 2): `/professor-didatico`

## Estrutura do repositório

```
professor-didatico/
├── .claude-plugin/
│   ├── marketplace.json     # permite instalar via /plugin marketplace add
│   └── plugin.json          # metadados do plugin
├── skills/
│   └── professor-didatico/
│       └── SKILL.md         # a skill em si (prompt, template e exemplos)
├── LICENSE
└── README.md
```

## Contribuindo

Sugestões de melhores analogias, novos exemplos ou ajustes no método são bem-vindos. Abra uma *issue* ou um *pull request*.

## Licença

[MIT](LICENSE) — use, modifique e compartilhe à vontade.
