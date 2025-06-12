# 🎓 Student Performance Prediction

Este projeto tem como objetivo prever o desempenho acadêmico de estudantes com base em fatores como condição socioeconômica, horas de estudo, sono e frequência escolar, utilizando técnicas de Machine Learning.

## 📁 Dataset

- **Fonte**: [Predict Student Performance Dataset - Kaggle](https://www.kaggle.com/datasets/stealthtechnologies/predict-student-performance-dataset)
- **Descrição**: O dataset é sintético, com 1.388 registros e 5 colunas numéricas. Cada linha representa um estudante.

### 📌 Colunas do Dataset

| Coluna               | Descrição                                               |
|----------------------|----------------------------------------------------------|
| `Socioeconomic Score`| Índice que reflete a condição socioeconômica do estudante |
| `Study Hours`        | Média de horas de estudo por dia                          |
| `Sleep Hours`        | Média de horas de sono por noite                          |
| `Attendance (%)`     | Percentual de presença nas aulas                          |
| `Grades`             | Nota final do estudante (variável alvo)                  |

---

## 🤖 Modelos Utilizados

Treinamos três modelos de regressão supervisionada para prever a nota final (`Grades`):

1. **Random Forest Regressor**
2. **K-Nearest Neighbors (KNN)**
3. **Rede Neural com TensorFlow (Sequential API)**

---

## ⚙️ Métricas de Avaliação

Para comparar o desempenho dos modelos de machine learning, utilizamos três métricas principais:

- **MAE (Mean Absolute Error)**  
  Mede o erro médio absoluto entre as previsões e os valores reais.  
  > *Quanto menor, melhor.* Representa o erro médio em unidades da variável de saída.

- **MSE (Mean Squared Error)**  
  Calcula o erro quadrático médio, penalizando com mais intensidade erros maiores.  
  > *Quanto menor, melhor.* Erros grandes têm impacto mais significativo.

- **R² (Coeficiente de Determinação)**  
  Indica o quanto do comportamento da variável dependente é explicado pelo modelo.  
  > *Varia de 0 a 1.* Quanto mais próximo de 1, melhor o desempenho explicativo do modelo.

### 📊 Resultados

| Modelo              | MAE    | MSE     | R²        |
|---------------------|--------|---------|-----------|
| Random Forest       | 1.33   | 3.78    | 0.9590    |
| KNN                 | 2.57   | 17.44   | 0.8080    |
| TensorFlow (Rede Neural) | 1.72   | 4.79    | 0.9473    |

---

## 📈 Conclusões

- A **Random Forest** obteve o melhor desempenho geral, com menor MSE e maior R².
- A **rede neural com TensorFlow** também apresentou bons resultados, com performance próxima da Random Forest.
- O **KNN** teve o pior desempenho entre os três modelos, mostrando maior erro e menor capacidade explicativa, possivelmente devido à sensibilidade à escala e ao valor de K.

---

## 🚀 Possíveis Melhorias

- Testar outros algoritmos como XGBoost, SVR ou LightGBM
- Ajuste fino de hiperparâmetros com GridSearchCV ou RandomizedSearchCV
- Cross-validation para validar generalização
- Análise de importância das variáveis (especialmente com Random Forest)

---

## 📎 Requisitos

- Python 3.12.7
- Pandas, Scikit-learn, TensorFlow, NumPy, Matplotlib, Seaborn

---


