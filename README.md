# Previsão de Vendas com Campanhas Publicitárias - Hashtag

Este repositório contém um projeto de Ciência de Dados focado na previsão de vendas de uma empresa fictícia chamada **Hashtag**, com base nos investimentos realizados em campanhas publicitárias na TV, rádio e jornal.

## Descrição

O objetivo do projeto é criar um modelo de previsão de vendas a partir dos investimentos realizados em publicidade nos canais de TV, rádio e jornal. A partir da análise e modelagem dos dados, serão feitas previsões de vendas para diferentes opções de investimentos.

## Base de Dados

A base de dados utilizada neste projeto está disponível através do seguinte link do Google Drive:

[Base de Dados - Publicidade e Vendas](https://drive.google.com/file/d/1SkpWM5jRJeXZ-wfVWB7JedxjCVBV_mAC/view?usp=sharing)

A base de dados contém os seguintes campos:

- **TV**: Valor investido em publicidade na TV (milhares de reais)
- **Radio**: Valor investido em publicidade no rádio (milhares de reais)
- **Jornal**: Valor investido em publicidade no jornal (milhares de reais)
- **Vendas**: Valor das vendas realizadas (milhões de reais)

## Bibliotecas Utilizadas

- `pandas`: Para manipulação de dados.
- `numpy`: Para operações matemáticas e numéricas.
- `openpyxl`: Para ler e escrever arquivos Excel.
- `matplotlib`: Para criação de gráficos e visualizações.
- `seaborn`: Para visualizações gráficas com mais estilo.
- `scikit-learn`: Para implementação dos modelos de aprendizado de máquina.

## Etapas do Projeto

### 1. Entendimento do Desafio
O desafio consiste em prever o volume de vendas de acordo com o investimento em publicidade nos meios de comunicação (TV, rádio e jornal).

### 2. Preparação dos Dados
- **Importação dos Dados**: Carregamento da base de dados para análise.
- **Análise Exploratória dos Dados**: Investigação das relações e correlações entre variáveis.
- **Limpeza dos Dados**: Verificação de dados ausentes e tipos de dados.

### 3. Análise Exploratória

A análise da correlação entre as variáveis revelou que os investimentos em TV têm uma correlação muito forte com as vendas (0.90), enquanto os investimentos em rádio e jornal apresentam uma correlação moderada (0.35 e 0.16, respectivamente).

### 4. Modelagem com Machine Learning

Foram utilizados dois modelos de regressão para prever as vendas:

- **Regressão Linear**: Modelo simples que tenta ajustar uma reta aos dados.
- **Random Forest Regressor**: Modelo baseado em várias árvores de decisão para prever os valores.

### 5. Divisão dos Dados
Os dados foram divididos em conjuntos de treinamento e teste utilizando a função `train_test_split` do Scikit-Learn.

### 6. Treinamento e Avaliação do Modelo

Os modelos foram avaliados usando a métrica R², que indica o quanto o modelo consegue explicar a variação dos dados. A pontuação do modelo de **Árvore de Decisão** foi de 0.94, sendo o modelo mais preciso.

### 7. Visualização das Previsões

Foram gerados gráficos de linha comparando as previsões de vendas feitas pelos dois modelos.

### 8. Previsões Finais

O modelo de Árvore de Decisão foi usado para prever o impacto de novos investimentos em publicidade, com os seguintes resultados para as opções de investimento:

| TV (milhares) | Rádio (milhares) | Jornal (milhares) | Previsão de Vendas (milhões) |
|---------------|------------------|-------------------|-----------------------------|
| 23.1          | 3.8              | 69.2              | 7.44                        |
| 44.5          | 0.0              | 5.1               | 8.29                        |
| 170.2         | 45.9             | 0.0               | 20.92                       |

## Como Rodar o Projeto

### Requisitos

- Python 3.x
- Bibliotecas Python: pandas, numpy, openpyxl, matplotlib, seaborn, scikit-learn

Você pode instalar todas as bibliotecas necessárias utilizando o seguinte comando:

```bash
pip install -r requirements.txt
```
