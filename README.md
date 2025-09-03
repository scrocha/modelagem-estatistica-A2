# Análise de Sobredispersão em Modelos de Contagem com o Conjunto de Dados RecreationDemand

## Introdução e Motivação

Este repositório apresenta uma análise sobre a sobredispersão em modelos de contagem, um fenômeno comum em dados onde a variância é maior que a média, violando uma premissa fundamental do modelo de Poisson. O trabalho explora este conceito utilizando o conjunto de dados `RecreationDemand`.

O objetivo é conduzir uma análise exploratória, ajustar e avaliar um modelo de regressão de Poisson, testar a sobredispersão e, por fim, comparar o modelo de Poisson com alternativas como o Binomial Negativo e o Poisson Inflado de Zeros para determinar o melhor ajuste para os dados.

## Conjunto de Dados: RecreationDemand

O conjunto de dados `RecreationDemand` contém informações de uma pesquisa de 1980 com 2.000 proprietários de barcos de lazer no leste do Texas, EUA. O foco da análise é a variável `trips`, que representa o número de viagens de barco ao Lago Somerville.

As variáveis do conjunto de dados são:
* **trips**: Número de viagens de barco ao Lago Somerville.
* **quality**: Avaliação da qualidade das instalações do lago (escala 1-5, 0 para não visitantes).
* **ski**: Se o indivíduo praticou esqui aquático (`sim` ou `não`).
* **income**: Renda anual da família (em milhares de USD).
* **userfee**: Se pagou taxa anual de uso (`sim` ou `não`).
* **costC**: Custo estimado para visitar o Lago Conroe (USD).
* **costS**: Custo estimado para visitar o Lago Somerville (USD).
* **costH**: Custo estimado para visitar o Lago Houston (USD).

## Estrutura do Repositório

* [**trabalho.ipynb**](./trabalho.ipynb): Notebook Jupyter contendo toda a análise, desde a exploração dos dados até o ajuste e comparação dos modelos.
* [**trabalho/StatMod.md**](./trabalho/StatMod.md): Arquivo com a descrição detalhada do problema, motivação e questões norteadoras do trabalho.
* [**trabalho/DatasetDescrição.md**](./trabalho/DatasetDescrição.md): Descreve o conjunto de dados `RecreationDemand`.
* [**trabalho/Requisitos.md**](./trabalho/Requisitos.md): Ficha de avaliação com os critérios e pontuações para o trabalho.
* [**images/**](./images/): Diretório contendo os gráficos gerados na análise, como a distribuição das variáveis, matriz de correlação e distribuição dos resíduos dos modelos.
* [**models/**](./models/): Contém os sumários dos modelos estatísticos ajustados.

## Análise e Modelos

A análise no notebook `trabalho.ipynb` segue os seguintes passos:

1.  **Análise Exploratória dos Dados**: Investigação inicial das variáveis, suas distribuições e correlações para informar a seleção de covariáveis.
2.  **Ajuste do Modelo de Poisson**: Um modelo de regressão de Poisson é ajustado para modelar a contagem de viagens.
3.  **Teste de Sobredispersão de Cameron & Trivedi (1990)**: É aplicado um teste para verificar se a variância dos dados é significativamente maior que a média, indicando a inadequação do modelo de Poisson.
4.  **Ajuste do Modelo Binomial Negativo**: Como alternativa ao Poisson, um modelo Binomial Negativo é ajustado, por ser mais flexível para lidar com a sobredispersão.
5.  **Análise de Excesso de Zeros e Modelo Poisson Inflado de Zeros**: A análise investiga se um excesso de observações zero pode ser a causa da sobredispersão e ajusta um modelo de Poisson Inflado de Zeros.
