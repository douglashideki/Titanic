# Titanic
Repositório com arquivos da **[competição do Kaggle sobre o famoso conjunto de dados do Titanic.](https://www.kaggle.com/c/titanic)**

O histórico dos resultados é mostrado abaixo e pode ser obtido no Kaggle: 
<img src='https://github.com/douglashideki/Titanic/blob/main/img/resultados_titanic.png'/>

---
## [Parte 1: Primeiro modelo]()
- Nesse etapa **fizemos apenas o básico para conseguir verificar qual seria o resultado** *sem fazer nenhum tratamento nem engenharia dos dados*
- Foi visualizado um resumo da base utilizando o [ydata-profiling](https://github.com/ydataai/ydata-profiling), **biblioteca capaz de gerar com poucas linhas toda a descrição do nosso dataset**
- Também eliminamos colunas com **elevada cardinalidade**, tratamos **valores vazios** utilizando a média e a moda das variáveis e eliminamos todas as **colunas de texto**
- Criamos os modelos utilizando 3 algoritmos: **Árvore de Classificação, KNN e Regressão Logística** e avaliamos esses modelos utilizando a acurácia e a matriz de confusão
- O ***score público retornado pelo Kaggle foi: 0,66746***
