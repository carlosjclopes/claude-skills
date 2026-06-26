# claude-skills

Skills públicas para Claude Code criadas por **Dr. Carlos Lopes** — médico nutrólogo, CEO da MEDX Tecnologia S/A.

Focadas em produtividade médica, gestão de consultório e uso prático de IA na prática clínica.

\---

## Skills disponíveis

|Skill|O que faz|
|-|-|
|[be-human](./be-human/)|Roteiros de Reels médicos para avatar digital com voz clonada (HeyGen + ElevenLabs)|
|[me-frite](./me-frite/)|Validação implacável de ideias — interrogação adaptativa por galhos de decisão|
|[conselho](./conselho/)|Board executivo sênior com 5 personas (CFO, CMO, COO, CTO, Estrategista de Growth)|
|[big4](./big4/)|Análise financeira de consultório com padrão de auditoria Big Four|

\---

## Instalação

### Claude Code

```bash
mkdir -p \~/.claude/skills
git clone https://github.com/drcarlosjclopes/claude-skills.git \~/.claude/skills/claude-skills
```

Ou instalar uma skill específica:

```bash
mkdir -p \~/.claude/skills/be-human
cp \~/.claude/skills/claude-skills/be-human/SKILL.md \~/.claude/skills/be-human/
```

\---

## Uso

### BeHuman

```
/be-human

Tema: \[descreva o tema do seu Reel]
Público: \[médicos ou pacientes]
```

### MeFrite

```
/me-frite

\[descreva o plano ou ideia que quer validar]
```

### Conselho

```
/conselho

\[descreva a decisão que quer analisar]
```

### Big4

```
/big4

\[informe os dados financeiros do seu consultório]
```

\---

## Créditos e inspirações

**be-human** é inspirada na skill [humanizer](https://github.com/blader/humanizer) de [@blader](https://github.com/blader) — que remove padrões de escrita gerada por IA para tornar textos mais naturais e humanos. A BeHuman adapta essa filosofia para roteiros de vídeo médico com avatar digital e voz clonada.

**me-frite** é derivada da skill [grill-me](https://github.com/anthropics/claude-code) incluída no Claude Code — que interroga planos e ideias um galho por vez até mapear todas as premissas e decisões. A MeFrite adiciona uma fase adaptativa de captação de premissas antes do fluxo principal, além de adaptações para o contexto médico-empreendedor.

\---

## Sobre o autor

**Dr. Carlos Lopes** é médico nutrólogo com foco em obesidade e CEO da [MEDX](https://medx.med.br), plataforma SaaS para médicos com mais de 20 anos de mercado.

Cria conteúdo sobre IA aplicada à prática médica em [@drcarlosjclopes](https://instagram.com/drcarlosjclopes).

\---

## Licença

MIT

