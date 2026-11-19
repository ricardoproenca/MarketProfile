# Market Profile

Notebook de estudo sobre Perfil de Mercado (Market Profile), com consultas a dados históricos de ações, cálculo de métricas do perfil e visualização de preços.

## Conteúdo

O arquivo [`marketprofile.ipynb`](marketprofile.ipynb) apresenta os conceitos de TPO, balanço inicial, área de valor, VAH, VAL, POC, caudas, intervalo e extensão de intervalo. Em seguida, usa a biblioteca `marketprofile` para calcular essas medidas a partir de cotações históricas e apresenta um gráfico de candlestick.

## Fluxo do notebook

1. **Carrega dados históricos** para `COGN3.SA` usando `pandas_datareader`, com fonte Yahoo e intervalo de 1 a 20 de agosto de 2020.
2. **Cria o perfil** com `MarketProfile` e seleciona o período disponível.
3. **Consulta métricas** do perfil: distribuição (`profile`), balanço inicial, faixa de abertura, POC, faixa do perfil, área de valor, alvo balanceado e nós de baixo/alto valor.
4. **Visualiza preços** em um gráfico interativo de candlestick com Plotly.
5. **Exibe um resumo** com balanço inicial, faixa de abertura, POC, faixa do perfil, área de valor e alvo balanceado.

As explicações conceituais e operacionais do notebook são introdutórias. Perfil de Mercado é apresentado como ferramenta de leitura do contexto e sentimento do mercado, não como estratégia autônoma de entrada e saída.

## Como executar

O notebook foi escrito para um ambiente Jupyter. Instale as dependências usadas nas células:

```bash
pip install marketprofile pandas-datareader matplotlib plotly
```

Depois, abra `marketprofile.ipynb` no Jupyter e execute as células em ordem. O notebook solicita dados do Yahoo Finance por meio do `pandas_datareader`; a disponibilidade dos dados depende da fonte e da conexão no momento da execução. Para analisar outro ativo ou período, altere o ticker e as datas na célula de carregamento.

## Referência

O notebook cita como fonte conceitual: [The Ultimate Guide to Market Profile](https://eminimind.com/the-ultimate-guide-to-market-profile/).
