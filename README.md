# 🛡️ Detecção de Fraudes em Cartão de Crédito

![Python](https://shields.io)
![Scikit-Learn](https://shields.io)
![Pandas](https://shields.io)

Este projeto visa desenvolver um sistema robusto de detecção de fraudes em transações de cartão de crédito utilizando técnicas avançadas de **Aprendizado de Máquina**. 

O desafio central reside no desequilíbrio extremo do dataset (*Credit Card Fraud Detection*), onde as fraudes representam uma fração mínima do total de transações, exigindo estratégias específicas de pré-processamento e avaliação.

---

## 📋 Resumo do Pipeline

O notebook [`deteccao_anomalias_creditcard.ipynb`](./deteccao_anomalias_creditcard.ipynb) implementa o seguinte fluxo de trabalho:

### 1. 🔍 Exploração e Diagnóstico
* **Análise Estatística:** Visualização inicial e entendimento da distribuição das classes.
* **Exploração de Dados:** Identificação de padrões em transações normais vs. fraudulentas.

### 2. 🛠️ Pré-processamento
* **Limpeza de Dados:** Preparação e verificação de integridade do dataset.
* **Escalonamento:** Tratamento de variáveis como `Time` e `Amount` para garantir que o modelo não seja enviesado por escalas diferentes.

### 3. ⚖️ Balanceamento do Dataset
Devido ao desequilíbrio de classes, foram aplicadas técnicas para melhorar o aprendizado do modelo:
* **Undersampling:** Redução da classe majoritária.
* **Oversampling (SMOTE):** Criação de dados sintéticos para a classe minoritária (fraudes).

### 4. 🧠 Modelos de Machine Learning
Implementação de algoritmos de alta performance:
* **Random Forest Classifier:** Modelo baseado em múltiplas árvores de decisão.
* **XGBoost Classifier:** Algoritmo de Gradient Boosting otimizado para velocidade e performance.

### 5. 📉 Avaliação e Otimização
* **Métricas Reais:** Foco em *Recall*, *Precision* e *F1-Score* (evitando a armadilha da acurácia simples).
* **Ajuste de Threshold:** Otimização do ponto de decisão para equilibrar a detecção de fraudes e a experiência do cliente.
* **Tuning de Hiperparâmetros:** Uso de `Grid Search` para extrair a máxima performance do XGBoost.

### 6. 💡 Análise de Importância
* Identificação das **Features** mais relevantes, permitindo entender quais variáveis (anônimas V1-V28) possuem maior poder preditivo na detecção de anomalias.

---

## 🎯 Objetivo Final
Maximizar a precisão na identificação de transações fraudulentas (sensibilidade), mantendo sob controle o índice de falsos positivos para evitar bloqueios indevidos de clientes legítimos.

---
*Projeto desenvolvido como parte do portfólio de Data Science.*
