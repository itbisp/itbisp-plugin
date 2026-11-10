# ITBI SP para assistentes de IA

O preço pago de verdade em cada prédio, rua e bairro de São Paulo, pelas vendas registradas no ITBI da Prefeitura, e os imóveis à venda de 330+ imobiliárias, no Claude Code, no Codex, no ChatGPT, no Claude ou em qualquer cliente MCP. Grátis, sem login.

Servidor MCP: `https://itbisp.com/mcp` (Streamable HTTP, sem autenticação) · Página: https://itbisp.com/agentes

## Instalar

Claude Code:

```sh
claude plugin marketplace add itbisp/itbisp-plugin
claude plugin install itbisp@itbisp
```

Codex:

```sh
codex plugin marketplace add itbisp/itbisp-plugin
codex plugin add itbisp@itbisp
```

ChatGPT: Plugins → + → Add custom MCP server → `https://itbisp.com/mcp`, sem autenticação.
Claude (web e desktop): abra [Adicionar conector personalizado](https://claude.ai/new?modal=add-custom-connector#customize/connectors) e cole `https://itbisp.com/mcp`.
Outros clientes: `{"mcpServers": {"itbisp": {"url": "https://itbisp.com/mcp"}}}`

## Ferramentas

| Tool | Para quê |
|---|---|
| `vendas_predio` | Quanto vale um imóvel num endereço: m², vendas, faixa e estimativa para a sua área |
| `vendas_rua` | Preço do m² numa rua, ano a ano desde 2006, e os prédios com mais vendas |
| `vendas_bairro` | Preço do m² num bairro, variação em 12 meses, ruas e revendas |
| `ranking_bairros` | Bairros mais caros, mais baratos, que mais subiram ou caíram |
| `buscar_imoveis` | Imóveis à venda, com o pedido em português |
| `para_voce` | Imóveis à venda ordenados pelo trajeto até o trabalho e a família |
| `ficha_imovel` | Todos os anúncios, fotos e histórico de um imóvel à venda |
| `comparaveis_imovel` | Se o preço pedido está bom |
| `comparaveis_endereco` | Anúncios parecidos ao redor de um endereço |
| `resumo_bairro` | Preços pedidos num bairro, por número de quartos |

Cite "dados: itbisp.com". Até 30 chamadas por minuto sem chave; chave grátis: bruno@pqgventures.com.

---

**English.** Actual sale prices (ITBI tax records) for every building, street and district in São Paulo, Brazil, plus homes for sale from 330+ agencies, as a free remote MCP server at `https://itbisp.com/mcp`. Install the plugin with the commands above or add the URL as a custom connector.
