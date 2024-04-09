# Implementação de Rede Neural para Classificação

Este projeto implementa uma rede neural para classificação usando o conjunto de dados `sementes.csv`. Uma nova construção neural utilizando uma biblioteca PyTorch e é treinada para prever a espécie de sementes com base em características específicas.

## Bibliotecas Utilizadas

- **pandas**: Utilizada para manipulação de dados em formato tabular.
- **tocha**: Utilizada para implementação da rede neural.
- **tocha.nn**: Utilizada para definição de módulos de rede neural.
- **torch.nn.funcional**: Utilizada para funções de ativação e outros utilitários.
- **sklearn.model_selection**: Utilizada para dividir os dados em conjunto de treinamento e teste.

## Carregamento dos Dados

O conjunto de dados `sementes.csv` é carregado utilizando uma diversidade `pd.read_csv()`. . . . Os dados são armazenados em um dataframe chamado `dado`.

## Pré-processamento dos Dados

- Uma coluna "Espécie" é removida do dataframe `dado` e armazenada separamente como `y`.
- Como variáveis de entrada (X) e o alto de identificação (y) são convertidos em tensores do PyTorch.

## Definição do Modelo de Rede Neural

- Uma classe `Modelo` é definida para representar um novo neural.
- Uma classe herda da classe `módulo nn` faça PyTorch.
- Ó método `__init__()` defina uma arquitetura da rede neural, incluindo o número de neurônios em cada camada.
- Ó método `avançar()` defina o fluxo de dados através da rede neural.

## Treinamento do Modelo

- Os dados são divididos em conjuntos de treinamento e teste usando uma função `trem_test_split()`.
- A função de permanente `CrossEntropyPerda()` é utilizada para avaliar o erro do modelo.
- Ó otimizador `Adão()` é utilizado para atualizar os parâmetros da rede neural.
- Um loop de treinamento é executado por um número específico de épocas.
- Dentro do loop, o modelo é treinado em cada exemplo do conjunto de treinamento, o erro é calculado e os parâmetros da rede neural são atualizados.

## Avaliação do Modelo

- Como previsões do modelo são feitas para o conjunto de teste.
- Uma precisão do modelo é calculada e exibida em um dataframe.
