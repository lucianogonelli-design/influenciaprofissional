# Projeto — Skills do Claude

Pasta que guarda as skills (a "fonte") deste projeto.

## Skills disponíveis

| Skill | O que faz |
| --- | --- |
| [`viral-scripts`](./viral-scripts/SKILL.md) | Cria, reescreve e diagnostica roteiros de 15 a 90 s para Reels, Shorts e TikTok em português brasileiro, com foco em retenção e conversão. |

## Como a skill fica ativa

Uma skill do Claude Code é uma pasta com um arquivo `SKILL.md` (com `name` e `description` no topo). O Claude Code procura skills em três lugares:

1. **No projeto:** `.claude/skills/<nome>/SKILL.md` — vale só dentro deste repositório.
2. **No usuário:** `~/.claude/skills/<nome>/SKILL.md` — vale em **todos** os seus projetos.
3. **Em plugins** instalados por um marketplace.

Neste repositório a `viral-scripts` já está instalada em `.claude/skills/viral-scripts/`, então ela ativa sozinha quando você trabalha aqui.

## Instalar no seu Claude pessoal (todos os projetos)

Para usar a skill em qualquer pasta, copie-a para a sua pasta pessoal de skills:

```bash
mkdir -p ~/.claude/skills
cp -r projeto/viral-scripts ~/.claude/skills/
```

Depois é só reabrir o Claude Code. Confirme com `/skills` (a `viral-scripts` deve aparecer na lista) ou peça diretamente: "cria um roteiro viral de 30 s sobre ...".

## Como usar

A skill dispara sozinha quando você pede algo do tipo:

- "Cria um roteiro viral de 30 s sobre ..."
- "Reescreve esse gancho pra prender mais nos primeiros 3 segundos"
- "Analisa a retenção desse roteiro e me diz onde as pessoas largam"
- "Faz um teste A/B de gancho pra esse vídeo"

Ela entrega o roteiro em blocos de tempo, com fala, visual, risco de queda, trava de retenção, loop aberto e uma única CTA.
