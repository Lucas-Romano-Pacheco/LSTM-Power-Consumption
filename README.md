# LSTM-Power-Consumption
Este projeto consiste em uma solução de Deep Learning para análise e previsão de séries temporais (Time Series Forecasting), focada no consumo de energia elétrica residencial. O objetivo principal é utilizar dados históricos para prever o consumo futuro de energia, aplicando Redes Neurais Recorrentes (RNN) do tipo Long Short-Term Memory (LSTM).

## 📋 Visão Geral do Pipeline

O projeto segue um fluxo de dados completo (**End-to-End**), estruturado nas seguintes etapas:

1.  **Pré-processamento e Limpeza (ETL)**
    * Ingestão de dados brutos (`household_power_consumption.txt`), com tratamento de valores nulos e formatação de datas.
    * Reamostragem temporal para análise de tendências diárias, semanais e mensais.

2.  **Análise Exploratória e Estatística**
    * Visualização da média de consumo em diferentes escalas de tempo.
    * Verificação de estacionariedade da série temporal utilizando o teste estatístico **Augmented Dickey-Fuller (ADF)**.

3.  **Engenharia de Atributos (Feature Engineering)**
    * Normalização dos dados (escala 0 a 1) com `MinMaxScaler` para otimizar o desempenho da rede neural.
    * Criação de janelas temporais (**Look Back**), onde o modelo utiliza os últimos 30 minutos para prever o consumo do minuto seguinte.

4.  **Modelagem Preditiva (Deep Learning)**
    * Construção de uma arquitetura **LSTM (Long Short-Term Memory)** com camadas de *Dropout* para regularização (evitar overfitting).
    * Utilização de *Early Stopping* para interrupção automática do treinamento ao atingir a convergência.

5.  **Avaliação e Resultados**
    * Cálculo de métricas de erro como o **RMSE** (Root Mean Squared Error).
    * Visualização comparativa entre os dados reais e as previsões geradas pelo modelo.



---

## 🛠️ Tecnologias Utilizadas

Este projeto foi desenvolvido utilizando as seguintes ferramentas e bibliotecas:

* **Linguagem:** Python 🐍
* **Manipulação de Dados:** Pandas, NumPy
* **Visualização:** Matplotlib, Seaborn
* **Machine Learning & Estatística:** Scikit-learn, Statsmodels
* **Deep Learning:** Keras (TensorFlow backend)
