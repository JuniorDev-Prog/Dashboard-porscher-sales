# Porsche Sales Intelligence

Dashboard interativa de vendas Porsche, desenvolvida em HTML, CSS e JavaScript para explorar os registros sanitizados do projeto da DIO.

## Acessar a dashboard

Abra [`index.html`](./index.html) no navegador. Para publicar com GitHub Pages, envie `index.html` e este `README.md` para a raiz do repositório e siga as instruções em [Publicação no GitHub Pages](#publicação-no-github-pages).

## O que a dashboard apresenta

### Indicadores

- **Faturamento total:** soma dos preços registrados no recorte selecionado, exibida em USD.
- **Vendas registradas:** quantidade de IDs de venda únicos.
- **Preço médio:** média dos preços registrados, em USD por venda.
- **Modelo líder:** modelo com maior número de registros no recorte.

### Gráficos

- **Modelos mais vendidos:** 10 modelos com mais registros.
- **Vendas por cidade:** 10 cidades com mais registros.
- **Vendas por ano-modelo:** distribuição dos registros por ano-modelo.
- **Formas de pagamento:** participação de cada forma no total de registros.
- **Evolução mensal de vendas:** quantidade de registros por mês, considerando apenas datas válidas.

### Filtros

É possível filtrar por modelo Porsche, ano-modelo, cidade e forma de pagamento. Os indicadores, gráficos e insights são atualizados de acordo com os filtros; use **Limpar filtros** para voltar à visão completa.

## Dados e limitações

Os 100 registros sanitizados usados pela dashboard estão incorporados diretamente no JavaScript de [`index.html`](./index.html); não é necessário carregar uma planilha separada. O conjunto inclui os campos:

- ID da venda e data sanitizada;
- modelo Porsche e ano-modelo;
- preço e quilometragem;
- forma de pagamento;
- cidade e estado;
- status da entrega.

Há 24 registros com data marcada como `INVALID`. Eles não são tratados como datas reais e ficam fora do gráfico mensal. Os valores monetários são exibidos em USD, conforme a configuração da dashboard. O total de preços representa a soma dos valores registrados — não uma validação contábil de receita realizada; os dados também contêm diferentes status de entrega.

A planilha de referência do desafio está disponível em [Planilha base Porsche (sanitizada)](https://hermes.dio.me/files/assets/8683bed0-cc33-4e06-bca9-04db9c31f9e2.xlsx). Confira a versão fornecida no curso antes de comparar resultados ou publicar dados.

## Tecnologias

- HTML, CSS e JavaScript em um único arquivo.
- [Chart.js](https://www.chartjs.org/), carregado por CDN, para os gráficos.
- Layout responsivo com tema escuro e detalhes em vermelho.
- Imagem do cabeçalho incorporada ao HTML.

É necessária conexão com a internet para carregar o Chart.js. A dashboard é uma página estática: não é um arquivo `.pbix` e não contém visuais nativos do Power BI.

## Publicação no GitHub Pages

1. Crie um repositório público no GitHub.
2. Envie `index.html` e `README.md` para a raiz do repositório.
3. No repositório, acesse **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Escolha a branch `main` e a pasta `/ (root)` e salve.
6. Aguarde a publicação e acesse o endereço indicado pelo GitHub. Para um repositório de projeto, o formato costuma ser `https://github.com/JuniorDev-Prog/Dashboard-porscher-sales.git`.
7. Atualize este README com o endereço público e teste os filtros e gráficos.

## Verificação antes da entrega

- [ ] `index.html` abre e exibe os gráficos.
- [ ] Os filtros funcionam individualmente e em conjunto.
- [ ] **Limpar filtros** restaura todos os registros.
- [ ] O site publicado no GitHub Pages está acessível.
- [ ] O README contém o link real da dashboard.
- [ ] Não foram publicados dados pessoais ou colunas desnecessárias.
