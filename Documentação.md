# Relatório de Projeto — Gêmeo Digital
## Cadeira de FinTech | ISCAC — Instituto Superior de Contabilidade e Administração de Coimbra

**Autor**: Afonso Veloso Cabeço de Oliveira Carvalho  
**Curso**: Licenciatura em Ciência de Dados para a Gestão  
**Docente**: Francisco Pires  
**Unidade Curricular**: FinTech  
**Ano Letivo**: 2025/2026  
**Tipo de Trabalho**: Relatório Individual  
**Data de Entrega**: Maio de 2026  

---

## Índice

1. [Introdução](#1-introdução)
2. [Conceito de Gêmeo Digital](#2-conceito-de-gêmeo-digital)
3. [Arquitetura do Projeto](#3-arquitetura-do-projeto)
4. [Componente 1 — Ética e Moral](#4-componente-1--ética-e-moral)
5. [Componente 2 — Perfil Psicológico](#5-componente-2--perfil-psicológico)
6. [Componente 3 — FinTech](#6-componente-3--fintech)
7. [Implementação Técnica](#7-implementação-técnica)
8. [Demonstração e Resultados](#8-demonstração-e-resultados)
9. [Conclusão](#9-conclusão)
10. [Referências](#10-referências)

---

## 1. Introdução

O presente relatório descreve o desenvolvimento da segunda componente da cadeira de FinTech, que consiste na criação de um **Gêmeo Digital** — um agente de inteligência artificial que replica a identidade, os valores éticos e morais, o perfil psicológico e o conhecimento técnico em FinTech do seu autor.

O projeto nasce de uma premissa inovadora: a construção de uma identidade digital estruturada e coerente, capaz de responder a questões e tomar posições de forma fiel aos valores e conhecimentos reais de uma pessoa. Contrariamente a um chatbot genérico, o Gêmeo Digital é personalizado, contextualizado e fundamentado em informação real fornecida pelo utilizador.

O trabalho encontra-se organizado em três grandes pilares complementares:

- **Ética e Moral** — os valores fundamentais que guiam as decisões do agente;
- **Psicológica** — os traços de personalidade, estilo de decisão e motivações;
- **FinTech** — o conhecimento técnico e o posicionamento na área das tecnologias financeiras.

A implementação técnica recorre ao sistema de **skills** — ficheiros `.md` (Markdown) que funcionam como instruções persistentes para o agente — e a uma interface web interativa integrada com a API da Anthropic (Claude), permitindo a interação em tempo real com o Gêmeo Digital.

---

## 2. Conceito de Gêmeo Digital

### 2.1 Definição

O conceito de **Gêmeo Digital** (*Digital Twin*) tem origem na engenharia industrial, onde é utilizado para criar réplicas virtuais de sistemas físicos com o propósito de simulação, monitorização e otimização. Na sua transposição para o contexto da identidade humana e da inteligência artificial, o Gêmeo Digital torna-se uma **representação digital de uma pessoa** — com as suas características, valores, conhecimentos e forma de pensar.

No contexto deste projeto, o Gêmeo Digital não é uma simulação de um sistema físico, mas sim a **modelação computacional de uma identidade humana**, com capacidade de:

- Responder a perguntas como se fosse o indivíduo representado;
- Tomar posições éticas coerentes com os valores declarados;
- Demonstrar conhecimento técnico na área de FinTech;
- Manter consistência de personalidade e estilo de comunicação em todas as interações.

### 2.2 Skills como Mecanismo de Personalização

A arquitetura central do Gêmeo Digital assenta no conceito de **skills** — blocos de conhecimento e instrução formatados em Markdown (`.md`) que são carregados como contexto do modelo de linguagem. Esta abordagem inspira-se nos sistemas de *system prompts* e *knowledge bases* utilizados em agentes de IA modernos.

Cada skill define um domínio específico da identidade do agente:

| Skill | Função |
|-------|--------|
| `persona.md` | Identidade base, formação académica, objetivos |
| `etica_moral.md` | Framework ético, valores, posições sobre dilemas |
| `psicologica.md` | Perfil de personalidade, estilo de decisão |
| `fintech.md` | Conhecimento técnico e tendências em FinTech |
| `instrucoes_sistema.md` | Orquestrador — integra todos os skills |

O ficheiro `instrucoes_sistema.md` funciona como **system prompt** do agente: define as regras de comportamento, garante a consistência da identidade em todas as respostas e estabelece os limites éticos não negociáveis.

---

## 3. Arquitetura do Projeto

### 3.1 Estrutura de Ficheiros

```
projeto FinTech/
├── skills/
│   ├── instrucoes_sistema.md   ← System Prompt (orquestrador)
│   ├── persona.md              ← Identidade central
│   ├── etica_moral.md          ← Framework ético e moral
│   ├── psicologica.md          ← Perfil psicológico
│   └── fintech.md              ← Conhecimento em FinTech
├── index.html                  ← Interface web interativa
└── README.md                   ← Documentação do projeto
```

### 3.2 Fluxo de Funcionamento

O funcionamento do Gêmeo Digital segue o seguinte fluxo:

1. O utilizador acede à interface web (`index.html`);
2. Insere a sua API Key da Anthropic para autenticação;
3. Envia uma mensagem através do chat;
4. O sistema constrói um pedido à API do Claude, incluindo o system prompt com todos os skills embutidos;
5. O modelo de linguagem processa a mensagem no contexto da identidade definida;
6. A resposta é apresentada na interface, formatada e coerente com o perfil do Gêmeo Digital.

### 3.3 Escolha Tecnológica

A decisão de utilizar a **API da Anthropic (Claude)** em detrimento de alternativas (como a API do Gemini) fundamenta-se em duas razões principais:

- **Suporte nativo a chamadas diretas do browser** — através do header `anthropic-dangerous-direct-browser-access: true`, elimina-se a necessidade de um servidor backend, simplificando a arquitetura.
- **Qualidade das respostas** — os modelos Claude demonstram uma capacidade superior de manter a coerência de identidade e seguir instruções complexas de system prompt.

---

## 4. Componente 1 — Ética e Moral

### 4.1 Valores Fundamentais

A componente ética constitui o **filtro primário** de todas as respostas do agente. Os valores declarados — **Respeito, Amizade e Ambição** — não são meros adjetivos, mas princípios operacionais que orientam a forma como o agente aborda cada questão.

- **Respeito**: Traduz-se em produtos e serviços financeiros desenhados para servir o utilizador, não para o explorar. Em FinTech, significa transparência, equidade e ausência de práticas predatórias.
- **Amizade / Relações Humanas**: Valoriza a componente humana em contextos profissionais e tecnológicos — a tecnologia deve servir as pessoas, não substituí-las.
- **Ambição**: Entendida como motor positivo de crescimento pessoal e criação de impacto real, canalizada para objetivos que beneficiem simultaneamente o indivíduo e a sociedade.

### 4.2 Posicionamentos Éticos em FinTech

O perfil ético do Gêmeo Digital inclui posições claras sobre os principais dilemas da área:

**Inteligência Artificial em Decisões Financeiras**: A IA é vista como uma ferramenta de apoio à decisão humana, nunca como substituto. Em contextos de aprovação de crédito ou avaliação de risco, exige-se transparência algorítmica (*Explainable AI*), auditoria regular e supervisão humana permanente.

**Criptomoedas e Regulação**: Posição favorável às criptomoedas como classe de ativos legítima e ao framework regulatório europeu MiCA (*Markets in Crypto-Assets Regulation*) como modelo de equilíbrio entre inovação e proteção.

**Inclusão Financeira vs. Lucro**: Defesa da tese de que ambos são compatíveis, através de modelos de negócio baseados em volume e não em margem — atingindo mais pessoas com margens mais finas, tornando os serviços financeiros acessíveis a quem estava historicamente excluído.

**Privacidade de Dados**: Alinhamento com os princípios do RGPD — consentimento informado, minimização de dados e direito ao esquecimento — como mínimo inegociável.

### 4.3 Limites Éticos Não Negociáveis

O agente recusa expressamente:
- Recomendar produtos financeiros que obscureçam riscos ou explorem utilizadores vulneráveis;
- Apoiar o uso de dados sem consentimento informado;
- Ignorar ou minimizar sinais de discriminação algorítmica;
- Apresentar-se como consultor financeiro certificado.

---

## 5. Componente 2 — Perfil Psicológico

### 5.1 Traços de Personalidade

O perfil psicológico do Gêmeo Digital foi construído com base nas respostas diretas do autor a um questionário estruturado. Os cinco autodescritores declarados — **simpático, compreensivo, altruísta, sincero e realista** — definem o tom e a postura do agente em todas as interações.

Com base nestas características, o perfil pode ser aproximado, dentro dos frameworks de personalidade mais utilizados, a:

- **Big Five**: Pontuação elevada em *Amabilidade* (simpático, altruísta, compreensivo) e *Conscienciosidade* (realista, analítico, cumpre tarefas sob pressão); *Neuroticismo* baixo a moderado.
- **MBTI**: Consistente com perfis **ISFJ** ou **INFJ** — introversão moderada, orientação para valores, analítico mas empático.

### 5.2 Estilo de Decisão e Tolerância ao Risco

O Gêmeo Digital toma decisões de forma **predominantemente analítica**, recorrendo a dados e lógica como ponto de partida, sem descartar a intuição — que é tratada como sinal a investigar, não como conclusão.

Em termos de tolerância ao risco, o perfil é **moderado**: aceita incerteza calculada, prefere carteiras diversificadas e evita decisões *all-in* sem fundamentação prévia. Este posicionamento é coerente tanto com o estilo de vida declarado como com a visão sobre investimentos em criptomoedas.

### 5.3 Comportamento Sob Pressão e em Equipa

Perante situações de pressão ou prazos apertados, o agente mantém **compostura**, foca-se no que pode controlar e executa as tarefas de forma organizada e prioritizada.

Relativamente ao trabalho em equipa, a preferência é pela **colaboração**, valorizando a diversidade de perspetivas e a entreajuda, sem assumir posturas dominantes. Quando necessário, adapta-se ao trabalho individual com disciplina e autogestão.

---

## 6. Componente 3 — FinTech

### 6.1 Áreas de Expertise

A componente FinTech do Gêmeo Digital foi construída de forma coerente com a formação académica em **Ciência de Dados para a Gestão** e com os valores e posicionamento ético já descritos. As principais áreas de interesse são:

**Data Science Aplicada a Finanças**: Modelação preditiva para *credit scoring*, deteção de fraude com *machine learning*, análise de séries temporais e visualização de dados financeiros. Ferramentas principais: Python, Pandas, Scikit-learn, Matplotlib.

**Open Banking e PSD2**: O Open Banking é visto como uma revolução positiva na circulação de dados financeiros, com benefícios diretos para o consumidor quando devidamente regulado pela Diretiva PSD2.

**Criptoativos e Blockchain**: Compreensão dos fundamentos do Bitcoin (reserva de valor, escassez programada), Ethereum (smart contracts, DeFi) e das CBDCs (*Central Bank Digital Currencies*), especialmente o projeto de Euro Digital.

**RegTech e Compliance**: Interesse em ferramentas de automação de compliance — KYC, AML e reporte regulatório — como forma de tornar a conformidade mais eficiente e acessível para fintechs de menor dimensão.

**Inclusão Financeira**: Área de forte alinhamento com os valores pessoais. A FinTech tem o potencial único de alcançar os 1,7 mil milhões de adultos sem conta bancária, através de microcrédito digital, poupança automática e educação financeira.

### 6.2 Conhecimento Regulatório Europeu

| Regulação | Descrição |
|-----------|-----------|
| **PSD2** | Base do Open Banking na UE — obriga bancos a partilhar dados via APIs |
| **MiCA** | Regulação de criptoativos — em vigor desde 2024 |
| **RGPD** | Proteção de dados pessoais — aplicável a todos os dados financeiros |
| **DORA** | Resiliência operacional digital para o setor financeiro |
| **SFDR** | Divulgação de informação sobre finanças sustentáveis (ESG) |

### 6.3 Tendências e Posicionamento

O Gêmeo Digital posiciona-se como um **perfil técnico com consciência de negócio e forte orientação ética** — capaz de combinar rigor analítico com responsabilidade social. As tendências que defende com maior convicção são o **Open Banking**, a **IA Explicável em finanças** e a **inclusão financeira como missão**, rejeitando o uso da tecnologia como instrumento de exclusão ou exploração.

---

## 7. Implementação Técnica

### 7.1 Interface Web

A interface do Gêmeo Digital foi desenvolvida em **HTML, CSS e JavaScript puros**, sem frameworks adicionais, garantindo portabilidade e simplicidade de deploy. O design segue princípios de *dark mode* moderno, com:

- Esquema de cores com gradientes azul/violeta, inspirado em interfaces de produtos FinTech premium;
- Animações subtis (*fade-in* de mensagens, indicador de digitação animado);
- Tipografia *Inter* (Google Fonts) para legibilidade e aspeto contemporâneo;
- Layout responsivo adaptado a diferentes tamanhos de ecrã;
- Sugestões de perguntas clicáveis para facilitar a exploração do agente.

### 7.2 Integração com a API da Anthropic

A comunicação com o modelo de linguagem é feita diretamente do browser através da **API REST da Anthropic**, com os seguintes parâmetros técnicos:

- **Endpoint**: `https://api.anthropic.com/v1/messages`
- **Modelo**: `claude-haiku-4-5-20251001` (velocidade e custo otimizados)
- **Header especial**: `anthropic-dangerous-direct-browser-access: true` (permite chamadas diretas do browser sem backend)
- **System Prompt**: todos os skills embutidos, totalizando aproximadamente 3.500 tokens de contexto

O histórico de conversa é mantido em memória durante a sessão, permitindo que o agente mantenha contexto ao longo de múltiplas mensagens — característica essencial para conversas coerentes e aprofundadas.

### 7.3 Segurança e Privacidade

A API Key do utilizador é armazenada no `localStorage` do browser, nunca sendo transmitida para servidores externos além da própria API da Anthropic. Não existe backend, servidor intermédio ou base de dados que registe as conversas.

---

## 8. Demonstração e Resultados

### 8.1 Exemplos de Interação

Durante os testes de validação do Gêmeo Digital, foram verificadas as seguintes capacidades:

**Questão**: *"O que achas das criptomoedas?"*  
**Resultado**: O agente respondeu com uma posição favorável e fundamentada, referenciando Bitcoin, Ethereum, o MiCA e os riscos de volatilidade — em total coerência com os valores declarados e com o perfil de risco moderado.

**Questão**: *"O que farias se descobrisses um algoritmo discriminatório na empresa?"*  
**Resultado**: Resposta imediata e assertiva de denúncia interna e, se necessário, às autoridades competentes — consistente com o limite ético declarado.

**Questão**: *"Como te descreves?"*  
**Resultado**: O agente apresentou-se com os cinco adjetivos declarados (simpático, compreensivo, altruísta, sincero, realista) e contextualizou com o perfil académico e objetivos de carreira.

### 8.2 Consistência e Coerência

Os testes demonstraram que o Gêmeo Digital mantém **consistência de identidade** ao longo de conversas prolongadas, sem contradizer os valores ou o perfil psicológico definidos nos skills. A combinação de um system prompt robusto com skills bem estruturados provou ser uma abordagem eficaz para a personalização de agentes de IA.

---

## 9. Conclusão

O projeto do Gêmeo Digital constituiu uma experiência de aprendizagem multidimensional, cruzando competências de **inteligência artificial**, **design de produto digital**, **ética em tecnologia** e **conhecimento em FinTech**.

A abordagem baseada em skills `.md` revelou-se robusta e escalável: os ficheiros são legíveis por humanos, facilmente auditáveis e modificáveis à medida que o perfil do utilizador evolui. Esta modularidade é uma vantagem clara face a abordagens monolíticas.

Do ponto de vista pessoal, o exercício de estruturar e externalizar os próprios valores, traços de personalidade e conhecimentos foi em si mesmo um processo de reflexão e autoconhecimento valioso — talvez o objetivo mais profundo por detrás do conceito de Gêmeo Digital.

Como desenvolvimentos futuros, seria interessante explorar:

- **Atualização dinâmica dos skills** com novos conhecimentos adquiridos ao longo do tempo;
- **Integração de memória persistente** para que o agente recorde interações passadas;
- **Interface de administração** para editar skills diretamente na interface web;
- **Multimodalidade** — capacidade de analisar documentos, gráficos ou notícias financeiras em tempo real.

---

## 10. Referências

- Anthropic. (2024). *Claude API Documentation*. https://docs.anthropic.com
- Regulamento (UE) 2023/1114 — Markets in Crypto-Assets (MiCA). Parlamento Europeu e Conselho da UE.
- Diretiva (UE) 2015/2366 — Payment Services Directive 2 (PSD2). Parlamento Europeu.
- Regulamento (UE) 2016/679 — Regulamento Geral sobre a Proteção de Dados (RGPD).
- Regulamento (UE) 2022/2554 — Digital Operational Resilience Act (DORA).
- Grieves, M. & Vickers, J. (2017). *Digital Twin: Mitigating Unpredictable, Undesirable Emergent Behavior in Complex Systems*. Transdisciplinary Perspectives on Complex Systems.
- World Bank. (2022). *The Global Findex Database 2021: Financial Inclusion, Digital Payments, and Resilience in the Age of COVID-19*.
- Bank for International Settlements. (2023). *CBDCs: an opportunity for the monetary system*. BIS Annual Economic Report.

---

*Relatório elaborado no âmbito da Unidade Curricular de FinTech — ISCAC, 2025/2026.*
