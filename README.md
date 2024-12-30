# Analisador de Sentimentos em Comentários de Filmes

Este repositório contém um *notebook* em Python que demonstra o processo completo de análise de sentimentos de comentários de filmes, utilizando a base de dados [IMDB](https://keras.io/api/datasets/imdb/) e uma arquitetura de rede neural desenvolvida com [TensorFlow/Keras](https://www.tensorflow.org/). 

## Visão Geral

- **Pré-processamento e Tokenização**:  
  - Converte o texto para letras minúsculas.  
  - Remove pontuações e caracteres especiais.  
  - Transforma cada palavra em um índice numérico (token).

- **Codificação**:  
  - Atribui índices numéricos a cada palavra com base em um dicionário (*word_index*).  
  - Aplica *padding* para padronizar o comprimento das sequências de palavras.

- **Construção do Modelo**:  
  - Camada de *Embedding* para representar semanticamente as palavras.  
  - Camadas *Conv1D* e *MaxPooling* para extração de características em sequência.  
  - Camadas densas para a classificação binária (sentimento **positivo** ou **negativo**).

- **Treinamento e Avaliação**:  
  - Uso de métricas como *binary_accuracy* para medir a performance.  
  - *Confusion Matrix* para verificar distribuição de acertos e erros.  
  - *Callbacks* como *ModelCheckpoint* e *EarlyStopping* para otimização do treinamento.

- **Predição de Novos Comentários**:  
  - Funções para pré-processar, codificar e classificar textos inseridos pelo usuário em linha de comando.  
  - Retorna a probabilidade de o comentário ser **positivo** ou **negativo**.
