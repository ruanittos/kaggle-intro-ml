# Previsão de Preços de Imóveis (Iowa Housing - Kaggle)

Desenvolvimento e validação de modelos preditivos de regressão para estimar com precisão os preços de venda de imóveis no estado de Iowa (EUA). O projeto abrange desde a preparação e alinhamento de esquemas de dados até a otimização de hiperparâmetros e submissão final em competição.

---

## 🎯 Competências e Aprendizados do Projetos

### 1. Entendimento Interno do Ciclo de ML (`.fit()` e `.predict()`)
* **Compreensão do `.fit(X, y)`:** Abordagem teórica do treinamento como um processo matemático de otimização (minimização do erro MSE em divisões de nós) e não como um comando mecânico.
* **Reprodutibilidade do Experimento (`random_state`):** Controle da semente pseudoaleatória para garantir estabilidade e reprodutibilidade nas divisões dos dados e treinamento do modelo.
* **Prevenção de *Data Leakage*:** Separação estrita dos dados de validação (`val_X`, `val_y`) durante o ajuste do modelo, garantindo testes fiéis em dados nunca vistos.

### 2. Avaliação e Diagnóstico de Performance
* **Inspeção de Previsões e Métricas Globais:** Leitura comparativa entre o vetor de predições e os valores reais, consolidando a avaliação de desempenho por meio do **MAE (Mean Absolute Error)**.
* **Diagnóstico de Underfitting vs. Overfitting:** Identificação do comportamento do modelo em relação à sua profundidade e número de folhas (`max_leaf_nodes`).
* **Busca do Ponto Ideal de Otimização:** Criação de rotina iterativa em Python usando dicionários para mapear hiperparâmetros ao erro, extraindo programaticamente a melhor arquitetura de árvore.

### 3. Modelagem Avançada e Ensemble Methods
* **Evolução de Arquitetura:** Transição de uma única Árvore de Decisão (`DecisionTreeRegressor`) para um método de Ensemble com Florestas Aleatórias (`RandomForestRegressor`).
* **Redução de Variância:** Utilização do algoritmo de Bagging para combinar múltiplas árvores e aumentar a capacidade de generalização e estabilidade preditiva.

### 4. Engenharia de Produção e Validação de Esquema
* **Consistência de Features (Schema Match):** Garantia de alinhamento exato entre as colunas do dataset de treino e o dataset de teste (`test_X = test_data[features]`).
* **Retreinamento Final (*Full Retraining*):** Aplicação da boa prática de ajustar o modelo campeão com 100% dos dados disponíveis (`X`, `y`) antes da fase de inferência em produção.
* **Geração de Artefato e Submissão:** Exportação automatizada dos resultados finais em formato `.csv` estruturado conforme os requisitos da competição.

---

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python
* **Manipulação de Dados:** Pandas
* **Machine Learning:** Scikit-Learn (`DecisionTreeRegressor`, `RandomForestRegressor`, `mean_absolute_error`)
* **Plataforma de Execução:** Kaggle Notebooks
