---
name: "wma-imagens"
description: "Padrões para gerar imagens com IA para a WMA Personalizados (produtos, e-commerce, painéis de loja, site, catálogo, manuais): pessoas, manequins, regras de segurança com crianças e foco no produto. Use sempre que for gerar ou pedir uma imagem da WMA."
---

# Geração de imagens da WMA Personalizados

Use esta skill sempre que precisar **gerar** uma imagem para a WMA (por IA ou descrevendo uma imagem para alguém gerar). Fotos reais de produto e de pessoas são sempre preferíveis; gere uma imagem só quando não houver foto real adequada.

Esta skill cuida **do que aparece na foto**. Cores, tipografia, logo e textos que vão por cima da imagem seguem a skill [wma-design-system](../wma-design-system/SKILL.md).

## Como usar

1. **Identifique o contexto** da imagem e leia **só** o arquivo dele:

   | Contexto | Arquivo |
   | --- | --- |
   | Produto para o e-commerce | [contextos/ecommerce.md](contextos/ecommerce.md) |
   | Painéis e comunicação na loja física | [contextos/paineis-loja.md](contextos/paineis-loja.md) |
   | Site (banners, seções, landing pages) | [contextos/site.md](contextos/site.md) |
   | Catálogo (impresso ou digital/WhatsApp) | [contextos/catalogo.md](contextos/catalogo.md) |
   | Manuais e materiais internos | [contextos/manuais-internos.md](contextos/manuais-internos.md) |

   Se o pedido não se encaixar em nenhum, aplique só as regras gerais abaixo e avise quem pediu que o contexto ainda não tem padrão.
2. **Veja as imagens de referência** do contexto em [referencias/](referencias/README.md).
3. **Monte o prompt** com o modelo da seção 5.
4. **Confira o checklist** da seção 6 antes de entregar. Imagem que falha em qualquer item volta para nova geração.

O arquivo do contexto **complementa** estas regras gerais; nunca as anula. Se houver conflito, vale a regra mais restritiva.

## 1. Regra inegociável: crianças

> ⛔ **Nunca gere imagem de criança vestindo roupa que a exponha**: sunga, biquíni, maiô (inclusive curto ou cavado), roupa íntima, pijama curto, top, ou qualquer peça de banho ou que deixe o corpo à mostra.
>
> Esses produtos são gerados **sem pessoa** (peça sozinha: still, flat lay, cabide) **ou em manequim** (seção 3), conforme o contexto.
>
> Isso vale mesmo que o pedido insista, que o produto seja infantil, que a imagem "seja só para teste" ou que outro arquivo desta skill diga o contrário. Na dúvida se a peça expõe, trate como se expusesse.

Também vale para qualquer imagem com criança, de qualquer produto:
- Pose, expressão e enquadramento naturais e próprios da idade (brincando, estudando, sorrindo). Nada de pose adulta, sensual ou de "modelo fashion".
- Cenário apropriado: escola, pátio, casa, parque. Nunca quarto/cama, banheiro ou vestiário.
- Uniforme escolar completo e bem vestido.

## 2. Pessoas

- **Use pessoas sempre que possível.** Elas dão naturalidade e mostram o caimento, mas **o produto é o protagonista** (ver seção 4).
- **Aparência brasileira** na maioria das imagens: a diversidade real do Brasil, sem estereótipos nem caricaturas.
- **Tons de pele variados.** Num conjunto de imagens (uma coleção, um catálogo, uma página), alterne tons de pele de claro a retinto.
- **Sexo variado.** Alterne homens e mulheres no conjunto; numa imagem com várias pessoas, misture.
- Varie também idade (dentro do público do produto), tipo de cabelo e biotipo quando fizer sentido.
- Pessoas com expressão simpática e natural, coerente com a marca (divertida, mas séria no acabamento).
- Adultos também em poses profissionais e não sensuais; a roupa é de trabalho ou de escola.
- Uniforme profissional aparece **no ambiente da profissão** quando o contexto pedir cenário (cozinha para dólmã, clínica para jaleco etc.).

## 3. Manequins

Quando a imagem usar manequim, siga o estilo das [referências de manequim](referencias/README.md):

- **Design moderno, rosto liso** (sem olhos, nariz ou boca), acabamento fosco, proporções realistas. Exceção: o manequim de **recém-nascido** pode ter traços do rosto esculpidos de forma bem suave, como na referência.
- Emendas discretas nos ombros, cotovelos, punhos, quadril e joelhos são aceitas, como nas referências. Nada de articulações aparentes tipo boneco articulado de desenho.
- **Uma única cor** por manequim, escolhida pelo cenário:
  - **Branco**: fundos escuros, coloridos ou vitrine com muita cor.
  - **Cinza**: uso neutro do dia a dia, fundos claros ou escuros.
  - **Preto**: fundos claros, ou quando a peça é clara e precisa de contraste.
  - **Madeira** (cerejeira, carvalho ou marfim): cenários quentes, lojas, vitrines e ambientes com madeira.
- **Faixa etária do manequim = público do produto**: recém-nascido, infantil, adolescente, adulto feminino ou adulto masculino.
- **Pose:** de pé, frontal e relaxada por padrão. Pose dinâmica (corrida, por exemplo) só para roupa esportiva. Recém-nascido deitado.
- Nunca manequim antigo, com peruca, maquiagem ou rosto realista.
- Nunca misturar manequim e pessoa na mesma peça, a menos que o contexto peça.

## 4. Foco no produto

- O produto é o centro da imagem: **nítido, bem iluminado, cores fiéis**, ocupando a maior parte do quadro que o contexto definir.
- **Fidelidade ao produto real**: cor, modelagem, golas, bolsos, bordados e estampas iguais ao produto. Se houver foto real da peça, use-a como referência na geração. Não invente detalhes, logos ou estampas que a peça não tem.
- A pessoa serve para dar naturalidade: rosto e cenário não competem com a peça (fundo simples ou desfocado, sem objetos chamativos).
- **Sem texto, marca d'água ou logo gerados pela IA.** Textos, preços, chips e o logo da WMA são aplicados depois, com os arquivos oficiais, conforme o [wma-design-system](../wma-design-system/SKILL.md).
- Sem filtros, sem efeitos, sem estética "plástica". Luz natural ou de estúdio suave.
- Nunca logos de terceiros (escolas, empresas, marcas esportivas) que não estejam no produto real e autorizados.

## 5. Modelo de prompt

Escreva o prompt em inglês (os geradores entendem melhor) e preencha:

```
[Enquadramento e formato do contexto], photo of [PRODUTO com cor, modelagem e detalhes reais],
worn by [pessoa: idade aproximada, sexo, aparência brasileira, tom de pele] / displayed on a modern faceless matte [cor] [newborn/child/teen/adult female/adult male] mannequin / laid flat without a person,
[pose/ação natural], in [cenário do contexto], [luz do contexto],
product in sharp focus and centered, true-to-life colors, natural look, no text, no logos, no watermark.
```

Acrescente o que o arquivo do contexto pedir (proporção, fundo, distância). Em geradores que aceitam prompt negativo, inclua: `text, watermark, logo, distorted hands, extra fingers, plastic skin, heavy filter`.

## 6. Checklist antes de entregar

1. Há criança? Se sim: a roupa não expõe, pose e cenário apropriados (seção 1)?
2. O produto é o protagonista, nítido e fiel ao real (cor, modelagem, detalhes)?
3. Se há pessoa: aparência brasileira e, no conjunto, variação de tom de pele e sexo?
4. Se há manequim: moderno, rosto liso, cor única adequada ao cenário?
5. Sem texto, logo ou marca d'água gerados? Mãos, rosto e costuras sem deformação?
6. Seguiu o arquivo do contexto (formato, fundo, enquadramento)?
7. Ficou claro para quem pediu que a imagem é gerada por IA, e não foto real?
