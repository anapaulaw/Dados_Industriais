O objetivo deste projeto é desenvolver um **modelo preditivo** capaz de **identificar antecipadamente a probabilidade de falha** em máquinas com base em variáveis de sensores.
Este trabalho simula um caso real de **Manutenção Preditiva**, tema amplamente aplicado em indústrias 4.0, centros logísticos e sistemas de monitoramento de equipamentos.

_____________________________________________________________________________________________________________________________________________________________________________

##Objetivo

Construir um **modelo supervisionado** para prever se uma máquina irá apresentar falha, utilizando dados de sensores e variáveis operacionais.  
O foco está em:
- Detectar padrões que antecedem as falhas;
- Equilibrar as classes de falha e não falha;
- Comparar diferentes algoritmos de classificação;
- Explicar os resultados de forma interpretável e prática.

____________________________________________________________________________________________________________________________________________________________________________

#Pipeline 

### 1. **Importação e Limpeza de Dados**
- Leitura da base original
- Padronização de nomes e tratamento de valores ausentes
- Remoção de identificadores irrelevantes para o modelo

### 2. **Análise Exploratória (EDA)**
- Distribuição das variáveis numéricas e categóricas
- Correlação entre sensores
- Análise da variável-alvo (`machine_failure`)
- Identificação de colinearidade e outliers

### 3. **Engenharia de Atributos**
- Criação de variáveis derivadas (interações entre sensores);
- Normalização dos dados numéricos;
- Codificação de variáveis categóricas (`OneHotEncoder`);
- Inclusão de variáveis de tendência e estatísticas agregadas.


_____________________________________________________________________________________________________________________________________________________________________________

###Balanceamento de Classes

- Utilização do **SMOTEENN** (combinação de oversampling e undersampling)  
  → Melhora o equilíbrio entre casos de falha e não falha sem inflar ruído artificial.
____________________________________________________________________________________________________________________________________________________________________________

### 5. **Modelagem**

Modelos comparados:
- 🔹 **Regressão Logística** 
- 🌲 **Random Forest**  
- ⚡ **XGBoost** 

Ajuste de hiperparâmetros via **GridSearchCV** com validação estratificada (F1-score como métrica principal).


__________________________________________________________________________________________________________________________________________________________

### Avaliação

Métricas utilizadas:
- Accuracy, Precision, Recall, F1-score, ROC-AUC  
- Matriz de confusão  
- Curva ROC e Precision-Recall  
- **Ajuste de cutoff de decisão** com base no custo dos erros


Exportação e Deploy
- Salvamento do modelo final (`joblib`)  
- Função de predição pronta para integração com API ou Streamlit  



O modelo foi calibrado para **minimizar FNs**, priorizando segurança operacional.

