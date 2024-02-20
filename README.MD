# Classificação de Urso

# Sobre o projeto

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

# Construção do dataset

Como ponto de partida, utilizamos o conjunto de dados disponibilizado no Kaggle:

![Dataset Kaggle](/imagens/kaggle-dataset.png)

O conjunto de dados mencionado anteriormente incluía apenas 5 classes. Para enriquecer o conjunto, utilizei a API de download de imagens do Bing para adquirir mais 3 espécies, incorporando assim mais imagens e expandindo as classes já existentes no conjunto de dados original.

# Resultados

Dos diversos resultados obtidos, os mais significativos foram alcançados ao utilizar o modelo pré-treinado VGG16 da biblioteca Keras. Durante o treinamento com as 8 classes mencionadas, o modelo atingiu uma precisão de 100% nos dados de treinamento e 77% nos dados de validação. Ao analsar mais detalhadamente, observamos que o modelo enfrentou desafios significativos na identificação de Ursos Negros.

![Dataset Kaggle](/imagens/matriz-confusao.jpeg)

Posteriormente, realizei uma tentativa de treinamento excluindo a classe dos ursos negros, o que resultou em uma precisão de 99% nos dados de treinamento e 90% nos dados de validação. Esse desempenho pode ser atribuído à semelhança entre ursos negros, ursos preguiças e ursos do sol. Vale ressaltar que a qualidade do conjunto de dados também pode ser questionada ou aprimorada para impactar os resultados.