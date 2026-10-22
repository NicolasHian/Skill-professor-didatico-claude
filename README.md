# 🎓 Professor Didático — Skill para o Claude

Uma skill que transforma o Claude em um **professor extremamente didático e acessível**, capaz de ensinar qualquer assunto — do básico ao avançado — com linguagem simples, exemplos do dia a dia e checagem de entendimento.

> "Se você não consegue explicar de forma simples, você não entendeu bem o suficiente."

## Por que eu criei essa skill

Criei essa skill para estudar a minha área de interesse de um jeito mais eficiente.

Eu uso o Claude como apoio nos estudos. Só que, muitas vezes, as respostas vinham longas demais, cheias de termos técnicos ou com mais informação do que eu precisava naquele momento. Em vez de me ajudar, isso me tirava o foco.

Então montei um "professor" que explica do jeito que eu aprendo melhor:
- **Primeiro a ideia simples**, depois o nome técnico.
- **Um exemplo do dia a dia** para o conceito fazer sentido.
- **Explicações curtas**, uma parte de cada vez.
- **Uma pergunta no final** para eu confirmar que entendi antes de seguir.

Com isso, consigo **aprender mais rápido sem atrapalhar os meus estudos**. O Claude complementa o que eu estou estudando, sem me sobrecarregar nem me desviar do caminho.

Como funcionou bem para mim, resolvi deixar aberto para quem também quiser estudar assim.

## O que é uma skill?

Uma **skill** é um pacote de instruções que você adiciona ao Claude. Ela ensina o Claude a fazer uma tarefa de um jeito específico.

Pensa num professor substituto que recebe um caderno com "como essa turma gosta de aprender". Ele continua sendo o mesmo professor, só que agora segue o caderno. A skill é esse caderno: o Claude continua sendo o Claude, mas passa a explicar do jeito descrito aqui.

## O que ela faz

Quando você quer aprender alguma coisa, o Claude deixa de responder como uma enciclopédia e passa a responder como um professor:

- **Explica com palavras simples** e só depois mostra o nome técnico.
- **Usa exemplos e analogias do dia a dia** para o conceito ficar concreto.
- **Divide assuntos grandes em partes** e ensina uma de cada vez.
- **Termina com uma pergunta ou mini-desafio** para você checar se entendeu.
- **Dá retorno gentil** quando você erra um desafio, mostrando onde o raciocínio desviou.
- **Não te sobrecarrega:** nada de paredes de texto nem de assumir que você já sabe conceitos avançados.

## Como ela funciona

Para explicar um conceito novo, o Claude segue 4 passos:

1. **Técnica Feynman:** começa com "o que é isso?" em uma frase que uma criança de 12 anos entenderia.
2. **Analogia ou exemplo concreto:** o que deixar a ideia mais clara (restaurante, trânsito, velocímetro...).
3. **Três níveis curtos (scaffolding):**
   - A ideia central
   - Como funciona na prática
   - Por que isso importa
4. **Checagem de entendimento:** uma pergunta ou mini-desafio com resposta clara.

Ela tem **dois modos**, e o Claude escolhe sozinho:

| Modo | Quando | Como responde |
|---|---|---|
| **Completo** | Conceito novo ou complexo | Os 4 passos acima |
| **Leve** | Dúvida pontual no meio do estudo | Uma frase, um exemplo e uma pergunta |

**Exemplo de resposta no modo leve:**

> **Você:** O que é memória RAM?
>
> **Claude:** É a memória de curto prazo do computador: guarda o que você está usando **agora** e se apaga quando ele desliga.
>
> 🧩 Pensa na mesa de estudo. O armário (o HD ou SSD) guarda todos os livros; a mesa (a RAM) só tem o que está aberto. Mesa maior = mais coisas abertas ao mesmo tempo.
>
> 👉 Faz sentido, ou quer que eu explique a diferença entre RAM e armazenamento com mais calma?

## Precisa ativar?

**Não precisa ativar a cada conversa.** Depois de instalada, ela funciona sozinha.

O Claude lê a descrição da skill e decide quando usar. Ela entra em ação quando você quer **aprender** algo, por exemplo:
- pede para "explicar" ou "ensinar";
- diz "não entendi";
- pede "me explica como se eu tivesse 12 anos";
- diz que está estudando ou revisando para uma prova.

Ela **não** entra em perguntas rápidas, correção de código ou tarefas práticas. Nesses casos o Claude responde normalmente, sem aula.

Se quiser garantir que ela seja usada, peça direto: *"Use a skill professor-didatico para me explicar…"*.

## Como instalar

### No Claude.ai (site ou app) — a forma mais simples

1. Baixe o arquivo `professor-didatico.zip` na [página de Releases](https://github.com/NicolasHian/professor-didatico/releases/latest).
2. No Claude.ai, abra **Configurações → Capacidades**.
3. Se aparecer a opção **Execução de código e criação de arquivos**, deixe ela ligada. As skills dependem dela.
4. Na seção **Skills**, clique em **Enviar skill** e escolha o `.zip`.
5. Confira se a skill **professor-didatico** aparece na lista e está **ligada**.

> A disponibilidade de skills pode variar conforme o seu plano do Claude.

### No Claude Code — via plugin

Dentro do Claude Code, rode:

```
/plugin marketplace add NicolasHian/professor-didatico
/plugin install professor-didatico@professor-didatico
```

### No Claude Code — manual

Copie a pasta da skill para o seu diretório pessoal de skills:

```bash
git clone https://github.com/NicolasHian/professor-didatico.git
cp -r professor-didatico/skills/professor-didatico ~/.claude/skills/
```

Depois, abra uma nova sessão do Claude Code para ela ser carregada.

### Em um Projeto do Claude ou em outra IA (como instrução de sistema)

Abra [`skills/professor-didatico/SKILL.md`](skills/professor-didatico/SKILL.md), copie tudo **abaixo** do bloco `---` inicial e cole nas instruções de um Projeto no Claude, de um GPT personalizado, de um Gem do Gemini etc.

Nesse formato, o professor fica **sempre ligado** dentro daquele projeto.

## Como usar

Depois de instalada, é só conversar normalmente e pedir para aprender:

- "Me explica o que é uma API"
- "Não entendi derivada, tenho prova semana que vem"
- "Como funciona a inflação?"
- "Me ensina blockchain como se eu tivesse 12 anos"

**Dicas para aproveitar melhor:**
- **Responda os mini-desafios.** É aí que você descobre se entendeu de verdade.
- **Diga o que você já sabe** ("já sei o básico de funções"), para ele não repetir o óbvio.
- **Fale da sua área** ("trabalho com vendas"): ele usa isso nas analogias.
- **Peça outro exemplo** sempre que algo não fizer sentido. Ele explica de um jeito diferente, não só mais devagar.
- **Quer só a resposta?** Diga "só a resposta" e ele vai direto ao ponto.

No Claude Code, você também pode chamar a skill por comando:
- Instalada como plugin: `/professor-didatico:professor-didatico`
- Instalada manualmente: `/professor-didatico`

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
