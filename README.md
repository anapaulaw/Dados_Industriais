Este projeto tem como objetivo desenvolver modelos de previsão de falhas em máquinas industriais utilizando técnicas de Machine Learning. A base de dados utilizada contém informações de sensores e indicadores operacionais simulados, mas representando cenários reais de produção industrial.

Aplicação de  modelos de classificação binária para identificar a probabilidade de falha em equipamentos, permitindo antecipar manutenções e reduzir paradas não planejadas, contribuindo para maior eficiência e redução de custos no setor industrial.

__________________________________________________________________________________________________________________________________________________________________________________

PIPELINE

*  Carregamento e análise da base de dados

*  Identificação do tamanho, tipos de variáveis e presença de dados ausentes.

*  Definição do target: Machine failure.

*  Pré-processamento

*  Tratamento de dados numéricos (imputação de medianas e escalonamento).

*  Tratamento de dados categóricos (imputação do valor mais frequente e codificação one-hot).

*  Divisão treino-teste

*  Separação da base em 75% treino e 25% teste com estratificação.

*  Balanceamento de classes

*  Aplicação de undersampling para equilibrar a proporção entre falhas e não-falhas.

  ____________________________________________________________________________________________________________________________________________________________________

TESTE DE DUAS ESTRATEGIAS

*  Modelo A: Regressão logística com class_weight='balanced'.

*  Modelo B: Regressão logística com undersampling + regularização L1.

*  Treinamento e avaliação dos modelos

  __________________________________________________________________________________________________________________________________________________________________

MÉTRICAS

*  Acurácia, F1-score, Precision, Recall.

*  ROC AUC e Precision-Recall Curve.

*  Ajuste de threshold para maximizar F1-score.

*  Visualização de matriz de confusão.

*  Validação cruzada

*  Avaliação da robustez dos modelos com Stratified K-Fold (5 folds).

*  Comparação de desempenho entre os dois modelos.

  ________________________________________________________________________________________________________________________________________________________________________________

RESULTADOS

O Modelo A (class_weight) e o Modelo B (undersample + L1) apresentaram desempenhos comparáveis em ROC AUC e métricas de classificação.

A análise de threshold no Modelo B permitiu otimizar o F1-score, mostrando que ajustes simples podem impactar significativamente a performance.

As curvas ROC e Precision-Recall evidenciam a capacidade de cada modelo em identificar corretamente as falhas, mesmo com uma base de dados pequena.

________________________________________________________________________________________________________________________________________________________________________________


A previsão de falhas em equipamentos é crucial no setor industrial, pois permite: Reduzir o tempo de inatividade não planejado, Planejar manutenção preventiva de forma mais eficiente
,Reduzir custos operacionais e aumentar a produtividade.

Mesmo utilizando uma base pequena e simulada, este estudo mostra como técnicas de machine learning podem ser aplicadas a dados reais de sensores industriais, servindo como prova de conceito para futuras implementações em escala real. O projeto demonstra que, mesmo com dados limitados, é possível construir pipelines robustos de classificação, testar estratégias de balanceamento e regularização, e gerar insights valiosos para tomada de decisão industrial.


