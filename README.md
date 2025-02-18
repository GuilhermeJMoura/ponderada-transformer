# ponderada-transformer - Guilherme Jesus Moura

## Pontos positivos:
- **Código Modular:** Um dos pontos positivos é que o código apresentado no tutorial é bem modular e reutilizável, separando bem o que é Encoder, Decoder, Attention e Positional Encoding 
- **Implementação de Multi-Head Attention:** Outro ponto positivo foi a implementação do multi-head attention, permitindo que o modelo capture diferentes aspectos do contexto.
- **Exemplo prático utilizando dataset real:** Outra coisa muito boa sobre a implementação é que ele utilizou um dataset real de tradução (do português para o inglês), ajudando a ver na prática como o modelo se comportaria em produção.

## Pontos negativos:
- **Tutorial desatualizado:** Um ponto negativo é que o tutorial estava um pouco desatualizo. Ao tentar rodar as funções, em alguns trechos de código aconteciam erros que necessitavam de ajustes pois a biblioteca utilizada foi atualizada.
- **Tempo de treinamento demorado:** O tempo de treinamento para esse modelo Transformer também foi um ponto negativo, rodando apenas 10 épocas em uma GPU T4 o modelo demorou 18 minutos, o que é um tempo considerável pela pouca quantidade de épocas.
- **Não se dá bem com palavras em inglês no meio do texto em português:** Fiz o teste com a frase "eu gosto de jogar blackjack postando nos stories" e ele me retornou "i like to play blackling on the editor to take us out of the sieria.". O que significa que quando há palavras em inglês no meio do texto em português, o modelo tem uma leve dificuldade em não tentar traduzir essa palavra também.

# Comparação Tempo Treinamento:
Para ficar justa a comparação, treinei o modelo de Transformer utilizando a GPU T4 do Colab e a CPU, ambos por 1 época e usando a mesma quantidade de memória RAM, os resultados obtidos foram os seguintes:

|   | CPU | GPU      |
|-------|-------|------------|
| Treinamento   | 78 minutos    | 2 minutos  |

Ou seja, a GPU é 3800% mais rápida no treinamento do modelo de Transformer do que a CPU.
Em um outro teste, o modelo foi treinado por 15 épocas na GPU e demorou 26 minutos. Se fossemos treinar essas mesmas 15 épocas na CPU, o modelo demoraria 1170 minutos para ser tereinado, ou 19 horas e meia.