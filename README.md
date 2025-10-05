1 - Objetivos

Detectar falhas logísticas e operacionais com base em variáveis de sensores e histórico de eventos.

Comparar o desempenho de diferentes configurações da Regressão Logística Regularizada.

Aplicar técnicas de balanceamento (SMOTE) para lidar com a desproporção entre classes.

Gerar indicadores de desempenho (AUC, precisão, recall e curva ROC).

Criar uma base sólida para aplicações de manutenção preditiva e análise de risco operacional.


2 - Tecnologias Utilizadas

Python 3.10+

Pandas e NumPy — manipulação e transformação dos dados

Matplotlib e Seaborn — visualização exploratória

Scikit-learn — modelagem preditiva e avaliação de métricas

Imbalanced-learn (SMOTE) — tratamento de classes desbalanceadas

Lifelines (opcional) — análises de sobrevivência (falhas ao longo do tempo)

Jupyter Notebook — ambiente de execução e documentação

3 - Metodologia (Modelagem Estatística e Machine Learning)
3.1 - Etapa de Preparação

Limpeza dos dados e padronização de colunas.

Identificação da variável-alvo (Machine_failure).

Tratamento de valores ausentes com SimpleImputer.

Codificação de variáveis categóricas com OneHotEncoder.

Escalonamento dos atributos numéricos com StandardScaler.

3.2 - Balanceamento de Classes

Aplicação do SMOTE (Synthetic Minority Over-sampling Technique) para aumentar a representatividade da classe minoritária e evitar viés do modelo.

3.3 - Modelagem Preditiva

Construção de um Pipeline híbrido (ImbPipeline) com pré-processamento e modelo final.

Treinamento de uma Regressão Logística Regularizada (L1 e L2).

Avaliação com Validação Cruzada Estratificada (StratifiedKFold) e busca de hiperparâmetros com GridSearchCV.

3.4 - Avaliação de Desempenho

Curva ROC e AUC (área sob a curva).

Precision-Recall Curve e Average Precision Score.

Relatório de Classificação (precisão, recall, F1-score).

Curvas de calibração para verificar a confiança das previsões probabilísticas.

4 - Resultados e Conclusões

O modelo de Regressão Logística apresentou bom desempenho preditivo, com AUC-ROC acima de 0.80 em validação cruzada.

O uso do SMOTE reduziu o viés contra a classe minoritária e melhorou o equilíbrio entre recall e precisão.

As curvas de calibração indicaram previsões probabilísticas bem ajustadas.

A metodologia proposta é aplicável a cenários de prevenção de falhas operacionais, manutenção preditiva e otimização logística.


Ana Paula Vanderley
*  Cientista de Dados | Analista de Dados Pleno
*  Foco em modelagem estatística, machine learning e previsão de eventos operacionais.
*   inkedIn  https://www.linkedin.com/in/apvanderley/
