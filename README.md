# Classificador Rede Neural
### Descrição
Treinando um algoritmo de rede neural para classificação, aplicando em uma base de dados para classificar registros e compartilhar os resultados(Censo de 1994 - EUA).

O objetivo é prever se uma pessoa possui renda anual <= ou > 50 mil dólares por ano.

**Percentual mínimo a ser batido** -> Base Line Classifier = 0.7559 (ZeroR).

### Resultados - Validação Cruzada - StratifiedKFold

**Precisão** | **Pré-Processamentos** | **Desvio Padrão**
| :------: | :------: | :------: |
0.6246 | LabelEncoder | 0.2492
0.7655 | OneHotEncoder | 0.0847
**0.8465** | **LabelEncoder + StandardScaler** | **0.0079**
0.8328 | OneHotEncoder + StandardScaler | 0.0062
0.8316 | LabelEnconder + OneHotEncoder + StandardScaler | 0.0039

### Matriz de Confusão (Média):
**x** | 0 | 1
| :------: | :------: | :------: |
0 | **2223.2** | 248.8
1 | 299.4 | **484.7**

A Matriz na tabela acima é formada pela média de todas as matrizes geradas ao longo de 10 execuções usando pré-processamentos LabelEnconder + StandardScaler.

A diagonal principal (em negrito) destaca os registros classificados corretamente.

### Especificações dos parametros usados:
- MLPClassifier(verbose= True, max_iter= 1000, tol= 0.000010)

### Bibliotecas usadas:
- Pandas
- Sklearn
- Numpy

### Ferramentas Usadas:
- Anaconda
- Spyder

### Fonte da Base de Dados: 
- Dua, D. and Graff, C. (2019). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

### Como usar:
1. Faça o download do classificador já treinado dispoível neste mesmo repositório [aqui](https://github.com/juliomrodrigues/Classificador-Rede-Neural/blob/main/classificador_rede_neural.sav).
2. Abra o arquivo.py que deseja usar o classificador ou então crie um novo.
3. Execute o código abaixo para fazer a importação:
~~~~python
import pickle
classificador = pickle.load(open('classificador_rede_neural.sav', 'rb'))

~~~~~
4. Pronto, agora o classficador está pronto para ser usado. 
5. Se desejar treinar um novo classificador, faça o download do arquivo de treinamento e execute novas combinações de pré-processamentos e parâmetros [aqui](https://github.com/juliomrodrigues/Classificador-Rede-Neural/blob/main/treinamento_rede_neural.py).

### Outros Classificadores
- [Naive Bayes](https://github.com/juliomrodrigues/Classificador-Naive-Bayes)
- [Árvore de Decisão](https://github.com/juliomrodrigues/Arvore-de-Decisao)
- [Random Forest](https://github.com/juliomrodrigues/Random-Forest-Classificador)
- [Aprendizagem por Regras](https://github.com/juliomrodrigues/Classificador-Regras)
- [Aprendizagem por Instâncias(KNN)](https://github.com/juliomrodrigues/Classificador-KNN)
- [Regressão Logística](https://github.com/juliomrodrigues/Regressao-Logistica-Classificador)
- [SVM](https://github.com/juliomrodrigues/Classificador-SVM)
