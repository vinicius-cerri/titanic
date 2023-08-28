# Projeto Titanic (EM PRODUÇÃO)
Projeto de Ciência de Dados criado para a **[Competição sobre o Desastre do Titanic](https://www.kaggle.com/competitions/titanic/overview)**

## Etapa 1: Importação de Bibliotecas e Base de Dados
- Nesse etapa realizei a **Importação de Todas as Bibliotecas** que foram utilizadas no código, assim como as **Bases de Dados** que serviram para treinar e testar o modelo
  - As Principais Bibliotecas usadas foram: **Pandas**, para a importação e posteriormente para os tratamentos dos dados, e **Scikit-Learn**, para toda a parte que envolve o Modelo de Inteligência Artificial
  - Divisão das Bases de Dados: A Base de Dados do arquivo train.csv foi a Base usada para fazer todos os tratamentos, treinos e testes no Modelo. Enquanto isso, a Base de Dados do arquivo test.csv foi a Base utilizada para fazer as previsões e submeter ao Kaggle, para Avaliação dos Resultados.

## Etapa 2: Tratar as Bases
- Na segunda etapa o foco principal foi tratar todas as colunas do nosso modelo
  - Se quiser **saber mais sobre tratamento de variáveis de texto**, você pode **conferir [esse artigo que eu escrevi no Medium](https://medium.com/@llucaslleall/tratando-vari%C3%A1veis-categ%C3%B3ricas-em-projetos-de-ci%C3%AAncia-de-dados-834dcc5bb636)**
  - Para fazer esse tratamento, utilizamos **lambda function e OneHotEncoder**
- Utilizamos os mesmos modelos vistos anteriormente
- O **score público retornado pelo Kaggle foi: 0,76555**

## [Etapa 3: Aprofundando no negócio e melhorando os tratamentos dos dados](https://github.com/lucaslealx/Titanic/blob/main/Parte3.ipynb)
- Na terceira etapa o grande objetivo era **entender melhor os dados** para **fazer um melhor tratamento** e tentar melhorar o resultado obtido anteriormente.
- Então fizemos:
  - O **ajuste na escala dos dados para as colunas Age e Fare**
  - Entendemos melhor as colunas **SibSp** (nº de irmãos/cônjuges a bordo do Titanic) e **Parch** (nº de pais/filhos a bordo do Titanic) e criamos **2 novas colunas: total de familiares a bordo do navio e se o passageiro estava sozinho ou não**
  - Para finalizar, analisamos a **correlação de todas as variáveis** para selecionar aquelas que mais faziam sentido para o modelo
- Utilizamos os mesmos modelos vistos anteriormente
- O **score público retornado pelo Kaggle foi: 0,77033**

## [Etapa 4: Selecionando outros algoritmos para fazer a previsão](https://github.com/lucaslealx/Titanic/blob/main/Parte4.ipynb)
- Nessa etapa vamos manter todas as colunas (incluindo SibSp e Parch) e utilizar novos algoritmos para verificar o resultado do modelo
- Os algoritmos que vamos utilizar nessa etapa são a **Regressão Logística** (vamos manter pois foi o com melhores resultados nas etapas anteriores), **RandomForest e MLPCLassifier (Redes Neurais)**
- O MLPClassifier (um algoritmo de Redes Neurais) obteve a maior acurácia nos dados de validação entre todos os modelos vistos até agora, porém ao usar esse modelo nos dados de teste (que faremos a submissão) o resultado foi pior que na etapa 3, mostrando que **provavelmente tivemos um overfitting do nosso modelo**
- O **score público retornado pelo Kaggle foi: 0,69856**

## [Etapa 5: Utilizando o GridSearchCV e determinando os melhores parâmetros](https://github.com/lucaslealx/Titanic/blob/main/Parte5.ipynb)
- Agora utilizamos o GridSearchCV para determinar os melhores parâmetros para os 3 modelos que utilizamos na etapa anterior
- Nesse caso, o modelo escolhido foi aquele utilizando o RandomForest e o resultado melhorou consideravalmente em relação a etapa 4 e foi melhor que na etapa 3
- O **score público retornado pelo Kaggle foi: 0,78229**
