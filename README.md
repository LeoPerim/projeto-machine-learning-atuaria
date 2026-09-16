# projeto-machine-learning-atuaria
  Este projeto tem como objetivo realizar processamento, análise e modelagem de imagens de vulcões, utilizando técnicas de visão computacional, redução de dimensionalidade e classificação supervisionada. A proposta central é explorar como diferentes técnicas de extração de características e pré-processamento influenciam o desempenho de modelos de Machine Learning na identificação de padrões em imagens vulcânicas.

***Objetivos***

- Realizar pré-processamento de imagens vulcânicas

- Aplicar técnicas de extração de características

- Reduzir dimensionalidade dos dados

- Comparar modelos de classificação

- Avaliar desempenho com métricas adequadas 

- Analisar impacto de transformações na performance

**Perspectiva de Negócio e Análise**

Datasets de imagens possuem naturalmente uma quantidade muito elevada de variáveis e podem apresentar desafios como:

- Overfitting
- Sensibilidade a ruídos
- Alto custo computacional

O projeto busca construir um pipeline de classificação robusto e com boa capacidade de generalização, simulando etapas encontradas em projetos reais de Data Science. Uma decisão importante foi priorizar o F2-score em vez de utilizar apenas a acurácia. O F2-score atribui maior importância ao recall, sendo útil em situações nas quais deixar de identificar corretamente uma observação relevante (falso negativo) pode ser mais prejudicial do que gerar um falso positivo.

**Metodologia**

**1 - Pré-processamento dos Dados**

As imagens passaram por diferentes etapas de preparação:

Redimensionamento e reorganização das imagens
Conversão para float32
Normalização dos valores para o intervalo [0, 1]
Detecção de bordas utilizando o filtro de Sobel
Transformação das imagens em vetores de características

Essa etapa teve como objetivo preparar os dados para os modelos e explorar formas de destacar informações estruturais presentes nas imagens.

**2 - Redução de Dimensionalidade**

Como cada imagem pode possuir milhares de pixels, trabalhar diretamente com todas as variáveis pode aumentar significativamente a complexidade computacional. Para lidar com esse problema, foi utilizado o PCA (Principal Component Analysis). O PCA foi utilizado com o objetivo de:

Reduzir a dimensionalidade dos dados
Diminuir o custo computacional
Reduzir a quantidade de informação redundante
Facilitar a aplicação dos modelos de Machine Learning
Manter uma parcela relevante da variância presente nos dados

**3 - Estratégia de Seleção dos Modelos**

Foram avaliados diferentes algoritmos de classificação:

Regressão Logística
Support Vector Machine (SVM) — Kernel Linear
Support Vector Machine (SVM) — Kernel RBF
K-Nearest Neighbors (KNN)
Naive Bayes

Os modelos foram comparados utilizando técnicas de validação e ajuste de hiperparâmetros. O GridSearchCV foi utilizado para buscar combinações de hiperparâmetros e avaliar o desempenho dos modelos por meio de validação cruzada.

**Avaliação dos Modelos**

Os modelos foram avaliados considerando diferentes aspectos, incluindo:

F2-score
Acurácia
Capacidade de generalização
Desempenho durante a validação cruzada
Impacto das diferentes técnicas de pré-processamento

A escolha do modelo final considerou não apenas seu desempenho, mas também a robustez e adequação ao problema de classificação.

**Principais Aprendizados**

O desenvolvimento deste projeto permitiu aprofundar conhecimentos em:

Engenharia de atributos aplicada a imagens
Técnicas de pré-processamento
Redução de dimensionalidade com PCA
Seleção de métricas de avaliação
Comparação de modelos de Machine Learning
Validação cruzada
Otimização de hiperparâmetros
Análise do trade-off entre viés e variância
Estruturação de pipelines de Machine Learning
Avaliação da capacidade de generalização dos modelos

Além da implementação dos algoritmos, o projeto buscou desenvolver uma abordagem baseada em análise crítica dos resultados, entendendo não apenas qual modelo apresenta determinado desempenho, mas também os motivos e limitações por trás desse resultado.
