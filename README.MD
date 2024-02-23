# Classificação de Urso

## Sobre o projeto

O atual projeto representa uma iniciativa de aprendizado de máquina cujo propósito é classificar distintas espécies de ursos por meio da análise de imagens. Desenvolvido em Python, utiliza as bibliotecas TensorFlow e Keras para a implementação do aprendizado de máquina.

O principal propósito deste projeto é desenvolver um modelo capaz de classificar imagens de ursos com alta precisão, categorizando-os em diferentes grupos, a saber:

- Ursos Negros (abrangendo ursos negros americanos e asiáticos)
- Ursos Pardos
- Ursos Polares
- Ursos Pandas
- Ursos do Sol
- Ursos Preguiça
- Ursos de Óculos
- Ursos de Pelúcia

## Construção do dataset

Como ponto de partida, foi utilizado o conjunto de dados disponibilizado no Kaggle:

![Dataset Kaggle](/imagens/kaggle-dataset.png)

O conjunto de dados mencionado anteriormente incluía apenas 5 classes. Para enriquecer o conjunto, utilizei a API de download de imagens do Bing para adquirir mais 3 espécies, incorporando assim mais imagens e expandindo as classes já existentes no conjunto de dados original, chegando assim a 724 imagens em todo o conjunto.

# Resultados
## Primeira Versão

Dos diversos resultados obtidos, os mais significativos foram alcançados ao utilizar transferência de aprendizado com o modelo VGG16 da biblioteca Keras. Além disso, foram utilizados outros mecanismos, sem a utilização de um modelo pré treinado foi alcançado uma precisão de 18% e utilizando transferência de aprendizado com o modelo resnet50 45% de precisão. Durante o treinamento com as 8 classes mencionadas, o modelo atingiu uma precisão de 100% nos dados de treinamento e 77% nos dados de validação. Ao analisar mais detalhadamente, observamos que o modelo enfrentou desafios significativos na identificação de Ursos Negros.

![Dataset Kaggle](/imagens/matriz-confusao.jpeg)

Posteriormente, realizei uma tentativa de treinamento excluindo a classe dos ursos negros, o que resultou em uma precisão de 99% nos dados de treinamento e 90% nos dados de validação. Esse desempenho pode ser atribuído à semelhança entre ursos negros, ursos preguiças e ursos do sol. Vale ressaltar que a qualidade do conjunto de dados também pode ser questionada ou aprimorada para impactar os resultados.

## Segunda Versão

Considerando esses aspectos, incorporei 617 novas imagens ao conjunto de dados para enriquecimento, resultando em um aumento significativo na diversidade de dados. Com a inclusão desses novos dados de treinamento, consegui atingir uma precisão notável de 100% nos dados de treinamento e 86% nos dados de validação. No entanto, persiste o desafio na identificação de Ursos Negros e Ursos de Óculos, devido à sua semelhança com outras espécies. Este é um ponto a ser abordado para aprimorar ainda mais a eficácia do modelo.

![Dataset Kaggle](/imagens/matriz-confusao-2.jpeg)

## Terceira Versão

Incluí mais 143 imagens abrangendo ursos negros, pardos e polares. Ao utilizar o novo conjunto de dados, diversos modelos de transferência de aprendizado foram testados, e destaca-se o excepcional desempenho do modelo InceptionV3, atingindo uma impressionante precisão de 99% na fase de treinamento e 94% durante a fase de validação.

![Dataset Kaggle](/imagens/matriz-confusao-3.jpeg)

## Versão Pytorch

Utilizando a biblioteca "fastbook", que simplifica significativamente a implementação do PyTorch, em conjunto com o modelo ResNet18, alcancei uma precisão impressionante de 98%.

![Dataset Kaggle](/imagens/matriz-pytorch.jpeg)

A biblioteca "fastbook" é uma parte integrante do ecossistema "fastai" e foi desenvolvida para tornar mais acessível a utilização do PyTorch, proporcionando uma abordagem mais simplificada e orientada para tarefas específicas, como aprendizado de máquina e visão computacional. 