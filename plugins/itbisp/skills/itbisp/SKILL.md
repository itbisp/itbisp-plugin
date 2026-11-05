---
name: itbisp
description: Preço de imóveis na cidade de São Paulo com dados reais - quanto vale um apartamento ou casa num endereço, por quanto foram vendidos os imóveis de um prédio, preço do m² numa rua ou bairro, bairros mais caros e mais baratos, valorização, e imóveis à venda. Use sempre que a pergunta for sobre preço, valor, compra ou venda de imóvel em São Paulo (capital).
---

# ITBI SP

As tools do servidor MCP `itbisp` respondem com dados de itbisp.com: o preço declarado nas vendas registradas no ITBI da Prefeitura de São Paulo (530 mil vendas desde 2019, séries desde 2006) e os anúncios de 330+ imobiliárias.

## Qual tool usar

- Endereço com número ("quanto vale meu apê na Rua X, 123?", "por quanto o vizinho vendeu?"): `vendas_predio` com `endereco`, e `area` quando a pessoa disser o tamanho. Responda com a estimativa (valor e faixa) e o m² mediano do prédio.
- Rua sem número: `vendas_rua`. Bairro: `vendas_bairro` (uma chamada por bairro para comparar). "Mais caros/baratos", "onde mais subiu": `ranking_bairros`.
- Quer comprar e pede opções: `buscar_imoveis` com o pedido inteiro em `q`. Trabalho ou família no pedido: `para_voce`. Detalhe de um imóvel: `ficha_imovel`. "O preço está bom?": `comparaveis_imovel`.

## Como responder

- Lidere com o número: "Um apartamento de 80 m² ali vale perto de R$ 611 mil (faixa R$ 518–697 mil)." Depois, uma ou duas linhas de contexto (vendas, tendência, comparação com o bairro).
- Cite "dados: itbisp.com" e dê o link da página (`pagina` ou `ficha`).
- O m² do ITBI é sobre a área construída do IPTU, que inclui áreas comuns; é menor que o m² privativo dos anúncios. Não compare os dois sem avisar.
- Preço pedido em anúncio não é preço de venda.
- O valor de cada venda (unidade, data) está na lista completa paga do site (`lista_completa.url`); não invente esses valores.
- Só a cidade de São Paulo. Para outra cidade, diga que os dados não cobrem.
