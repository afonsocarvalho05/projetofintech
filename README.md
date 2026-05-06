# 🤖 Gêmeo Digital — Afonso Carvalho

**Cadeira**: FinTech | **Instituição**: ISCAC  
**Estudante**: Afonso Veloso Cabeço de Oliveira Carvalho  
**Curso**: Ciência de Dados para a Gestão

---

## O que é o Gêmeo Digital?

Um **Gêmeo Digital** é uma representação digital de uma pessoa real — neste caso, do Afonso Carvalho. Trata-se de um agente de IA alimentado por **skills** (ficheiros `.md`) que replicam a sua identidade, valores, personalidade e conhecimento técnico em FinTech.

O agente é capaz de:
- Responder questões **como se fosse o Afonso**, mantendo coerência com os seus valores e personalidade.
- Analisar dilemas éticos e financeiros à luz do seu framework moral.
- Demonstrar conhecimento técnico de FinTech alinhado com o seu perfil académico.

---

## Arquitetura do Agente

```
projeto FinTech/
├── skills/
│   ├── instrucoes_sistema.md   ← System Prompt (orquestrador)
│   ├── persona.md              ← Identidade base
│   ├── etica_moral.md          ← Framework ético e moral
│   ├── psicologica.md          ← Perfil psicológico
│   └── fintech.md              ← Conhecimento FinTech
└── README.md                   ← Este ficheiro
```

---

## Skills

### 🧑 `persona.md` — Identidade Central
Define **quem** é o agente: nome, formação (ISCAC — Ciência de Dados para a Gestão), objetivos de carreira e estilo de comunicação.

### ⚖️ `etica_moral.md` — Framework Ético e Moral
Define o **sistema de valores** do agente:
- Valores: Respeito, Amizade, Ambição
- Posição sobre IA em finanças: ferramenta de apoio, não substituto humano
- Posição sobre criptomoedas: ativo legítimo, regulação necessária (MiCA)
- Inclusão financeira: modelos de volume, não de margem
- Privacidade: RGPD como mínimo, controlo do utilizador como princípio
- ESG: eficiência tecnológica convertida em impacto social real

### 🧠 `psicologica.md` — Perfil Psicológico
Replica os **traços de personalidade**:
- Adjetivos: simpático, compreensivo, altruísta, sincero, realista
- Decisão: analítica, baseada em dados
- Risco: moderado e calculado
- Pressão: compostura, foco no que controla
- Motivação: objetivos claros e crescimento pessoal

### 💳 `fintech.md` — Expertise FinTech
O **conhecimento técnico** do agente:
- Data Science aplicada (Python, ML, credit scoring)
- Open Banking e PSD2
- Criptoativos, DeFi e CBDCs
- RegTech e RGPD
- Inclusão financeira como missão
- Tendências: Embedded Finance, XAI, ESG

### ⚙️ `instrucoes_sistema.md` — System Prompt
O **ficheiro mestre** que integra todos os skills. Define:
- Como o agente se apresenta e comunica
- Quais as regras de comportamento (ética como filtro primário)
- Os limites não negociáveis
- Como cada tipo de pergunta ativa diferentes skills

---

## Como Usar o Agente

1. Abrir uma sessão de chat com um modelo de linguagem (ex: Gemini, ChatGPT, Claude).
2. Copiar o conteúdo de `instrucoes_sistema.md` como **system prompt** (instrução de sistema).
3. Opcionalmente, adicionar os outros skills como contexto adicional.
4. Interagir com o agente — ele responderá como o Gêmeo Digital do Afonso.

---

## Componentes do Projeto

| Componente | Ficheiro | Estado |
|---|---|---|
| Identidade Central | `skills/persona.md` | ✅ Completo |
| Ética e Moral | `skills/etica_moral.md` | ✅ Completo |
| Perfil Psicológico | `skills/psicologica.md` | ✅ Completo |
| Expertise FinTech | `skills/fintech.md` | ✅ Completo |
| System Prompt | `skills/instrucoes_sistema.md` | ✅ Completo |

---

## Exemplos de Interação

**Pergunta**: *"O que achas das criptomoedas?"*  
**Resposta esperada**: Posição favorável, referindo-as como o futuro do sistema financeiro, com defesa de regulação equilibrada (MiCA) e tolerância ao risco moderada.

**Pergunta**: *"Descobriste que um algoritmo da empresa discrimina minorias. O que fazes?"*  
**Resposta esperada**: Denunciar internamente e, se necessário, às autoridades competentes. Nenhuma conivência.

**Pergunta**: *"Preferes trabalhar sozinho ou em equipa?"*  
**Resposta esperada**: Em geral em equipa, mas adaptável ao contexto. Valoriza a diversidade de perspetivas.

---

*Projeto desenvolvido no âmbito da cadeira de FinTech — ISCAC, 2025/2026.*
