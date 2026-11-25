---
name: "wma-design-system"
description: "Identidade visual da WMA Personalizados: paleta, Nunito Sans, botões, títulos em chips rotacionados, logo, contraste e voz. Use em qualquer arte, página, e-mail, PDF, slide ou post da WMA."
---

# Design system da WMA Personalizados

Use esta skill sempre que criar material visual para a WMA (confecção de uniformes escolares e profissionais, Aracaju-SE): site, landing pages, e-mails, PDFs, slides, posts, stories, banners, flyers, catálogos.

## 1. Personalidade (o que decide os casos não previstos)

A própria página `/marca` define: *"uma marca bem humorada e divertida que foca sempre na qualidade do que produzimos"*.

- **Divertida, mas séria no acabamento.** Cores vivas, formas arredondadas, leve inclinação nos títulos. Nunca bagunçado: poucas cores por peça, bom contraste, muito respiro.
- **Tátil.** Botões e cards têm a borda inferior mais grossa (efeito de "botão de verdade"), como costura/etiqueta.
- **Roxo é a marca; as outras cores são tempero.** Lima, vermelho e amarelo aparecem quase só dentro dos chips de título.
- **Português do Brasil, informal, caloroso.**

## 2. Cores

### Marca (roxos)
| Token | Hex | Nome na `/marca` | Uso |
|---|---|---|---|
| `wma-lighter` | `#EED9FF` | Lavanda | fundos de seção (muitas vezes a 50%), padrão de tracinhos, texto sobre roxo-escuro |
| `wma-light` | `#E7C9FF` | Lavanda pálido | chips, pills de destaque, balões, seleção de texto |
| `wma-mid` | `#932CE3` | Roxo | botão principal, links, ícones de ação, sublinhado ondulado |
| `wma-low` | `#3A1B52` | American Purple | **texto principal**, bordas, chip escuro |
| `wma-black` | `#333333` | Carvão escuro | texto de leitura longa, formulários, documentos legais |

### Neutros
`#FFFFFF` fundo padrão · `#F4F4F5` (zinc-100) seção alternada · `#FAFAFA` (zinc-50) FAQ/painéis · `#E4E4E7` (zinc-200) bordas/divisórias · `#71717B` (zinc-500) subtítulos (só ≥16px) · `#09090B` (zinc-950) rodapé escuro e texto neutro de títulos de páginas internas.

### Cores dos chips (exclusivas de título)
| Cor | Hex |
|---|---|
| Lima | `#D8F999` (fundo) |
| Azul | `#155DFC` display / `#193CB8` texto menor |
| Vermelho | `#E7000B` |
| Amarelo | `#FDC700` |

### Semânticas
Perigo: `#CC2937` (base), `#F75A68` (claro), `#2D090C` (escuro/borda). Azul de selo/"Fabricante autorizado": `#155DFC`. Verde só para WhatsApp: `#00C950`.

### Trio de cards coloridos (fundo / borda / texto)
- Amarelo: `#FEFCE8` / `#A65F00` / `#432004`
- Verde: `#F0FDF4` / `#008236` / `#032E15`
- Roxo: `#FAF5FF` / `#8200DB` / `#3C0366`

## 3. Contraste (WCAG 2.x, calculado)

**Pares aprovados para qualquer tamanho de texto**
- `#3A1B52` sobre `#FFFFFF` 14,4:1 · sobre `#EED9FF` 11,0:1 · sobre `#E7C9FF` 9,7:1 · sobre `#D8F999` 12,3:1 · sobre `#FDC700` 9,2:1 (usar o amarelo como fundo com texto roxo-escuro é seguro)
- `#E7C9FF` ou `#EED9FF` sobre `#3A1B52` 9,7:1 / 11,0:1
- `#333333` sobre branco 12,6:1
- `#FFFFFF` sobre `#932CE3` 5,7:1 (botão principal) · sobre `#CC2937` 5,3:1 · sobre `#09090B` 19,9:1
- `#932CE3` sobre branco 5,7:1 e sobre `#F4F4F5` 5,2:1 (links)
- `#193CB8` sobre `#D8F999` 7,5:1 · `#1447E6` sobre `#D8F999` 5,8:1
- Cards coloridos (texto 950 sobre fundo 50) ≈ 14:1

**Restritos (só texto grande: ≥24px bold, ou ≥18,66px bold)**
- `#155DFC` sobre `#D8F999`: 4,5:1. No limite; use só em título de exibição ≥48px. Abaixo disso, `#193CB8`.
- `#FDC700` sobre `#E7000B`: 3,0:1. Só no chip vermelho, palavra curta em exibição. Nunca em texto corrido.
- `#932CE3` sobre `#EED9FF`: 4,3:1. Não usar em texto pequeno sobre lavanda.

**Proibidos**
- `#FDC700` sobre branco 1,6:1 · `#932CE3` sobre `#3A1B52` 2,5:1 · branco sobre verde WhatsApp `#00C950` 2,2:1 (permitido apenas como ícone de marca do WhatsApp, nunca com texto).
- Texto cinza claro sobre lavanda; texto sobre foto sem overlay/chip.

Regra prática: em dúvida, **roxo-escuro `#3A1B52` sobre claro, ou lavanda sobre roxo-escuro**. Rode um cálculo de contraste antes de introduzir qualquer par novo.

## 4. Tipografia

- **Família única: Nunito Sans** (Google Fonts). Fallback: `system-ui, Arial, sans-serif`. Em e-mail: `Nunito, Arial, Helvetica, sans-serif`. Nunca misturar outra família.
- Pesos: **500** corpo · **600** botões e rótulos · **700** títulos de seção/cards · **900 (Black)** chips, números de destaque ("28+"), chamadas curtas.
- Escala (web): h1 interno 24→36px bold · h2 de seção 30–36px bold (line-height normal) · h3 de card 20px bold · corpo 16–18px · lead 24px · subtítulo 18px `#71717B` · botão 14px.
- Chips: **MAIÚSCULAS**, peso 900, `line-height:1`, 30→60px conforme a seção.
- Antialiased; `selection` = fundo `#E7C9FF` a 75% com texto `#333333`.
- Ênfase dentro de título: ou **pill** (seção 7), ou `text-decoration: underline wavy #932CE3` ("Uniformes <u>Profissionais</u>"). Uma ênfase por título.

## 5. Assinatura visual: título em chips rotacionados

O título de maior impacto quebra a frase em palavras, cada uma num **bloco colorido arredondado** inclinado, empilhados e encostados (levemente sobrepostos). Exemplo canônico ("PERSONALIZE / DO SEU JEITO") sobre o padrão de tracinhos:

| Chip | Fundo | Texto | Rotação |
|---|---|---|---|
| Lima | `#D8F999` | `#155DFC` | -2° |
| Escuro | `#3A1B52` | `#E7C9FF` | +2° |
| Vermelho | `#E7000B` | `#FDC700` | -1° |
| Lavanda | `#E7C9FF` | `#3A1B52` | +1° |

Par "uniformes / escolares": lima (-2°) + lavanda (+1°). Receita:

```css
.chips{font-family:'Nunito Sans';font-weight:900;text-transform:uppercase;font-size:48px;line-height:1}
.chip{display:block;width:min-content;padding:.25em;border-radius:.46em}   /* site: p-3 (12px) e rounded-3xl (22px) fixos */
.chips .row{display:flex} .chips .row .chip+.chip{margin-left:-4px}      /* encostados */
.chip.lime{color:#155DFC;background:#D8F999;transform:rotate(-2deg)}
.chip.dark{color:#E7C9FF;background:#3A1B52;transform:rotate(2deg)}
.chip.red {color:#FDC700;background:#E7000B;transform:rotate(-1deg)}
.chip.lav {color:#3A1B52;background:#E7C9FF;transform:rotate(1deg)}
```

**Regras**
- Medidas para artes sem CSS (Canva, SVG, imagem): padding ≈ 0,25 × tamanho da fonte; raio ≈ 0,45 × tamanho da fonte; altura do bloco ≈ 1,5 × tamanho da fonte.
- Uma palavra (ou duas curtas) por chip; 2 a 4 chips por título. Rotações alternando sinal, **máximo ±3°** (±1° a ±2° é o padrão).
- Sinais de cor alternados: nunca dois chips vizinhos da mesma cor. Sempre da paleta de chips; a combinação texto/fundo é fixa (não trocar pares).
- Para chips pequenos (<32px) prefira lima com `#193CB8` ou lavanda/roxo-escuro; o vermelho/amarelo só em exibição.
- Use no máximo **um título em chips por tela/peça**. O resto do texto é Nunito normal.

## 6. Botões

Botão "tátil": **1px nas laterais/topo e 4px na borda inferior**, raio 10px, 14px semibold, altura 36px, padding horizontal 24px.

| Variante | Texto | Fundo | Borda |
|---|---|---|---|
| Principal (padrão) | `#FFFFFF` | `#932CE3` | `#3A1B52` |
| Secundário | `#3A1B52` | `#FFFFFF` | `#3A1B52` |
| Outline | `#3A1B52` | `#FFFFFF` | `rgba(58,27,82,.15)` |
| Ghost | `#3A1B52` | `#FFFFFF` | branco; borda aparece no hover |
| Destrutivo | `#FFFFFF` | `#CC2937` | `#2D090C` |
| Link | `#932CE3` | transparente | sublinha no hover (offset 4px) |

Tamanhos: xs 28px (12px, px 16) · sm 32px · padrão 36px · lg 40px · ícone 36px quadrado.
Estados: hover `opacity:.75` com 300ms · pressionado `translateY(1px)` · desabilitado `opacity:.7` · foco: anel de 3px lavanda/roxo a 50%.

```css
.btn{display:inline-flex;align-items:center;justify-content:center;height:36px;padding:0 24px;border:1px solid;border-bottom-width:4px;border-radius:10px;font:600 14px 'Nunito Sans';transition:all .3s}
.btn-primary{color:#fff;background:#932CE3;border-color:#3A1B52}
```

- **Um botão principal por área.** CTA padrão: "Faça um orçamento". Ações secundárias como link de corpo.
- **Link de corpo (CTA leve):** texto herdado + ícone Phosphor `CaretCircleRight` (bold, 24px) à direita; no hover sublinha e o ícone gira -45°. Ex.: "Compre agora ➜".
- Botão do WhatsApp: círculo `#00C950`, ícone branco 40px, fixo canto inferior direito.
- Em mídias estáticas (post, banner) desenhe o botão com a mesma borda inferior grossa; ele precisa parecer clicável.

## 7. Cards, pills, selos e formas

- **Raios:** 6 / 8 / 10 (botões, inputs) / 14 (cards) / 18 / 22px (chips). Pilhas ou balões podem usar `rounded-full` em um dos lados.
- **Card tátil:** borda 2px (topo/laterais) + 4px embaixo, raio 14px, fundo claro tintado + borda e texto do mesmo matiz (trio da seção 2), ícone Phosphor **duotone 36px** no topo, título 20px bold, texto 18px. Largura 320px.
- **Pill de destaque inline** (dentro do título): fundo `#E7C9FF`, borda `#3A1B52` 1px (topo/laterais) + 2px (embaixo), raio 10px, padding 4px. Ex.: "…experiência para [você!!!]".
- **Card empilhado ("folha atrás"):** card branco com borda 2px `#3A1B52`, mais uma cópia vazia deslocada 16px para baixo/direita atrás dele. Usado para prints de redes sociais/depoimentos.
- **Balão de depoimento:** fundo `#E7C9FF`, borda branca 8px, ponta esquerda totalmente arredondada, sombra grande, rotação -6° (única exceção ao limite de ±3°).
- **Selo:** fundo branco, topo com raio 6px e base totalmente redonda, sombra média, ícone `SealCheck` bold 64px e texto Black em azul `#155DFC` ("Fabricante autorizado").
- **Estatísticas:** número Black 30–36px + legenda 16px, separadas do conteúdo por divisor tracejado 2px `#3A1B52`. Ex.: "28+ escolas".
- **Rodapé escuro:** `#09090B`, raio 24px, texto branco, margem lateral (não encosta nas bordas), slogan 24px bold.

## 8. Fundos e ritmo de seção

- Alterne fundos entre seções: branco → lavanda `#EED9FF` a 50% → `#F4F4F5` → branco → padrão de tracinhos. Espaço vertical generoso (96–160px entre blocos). Largura máxima de conteúdo ≈ 1024px; texto largo centralizado ou alinhado à esquerda em colunas de 384px.
- **Padrão de tracinhos** (fundo da chamada principal):

```css
.pattern{background-color:#fff;background-size:1em 1em;background-image:
 linear-gradient(25deg,#fff 40%,transparent 41%,transparent 59%,#fff 60%),
 linear-gradient(90deg,transparent 45%,#EED9FF 45%,#EED9FF 55%,transparent 55%,transparent 20%,#EED9FF 20%,#EED9FF 30%,transparent 30%)}
```
- Divisórias: tracejado 2px `#3A1B52`. Ilustrações vetoriais (pessoas, foguete) ficam sobre bloco lavanda `#EED9FF`.

## 9. Logo

Arquivos oficiais (também em `https://wmapersonalizados.com.br/logo/…`, ou `public/logo/` no repo): `logo.svg|png` (colorido: `#333333` + `#932CE3`), `logo-preto`, `logo-branco`; e o **logotipo** (versão compacta, proporção ≈ 42×78) nas mesmas três cores.

- **Nunca** editar, distorcer, recolorir ou reconfigurar. Use a variante certa para o fundo: colorido em claro, branco em escuro/roxo, preto em impressão P&B.
- O **logotipo** compacto só quando a marca já estiver claramente visível no resto da peça; na dúvida, use o logo completo.
- Proporção do logo completo ≈ 160×83 (1,93:1); no site aparece entre 128 e 160px de largura. Evite menos de 128px em tela.
- Margem de respiro: ao menos metade da altura do logo em todos os lados (convenção nossa, não oficial).
- Não coloque o logo colorido sobre o roxo `#932CE3` ou sobre fotos; use o branco.

## 10. Ícones, ilustração e emoji

- **Ícones:** Phosphor Icons. `duotone` 36px em cards de benefício; `bold` em selos e CTAs; `fill` em corações/marcadores. Cor = `currentColor`.
- **Emoji faz parte da voz:** 📍 em "Onde nos encontrar", 💜 no slogan, 🇧🇷 no copyright. Emojis 3D (foguete, alvo, troféu) em 64px acompanhando listas de 3 benefícios. Use poucos e coerentes (um por título/bloco).
- **Ilustrações:** vetoriais planas em tons de roxo sobre lavanda. Fotos: produto real (uniformes, bordado, silkscreen) em `webp`, sem filtros.

## 11. Voz e tom

- Português do Brasil, 2ª pessoa informal ("você", "a gente"); frases curtas e diretas; exclamação com moderação ("você!!!" é permitido como brincadeira em destaque).
- Frases-modelo: "Proporcionando a melhor experiência para você!!!" · "Estamos aqui para ajudar!" · "Compre agora" · "Faça um orçamento" · **slogan: "Vestir a sua profissão é o nosso trabalho 💜"**.
- Benefícios sempre concretos: entrega em 48h em Aracaju, entrega para todo o Brasil, pedido pelo WhatsApp, equipe especialista, "28+ escolas / 150+ uniformes / 3 estados" (confirmar números atuais antes de usar).
- CTA principal de venda: WhatsApp (escolares) ou orçamento (profissionais).

## 12. Receitas por mídia

**Site / HTML / landing pages**: stack Next.js + Tailwind v4 + shadcn (base-ui). Use os tokens `wma-*` e `Button`/`ButtonLink` existentes; não crie variantes novas de botão. Fonte via `next/font` (Nunito Sans, `display: swap`).

**E-mail**: fundo externo `#F3F4F6`, cartão branco, texto `#333`, fonte `Nunito, Arial`, links `#932CE3` sublinhados, botão com estilos inline (borda inferior 4px, ver seção 6), largura ≤600px. Sem chips rotacionados com CSS `transform` (clientes de e-mail não suportam): exporte o título como imagem com `alt` descritivo.

**PDF / documentos**: documentos funcionais (recibos, ordens) podem ser sóbrios, mas devem ter logo no topo, texto `#3A1B52` ou `#0F172A`, destaques em `#932CE3` e tabela zebrada `#F8FAFC`. Se o gerador permitir, registre Nunito Sans (hoje o recibo usa Helvetica).

**Post/carrossel (1080×1080 ou 1080×1350) e stories (1080×1920)**:
- Fundo lavanda `#EED9FF`, branco ou o padrão de tracinhos; 1 título em chips (60–120px), 1 linha de apoio em Nunito 600, 1 botão desenhado (CTA) e logo (branco sobre roxo-escuro ou colorido sobre claro) no canto.
- Stories: mantenha texto e logo fora de ~250px do topo e da base.
- Texto mínimo 32px em 1080px de largura. Máximo de 3 cores de destaque por peça.

**Slides**: 16:9, fundo branco/lavanda; título do slide em Nunito 900 maiúsculo ou chips só na capa e nos separadores; corpo ≥24pt; rodapé com logo pequeno. Uma ideia por slide.

**Banners, flyers, impressos**: reserve o padrão de tracinhos para fundo de chamada; cores de impressão: converta os hex para CMYK com perfil e confira o roxo `#932CE3` em prova; use logo preto em P&B.

**WhatsApp (catálogos, tabelas de preço)**: mesma paleta; texto grande, fundo claro, logo no cabeçalho; evite texto menor que 28px em imagens de 1080px.

## 13. Checklist antes de entregar

1. Só Nunito Sans, nos pesos 500/600/700/900?
2. Paleta restrita a roxos + neutros; lima/vermelho/amarelo só em chips?
3. Todos os pares texto/fundo ≥ 4,5:1 (ou ≥ 3:1 se texto grande e restrito)? Rodou o cálculo?
4. Existe exatamente um botão principal e ele tem borda inferior de 4px?
5. Logo na variante certa, sem distorção, com respiro?
6. No máximo um título em chips; rotação ≤ ±3°; cores vizinhas diferentes?
7. Tom divertido, PT-BR, sem jargão; slogan e números conferidos?
8. Alt text em imagens com texto; texto nunca só dentro de imagem em páginas web.

## 14. Não faça

- Não use gradientes decorativos, sombras pesadas ou efeito neon/glass; a marca é plana, com borda grossa e cor chapada (as únicas sombras: balão, selo e cards sutis).
- Não use outras fontes, outros roxos ou outro azul além de `#155DFC`/`#193CB8`/`#1447E6` nos chips e selo.
- Não aplique rotação em parágrafos, botões, logo ou fotos. Só chips, selos e balões de depoimento.
- Não coloque texto amarelo sobre fundo claro nem texto roxo médio sobre roxo-escuro.