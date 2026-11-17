# Transfusão no Trauma

**Skill para ensino, revisão de protocolos de hemorragia maciça e auditoria transfusional.**

[English](README.en.md) · [Instalação](#instalação) · [Fluxograma](#fluxograma-de-revisão) · [Instruções da skill](SKILL.md)

A skill ajuda a localizar e citar a evidência, identificar o que precisa de validação no serviço e adaptar o produto a três usos.

| Uso | O que a skill prepara |
| --- | --- |
| Ensino | Sínteses, comparações de evidências e simulações com casos fictícios |
| Revisão de protocolo | Comparação entre prática documentada, diretriz e proposta de fluxo |
| Auditoria | Indicadores com população, numerador, denominador, fonte e marcos temporais |

> [!IMPORTANT]
> Esta é uma ferramenta de apoio a ensino e revisão. Na assistência, siga o protocolo vigente e acione as equipes de trauma e hemoterapia conforme o fluxo local.

## Fluxograma de revisão

O algoritmo apresenta as etapas de trabalho da skill, desde a pergunta até a entrega com referências e pendências para validação local.

![Algoritmo de revisão, com caminhos para ensino, revisão de protocolo e auditoria](assets/fluxograma-revisao.svg)

## Instalação

### Agentes com Terminal

Com Node.js e npm disponíveis, execute na pasta do projeto. O instalador apresenta os agentes compatíveis.

```bash
npx skills add jocielle-tech/transfusao-no-trauma --skill transfusao-no-trauma
```

Para instalar a skill para todos os destinos de agentes reconhecidos pela CLI no projeto:

```bash
npx skills add jocielle-tech/transfusao-no-trauma --skill transfusao-no-trauma --agent '*' -y
```

Use `-g` para instalação no escopo do usuário. Para selecionar um agente, substitua `'*'` pelo seu identificador.

| Agente | Identificador para `--agent` |
| --- | --- |
| OpenAI Codex | `codex` |
| Claude Code | `claude-code` |
| Cursor | `cursor` |
| GitHub Copilot | `github-copilot` |
| Gemini CLI | `gemini-cli` |
| Google Antigravity | `antigravity` |
| OpenCode | `opencode` |
| Windsurf | `windsurf` |
| Cline | `cline` |
| Roo Code | `roo` |
| OpenClaw | `openclaw` |

Consulte a [lista atual de agentes](https://github.com/vercel-labs/skills/blob/main/docs/agents.md) e a [referência da CLI](https://github.com/vercel-labs/skills/blob/main/docs/commands.md).

### Instalação manual ou por upload

```bash
git clone https://github.com/jocielle-tech/transfusao-no-trauma.git
```

Copie a pasta `transfusao-no-trauma` para o diretório de skills reconhecido pelo agente. Exemplos no escopo do projeto incluem `.agents/skills/` para Codex e `.claude/skills/` para Claude Code. Para Claude web ou desktop, compacte a pasta da skill em ZIP e envie em **Personalizar → Habilidades** se o recurso estiver disponível na conta. A descoberta e a ativação variam por produto. [Especificação Agent Skills](https://agentskills.io/specification) · [Guia do Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude)

## Exemplos de uso

Inclua o contexto, o público e o formato desejado no pedido. Ao revisar um protocolo ou planejar uma auditoria, forneça os documentos disponíveis e dados desidentificados.

**Preparar uma aula**

> Use a skill transfusao-no-trauma para planejar uma aula de 30 minutos para residentes sobre transfusão pré-hospitalar. Resuma a evidência, cite as fontes e proponha três perguntas para discussão.

**Revisar um protocolo**

> Compare os critérios de ativação e encerramento do protocolo anexado com a diretriz do ACS. Apresente prática documentada, recomendação, proposta e pontos a validar com a hemoterapia. Identifique informações ausentes.

**Planejar uma auditoria**

> Proponha indicadores para o intervalo entre ativação e primeira transfusão e para o destino dos hemocomponentes liberados. Defina população, numerador, denominador, fonte e marcos temporais.

**Criar uma simulação**

> Crie um caso fictício de trauma com hemorragia para discussão em equipe. Inclua informações progressivas, perguntas para os participantes, referências e pontos que dependem do protocolo local.

## Fonte clínica

American College of Surgeons Trauma Quality Programs. *Best Practices Guidelines for Transfusion in Trauma*. Novembro de 2026. Consulte a edição e a paginação aplicáveis antes de usar limiares, metas fisiológicas, doses ou detalhes de compatibilidade. [Índice oficial do ACS](https://www.facs.org/quality-programs/trauma/quality/best-practices-guidelines/) · [PDF de novembro de 2026](https://www.facs.org/media/4y2arm2q/acs-tqp-best-practices-for-transfusion.pdf)
