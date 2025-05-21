# RecreationDemand

## Descrição Geral

O conjunto de dados `RecreationDemand` contém informações coletadas em 1980 por meio de uma pesquisa com 2.000 proprietários de barcos de lazer registrados em 23 condados do leste do Texas, EUA.

## Estrutura dos Dados

* **Observações**: 659
* **Variáveis**: 8

## Descrição das Variáveis

- **trips**: Número de viagens recreativas de barco realizadas ao Lago Somerville.
- **quality**: Avaliação subjetiva da qualidade das instalações do lago, em uma escala de 1 a 5. Para indivíduos que não visitaram o lago, o valor é 0.
- **ski**: Indica se o indivíduo praticou esqui aquático no lago (`sim` ou `não`).
- **income**: Renda anual da família do entrevistado, em milhares de dólares americanos (USD).
- **userfee**: Indica se o indivíduo pagou uma taxa anual de uso no Lago Somerville (`sim` ou `não`).
- **costC**: Despesa estimada ao visitar o Lago Conroe, em dólares americanos (USD).
- **costS**: Despesa estimada ao visitar o Lago Somerville, em dólares americanos (USD).
- **costH**: Despesa estimada ao visitar o Lago Houston, em dólares americanos (USD).

### Observações

- A variável "quality" inclui o valor 0 para não visitantes, o que pode reduzir sua média, conforme explicado em Seller et al. (1985).
