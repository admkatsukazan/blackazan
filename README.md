# BLACKAZAN

Contador ao vivo de pedidos pagos da Katsukazan na Nuvemshop, para a campanha de novembro de 2026, com 7 metas: 2.450, 2.800, 3.150, 3.550, 3.900, 4.250 e 4.600 pedidos.

**Link:** https://admkatsukazan.github.io/blackazan/

## Como funciona

- **Apps Script (Google):** guarda o token da Nuvemshop, lê os pedidos e entrega os números num link que termina em `/exec`. O código fica em `Codigo.gs`, no projeto BLACKAZAN do Apps Script.
- **GitHub Pages (este repositório):** publica a página. Ela busca os números no link do Apps Script a cada 30 segundos.
- O repositório não guarda token nem dados de cliente. O único dado de configuração é o link do Apps Script, em `config.js`.

## Arquivos

| Arquivo | Para que serve |
| --- | --- |
| `index.html` | A página do contador |
| `bg.jpg` | Imagem de fundo |
| `config.js` | O link do Apps Script |

## Trocar metas ou data de início

No Apps Script, no topo de `Codigo.gs`: `METAS` e `INICIO`. Depois, publique uma nova versão em **Implantar → Gerenciar implantações → lápis → Nova versão**. A página do GitHub pega as metas e a data sozinha.
