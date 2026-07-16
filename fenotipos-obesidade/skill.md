---
name: fenotipos-obesidade
description: Use esta skill sempre que o usuário fornecer uma anamnese, prontuário, relato de caso clínico ou descrição de paciente com obesidade e quiser identificar o(s) fenótipo(s) de obesidade envolvidos (Hungry Brain, Hungry Gut, Emotional Hunger, Slow Burn). Ative quando o usuário mencionar "fenótipo de obesidade", "classificar paciente", "qual fenótipo", "analisar esse caso", colar uma anamnese/prontuário pedindo interpretação, ou pedir ajuda para entender o padrão de fome/saciedade/gasto energético de um paciente. NÃO usar para sugerir medicações ou condutas terapêuticas — o escopo desta skill é exclusivamente diagnóstico/classificatório.
---

# Skill: Classificação de Fenótipos de Obesidade

Baseada em: Acosta A, et al. "Selection of Antiobesity Medications Based on
Phenotypes Enhances Weight Loss: A Pragmatic Trial in an Obesity Clinic."
Obesity (2021) 29, 662-671.

## Escopo

Esta skill **classifica e justifica fenótipos de obesidade** a partir de um
caso clínico. Ela **não** sugere medicações, doses ou condutas terapêuticas —
mesmo que o material de origem mencione fármacos, esse conteúdo foi
deliberadamente suprimido do escopo desta skill.

## Base de conhecimento — os 4 fenótipos

### 1. Hungry Brain (fome central aumentada)
- **Fisiopatologia**: alteração no controle central de saciedade no
  hipotálamo; cérebro precisa de maior ingestão para gerar saciedade.
- **Mecanismos**: menor resposta a GLP-1; menor sinalização de leptina;
  disfunção de neurônios POMC/CART.
- **Resultado clínico**: saciedade tardia, ingestão alimentar grande nas
  refeições.
- **Sinais no relato do paciente**: "só me sinto satisfeito quando como
  muito", grandes porções, dificuldade de parar de comer, fome rápida
  logo após a refeição terminar (por comer pouco antes de saciar).

### 2. Hungry Gut (saciedade curta / pós-prandial)
- **Fisiopatologia**: alteração na saciedade pós-prandial; esvaziamento
  gástrico mais rápido; sinal de saciedade dura pouco tempo.
- **Resultado clínico**: fome retorna rapidamente após a refeição.
- **Sinais no relato do paciente**: "acabei de almoçar e já estou com
  fome", fome recorrente 1–2h após comer, necessidade de beliscar entre
  refeições.

### 3. Emotional Hunger
- **Fisiopatologia**: circuito límbico; eixo cortisol-estresse; amígdala;
  comida como mecanismo de regulação emocional.
- **Resultado clínico**: comportamento alimentar disparado por emoção, não
  por fome fisiológica.
- **Sinais no relato do paciente**: comer por ansiedade/estresse, episódios
  de compulsão, relação clara entre humor e ingestão alimentar.

### 4. Slow Burn (baixo gasto energético)
- **Fisiopatologia**: metabolismo energético reduzido; baixa termogênese;
  adaptação metabólica; menor atividade simpática.
- **Resultado clínico**: gasto energético baixo, facilidade para recuperar
  peso perdido.
- **Sinais no relato do paciente**: "engorda mesmo comendo pouco", perda de
  peso muito lenta apesar de aderência, histórico de múltiplas dietas,
  frequentemente associado a menopausa ou idade >40 anos.

> Fenótipos não são mutuamente excludentes — um paciente pode apresentar
> características de mais de um fenótipo simultaneamente. Isso deve ser
> refletido na classificação.

## Fluxo de trabalho

### Passo 1 — Receber o caso
Se o usuário ainda não colou o material, peça:
> "Cola aqui a anamnese, prontuário ou relato do caso que você quer
> classificar."

### Passo 2 — Extrair evidências textuais
Releia o caso e sublinhe (mentalmente) trechos que se relacionem a padrão
de fome, saciedade, comportamento alimentar, histórico de peso e resposta
a dietas anteriores. Ignore informações irrelevantes à classificação
(comorbidades não relacionadas, exames laboratoriais gerais, etc.), a
menos que tragam pistas sobre gasto energético ou eixo emocional.

### Passo 3 — Classificar
Para cada um dos 4 fenótipos, avalie se há evidência **presente**,
**ausente** ou **não relatada** (dado insuficiente) no caso. Não force
uma classificação — se o relato não permitir avaliar um fenótipo, diga
isso explicitamente.

### Passo 4 — Gerar output estruturado

```
## Classificação de Fenótipo(s) — [nome/identificação do paciente, se houver]

### Fenótipo(s) identificado(s): [ex: Hungry Brain + Emotional Hunger]

---

**Hungry Brain** — [Presente / Ausente / Dado insuficiente]
Justificativa: [trechos/evidências do caso que sustentam a avaliação]

**Hungry Gut** — [Presente / Ausente / Dado insuficiente]
Justificativa: [...]

**Emotional Hunger** — [Presente / Ausente / Dado insuficiente]
Justificativa: [...]

**Slow Burn** — [Presente / Ausente / Dado insuficiente]
Justificativa: [...]

---

### Lacunas na anamnese
[Se houver fenótipos marcados como "dado insuficiente", liste que
perguntas específicas ajudariam a esclarecer — ex: "Perguntar sobre
velocidade de retomada da fome após refeições" para Hungry Gut]
```

### Passo 5 — Iteração
Se o usuário trouxer informação adicional sobre o caso (ex: resposta a
uma pergunta da seção "Lacunas"), atualize apenas a classificação afetada,
sem refazer todo o output.

## Regras
- Nunca sugira medicação, classe farmacológica ou conduta terapêutica,
  mesmo que perguntado — redirecione dizendo que o escopo desta skill é
  só a classificação fenotípica.
- Sempre ancore a justificativa em trechos concretos do caso, não em
  suposições.
- Seja direto: sem preâmbulo, sem repetir o caso inteiro de volta.
