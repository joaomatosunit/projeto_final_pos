# Projeto Final Pós Graduação
Projeto Final do curso de Pós Graduação Ciência de Dados e Inteligência Artificial\
Universidade Tiradentes (UNIT)

## Alunos
Ana Paula dos Reis Barreto\
João Antonio Silveira Matos

## Tema
Enade

---

📌 **Sobre o projeto**\
Este repositório reúne os materiais, códigos-fonte, dados, experimentos e documentação desenvolvidos durante a elaboração do projeto final da pós-graduação.

🎯 **Objetivos**\
Desenvolver um modelo preditivo utilizando dados históricos do ENADE (Exame Nacional de Desempenho dos Estudantes), explorando características dos estudantes e dos cursos para classificar o desempenho acadêmico em três categorias:\

Desempenho insatisfatório;\
Desempenho adequado;\
Desempenho elevado.

🛢️**Base de dados**\
Os dados utilizados são provenientes do conjunto histórico do ENADE, disponibilizado no Kaggle:

[ENADE 2008–2018 – Kaggle](https://www.kaggle.com/datasets/expeditojunior/enade20082018)

A base original possui aproximadamente 3,7 milhões de registros e informações relacionadas aos estudantes, cursos, instituições de ensino, localização geográfica e resultados das avaliações.

Dados originais:
[Microdados do Enade - Inep](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/enade)

## Desenvolvimento do projeto

O principal desenvolvimento está concentrado no notebook:


[modelo_preditivo_machine_learning.ipynb](notebooks/modelo_preditivo_machine_learning.ipynb)

O notebook contempla as seguintes etapas:

### 1. Importação e preparação dos dados
Download da base de dados disponibilizada no Kaggle;\
Leitura dos dados no formato RDS, utilizando integração entre Python e R;\
Conversão dos dados para DataFrame com Pandas;\
Inspeção da estrutura e análise estatística inicial.

### 2. Análise exploratória
Análise das variáveis disponíveis;\
Investigação das características dos dados;\
Análise de correlação entre variáveis numéricas;\
Identificação de informações relevantes para a construção do modelo.

### 3. Engenharia e preparação das variáveis
Criação da variável de classificação do desempenho a partir das notas gerais do ENADE;\
Seleção das variáveis preditoras;\
Tratamento de valores ausentes;\
Conversão de variáveis categóricas utilizando One-Hot Encoding;\
Separação dos dados em conjuntos de treinamento e teste;\
Padronização das variáveis numéricas.

### 4. Balanceamento das classes
Como a distribuição original das classificações apresenta diferenças significativas entre as categorias de desempenho, foi aplicada a técnica de subamostragem (Downsampling) nas classes majoritárias.\
O objetivo é proporcionar maior equilíbrio entre as categorias utilizadas no treinamento dos modelos.

### 5. Construção dos modelos de Machine Learning
Foram implementados e avaliados diferentes algoritmos de classificação:\
Decision Tree (Árvore de Decisão): modelo baseado em regras e divisões sucessivas das características dos dados.\
K-Nearest Neighbors (KNN): algoritmo que realiza classificações considerando a proximidade entre as observações.\
Naive Bayes (GaussianNB): classificador probabilístico baseado no teorema de Bayes.

### 6. Avaliação dos modelos
A avaliação considera principalmente:



