# Titanic
Repositório com os arquivos da **[competição do Kaggle sobre o famoso conjunto de dados do Titanic.](https://www.kaggle.com/c/titanic)**

O histórico dos resultados é mostrado abaixo e pode ser obtido no Kaggle:

<img src='[https://github.com/douglashideki/Titanic/blob/main/img/resultados_titanic.png](https://github.com/douglashideki/Titanic/blob/main/img/resultados_titanic.png)'/>




---
## [Parte 1: Primeiro modelo](https://github.com/douglashideki/Titanic/blob/main/Titanic%20-%20Parte%201/Titanic%20-%20Parte%201.ipynb)
- Foi realizada uma **análise preliminar** da **base de dados** com **tratamentos simples** para avaliar o desempenho do **modelo** em um conjunto básico, estabelecendo uma **linha de base** para comparações e otimizações futuras.  
- Gerou-se um **relatório** usando a biblioteca **ydata_profiling**, que fornece uma **análise exploratória** rápida e resumida, facilitando a compreensão das **características dos dados** e apoiando **decisões** para etapas posteriores.
- **Tratamento dos valores nulos**  
  - Utilizou-se a **mediana** das **variáveis**.  
  - Também foram feitas **pesquisas na internet** para preencher alguns **valores nulos**.  
- **Colunas com elevada cardinalidade** ou muitos **valores nulos** foram removidas.  
- **Transformação das colunas categóricas** ('**Sex**' e '**Embarked**') em **numéricas**.  
  - Foram utilizadas as técnicas "**get_dummies()**" e **OneHotEncoder**, que criam uma nova **coluna** para cada um dos **rótulos** da coluna original.  
- Foram criados três **modelos** utilizando os algoritmos '**DecisionTreeClassifier**', '**KNN**' e '**LogisticRegression**'.  
- Os modelos foram avaliados utilizando a **acurácia** e a **matriz de confusão**.  
- O **score** retornado pelo **Kaggle** foi: **0.76076** (utilizando o modelo de **Regressão Logística**).

## [Parte 2: Análise e Tratamentos mais Avançados](https://github.com/douglashideki/Titanic/blob/main/Titanic%20-%20Parte%202/Titanic%20-%20Parte%202.ipynb)
- Na **segunda parte** do projeto, foi realizada uma **análise exploratória** mais detalhada em cada coluna do **conjunto de dados**.  
- Inicialmente foi retirado o **título** pertencente a cada passageiro e então codificado com o **OneHotEncoder**.  
- Para a coluna '**Age**', foi criada uma **classificação** para as idades, sendo elas, **criança**, **adulto** e **idoso** e então codificado em **numérico**. Para realizar esta classificação, foi criada uma **função** e utilizado o método **.apply()** junto com o **lambda**.  
- Foi criada uma nova coluna "**Family**" que é a soma dos valores das colunas "**SibSp**" e "**Parch**".  
- A coluna "**Fare**" foi classificada em categorias, **gratuito**, **valor alto**, **médio** e **baixo**. Cada categoria foi então codificada para **numérica** e armazenada em uma nova coluna chamada "**Classe_Fare**".  
- Assim como na parte 1, foram criados três **modelos** utilizando os algoritmos '**DecisionTreeClassifier**', '**KNN**' e '**LogisticRegression**'.  
- O **score** retornado pelo **Kaggle** foi: **0.77033** (utilizando o modelo de **Regressão Logística**).

## [Parte 3: Modelo Final](https://github.com/douglashideki/Titanic/blob/main/Titanic%20-%20Parte%202/Titanic%20-%20Parte%202.ipynb)

- Na **terceira parte** do projeto, além do **LogisticRegression**, utilizamos outros **modelos** de Machine Learning mais **complexos**, como o **RandomForest**, **MLPClassifier** e **SVC**.
- Foi utilizado a técnica de **validação cruzada** com a finalidade de **avaliar** o desempenho dos modelos de maneira **mais precisa e robusta**.
- Também foi feito a **seleção de features** para escolher as **variáveis** ou atributos **mais relevantes** para o modelo e descartar aquelas que são **irrelevantes, redundantes ou ruidosas**.
  - Etapa importante para melhorar o **desempenho** e **performance** do modelo.
  - Na **seleção de features**, foi identificado que as colunas '**PassengerId**', '**Survived**', '**Embarked_Q**', '**Title_Others**' e '**Family**' tiveram **baixa pontuação** e poderiam ser removidas.
- Por fim, foi realizado o **GridSearchCV** para **ajustar os hiperparâmetros** dos modelos, realizando uma busca sistemática para encontrar a combinação ideal de parâmetros que **maximize o desempenho** do modelo e **previna overfitting**.
- O **score** retornado pelo **Kaggle** foi: **0.78468** (utilizando o modelo **MLPClassifier**).
