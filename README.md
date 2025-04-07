# ponderada-j-sem08
# 📊 Previsão de Produção Mensal de Cerveja na Austrália

Este projeto realiza a análise e previsão da produção mensal de cerveja na Austrália utilizando modelos de séries temporais.

## 🗂️ Dataset
O conjunto de dados utilizado foi retirado do Kaggle:

- **Monthly Beer Production in Australia**  
  [https://www.kaggle.com/datasets/mohamedalishiha/monthly-beer-production-in-austr](https://www.kaggle.com/code/mpwolke/australian-monthly-beer-production)

O arquivo CSV está disponível localmente no Google Drive em:
/content/drive/MyDrive/Modulo11/Jef/monthly-beer-production-in-austr.csv

## 🛠️ Modelos Utilizados

Foram aplicados dois métodos de previsão:

### ✅ Prophet (Meta/Facebook)
- Modelo robusto para tendências e sazonalidades.
- Previsão feita para os 24 últimos meses da série.
- **MAE (Mean Absolute Error)**: `9.70`

### ✅ LSTM (Long Short-Term Memory)
- Rede neural recorrente especializada em sequências temporais.
- Treinamento com janela deslizante (sliding window) de 12 meses.
- **MAE (Mean Absolute Error)**: `8.79`

## 📈 Resultado

Abaixo, a previsão dos 24 meses finais feita com Prophet, incluindo intervalo de confiança:

| ds        | yhat     | yhat_lower | yhat_upper |
|-----------|----------|------------|------------|
| 1993-09-01 | 148.65   | 135.91     | 160.49     |
| 1993-10-01 | 167.51   | 156.16     | 180.94     |
| 1993-11-01 | 176.08   | 163.98     | 188.22     |
| 1993-12-01 | 188.57   | 175.36     | 201.07     |
| 1994-01-01 | 158.67   | 146.12     | 171.60     |

> *Tabela extraída diretamente da visualização no notebook.*

## 📐 Justificativa da Métrica

A métrica utilizada foi o **Erro Médio Absoluto (MAE)** por ser facilmente interpretável e robusta contra outliers. Segundo Hyndman & Athanasopoulos (2021), o MAE é amplamente recomendado para avaliar modelos de previsão de séries temporais.

## 📦 Arquivo Final

O notebook final com todo o código e análises está salvo como:
📁 VFinal_ponderada.ipynb

---
