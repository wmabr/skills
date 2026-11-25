# Skills da WMA

Skills que os agentes da WMA Personalizados usam para trabalhar de forma organizada e padronizada, seguindo as diretrizes da marca.

## Estrutura

Cada skill fica em sua própria pasta dentro de `skills/`, com um `SKILL.md` e, quando houver, seus arquivos de apoio (imagens, modelos, scripts):

```
skills/
  <nome-da-skill>/
    SKILL.md
    ...arquivos de apoio
```

## Skills

| Skill | Para que serve |
| --- | --- |
| [wma-design-system](skills/wma-design-system/SKILL.md) | Identidade visual: paleta, Nunito Sans, botões, títulos em chips rotacionados, logo, contraste e voz. |
| [wma-imagens](skills/wma-imagens/SKILL.md) | Geração de imagens com IA: pessoas, manequins, regra de crianças, foco no produto e padrões por contexto. |

## Como adicionar uma skill

1. Crie `skills/<nome-da-skill>/SKILL.md` com o frontmatter `name` e `description`.
2. Adicione a skill à tabela acima.
3. Commit em inglês, no padrão Conventional Commits (ex.: `feat(skills): add wma-orcamentos skill`).
