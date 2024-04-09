# Implementação de Rede Neural para Classificação

Este projeto implementa uma rede neural para classificação usando o conjunto de dados `sementes.csv`. A rede neural é construída utilizando a biblioteca PyTorch e é treinada para prever a espécie de sementes com base em características específicas.

## Bibliotecas Utilizadas

- **pandas**: Utilizada para manipulação de dados em formato tabular.
- **torch**: Utilizada para implementação da rede neural.
- **torch.nn**: Utilizada para definição de módulos de rede neural.
- **torch.nn.functional**: Utilizada para funções de ativação e outros utilitários.
- **sklearn.model_selection**: Utilizada para dividir os dados em conjuntos de treinamento e teste.

## Carregamento dos Dados

O conjunto de dados `sementes.csv` é carregado utilizando a função `pd.read_csv()`. Os dados são armazenados em um dataframe chamado `dados`.

## Pré-processamento dos Dados

- A coluna "Espécie" é removida do dataframe `dados` e armazenada separadamente como `y`.
- As variáveis de entrada (X) e o alvo de identificação (y) são convertidos em tensores do PyTorch.

## Definição do Modelo de Rede Neural

- Uma classe `Modelo` é definida para representar a rede neural.
- A classe herda da classe `nn.Module` do PyTorch.
- O método `__init__()` define a arquitetura da rede neural, incluindo o número de neurônios em cada camada.
- O método `forward()` define o fluxo de dados através da rede neural.

## Treinamento do Modelo

- Os dados são divididos em conjuntos de treinamento e teste usando a função `train_test_split()`.
- A função de perda `CrossEntropyLoss()` é utilizada para avaliar o erro do modelo.
- O otimizador `Adam()` é utilizado para atualizar os parâmetros da rede neural.
- Um loop de treinamento é executado por um número especificado de épocas.
- Dentro do loop, o modelo é treinado em cada exemplo do conjunto de treinamento, o erro é calculado e os parâmetros da rede neural são atualizados.

## Avaliação do Modelo

- As previsões do modelo são feitas para o conjunto de teste.
- A precisão do modelo é calculada e exibida em um dataframe.
