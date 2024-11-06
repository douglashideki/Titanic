# Titanic
Repositório com os arquivos da **[competição do Kaggle sobre o famoso conjunto de dados do Titanic.](https://www.kaggle.com/c/titanic)**

O histórico dos resultados é mostrado abaixo e pode ser obtido no Kaggle:

<img src='https://github.com/douglashideki/Titanic/blob/main/img/resultados_titanic.png'/>

---
## [Parte 1: Primeiro modelo](https://github.com/douglashideki/Titanic/blob/main/Titanic%20-%20Parte%201/Titanic%20-%20Parte%201.ipynb)
- Foi realizada uma análise preliminar da base de dados com tratamentos simples para avaliar o desempenho do modelo em um conjunto básico, estabelecendo uma linha de base para comparações e otimizações futuras.
- Gerou-se um relatório usando a biblioteca ydata_profiling, que fornece uma análise exploratória rápida e resumida, facilitando a compreensão das características dos dados e apoiando decisões para etapas posteriores.
- Tratamento dos **valores nulos**
  - Utilizado a **mediana das variáveis**.
  - Também foram feitas **pesquisas na internet** para preencher alguns valores nulos.
- Colunas com **elevada cardinalidade** ou **muitos valores nulos** foram **removidas**.
- **Transformação** das **colunas categóricas** ('Sex' e 'Embarked') **em numéricas**
  - Foram utilizados as técnicas **"get_dummies()"** e **OneHotEncoder**, que cria uma nova coluna para cada um dos rótulos da coluna original.
- Foram criados **três modelos** utilizando os algoritmos **'DecisionTreeClassifier', 'KNN' e 'LogisticRegression'.**
- Os modelos foram **avaliados** utilizando a **acurácia e a matriz de confusão.**
- **O score retornado pelo Kaggle foi: 0.76076** (utilizando o modelo de Regressão Logística).
