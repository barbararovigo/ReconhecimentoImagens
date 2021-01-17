# Reconhecimento de Imagens

Este trabalho refere-se ao trabalho final da disciplina: Aprendizado de Máquina II - Aprendizado Não Supervisionado, do curso de Especialização em Data Science, da FURB - Universidade Regional de Blumenau. O objetivo é aplicar a Análise de Componentes Principais (ACP) ou Principal Component Analysis (PCA) para o reconhecimento de imagens, neste caso, faces humanas.

Neste repositório temos:
  - Uma pasta com o nome  **ORL2**, com 410 imagens, de 70 x 80 pixels, 8 bits, sendo 10 imagens de cada pessoa com diferentes expressões faciais. As imagens estão organizadas de forma sequencial e seu nome descreve seu id e label. Ex: imagem 20_2.jpg: 20 refere-se ao id e 2 o seu label. Desta forma, o label 2 possui 10 ids que correspondem as 10 fotos da pessoa 2. 
  - Arquivo fonte **Recimages.ipynb** implementado através da ferramenta online _https://colab.research.google.com/_. O link direto no colab é:https://colab.research.google.com/drive/1iQHI16nmkksi2PoUa5FME4D5jYR09vXW?usp=sharing
  
Objetivos do trabalho:
  - Separar cada uma das 10 imagens em: 7 imagens para treino e 3 imagens para teste, ou seja, 70% das imagens serão usadas para treinar o algoritmo e 30% para testar se o mesmo reconhece aquela face (as imagens tanto de treino quanto de testes devem ser sorteadas aleatoriamente).
  - Foi utilizada a linguagem Python, porém foi optado em realizar os cálculos de reconhecimento passo a passo. Em algumas etapas foi utilizado o OPENCV.
  - A pasta ORL2 foi adicionada ao diretório raiz do Google Drive, e no colab, após abrir o arquivo **Recimages.ipynb**, selecionar a opção MontarDrive:
  
  ![image](https://user-images.githubusercontent.com/63163264/104856524-ef4b8a80-58f1-11eb-82bd-e8d3c733e97b.png)
  
  Desta forma, as imagens estarão acessíveis ao nosso programa
  
  - Após importar e separar as imagens em treino e teste, já com tamanho padrão de 80 x 80 pixels e em escala de cinza, obteve-se a imagem média, que é a imagem média de todas as imagens de treino.
  - Após calcular a imagem média, cada imagem de treino foi corrigida em relação a imagem média, para que nenhuma coluna possa influenciar indevidamente o valor das componentes principais. A esta matriz foi dado o nome de **imagem_diff** gerando uma matriz com estas diferenças em relação a imagem média. Cada coluna desta matriz representa uma imagem.
  - Com a matriz de diferenças, calcula-se a covariância, neste caso utilizando, a **imagem_diff transposta x imagem_diff**. Neste ponto, diferente de outros métodos onde a covariância seria calculada **imagem_diff x imagem_diff transposta**, segundo método explicado pelo professor, perde-se, porém não significativamente, a variância é mantida e elimina-se redundância. Veja um comparativo entre a quantidade de operações entre os dois métodos:
  
 ![image](https://user-images.githubusercontent.com/63163264/104857319-5a975b80-58f6-11eb-9777-bc301575432e.png)
   
  - Posteriormente calcula-se os autovalores e autovetores da matriz de covariância
  - Os autovetores, ordenados em ordem descrescente de autovalores, possuem as principais componentes que serão utilizadas para projetar as eigenfaces. O trabalho proposto vai avaliar a acurácia do modelo aplicando entre 10 e 20 componentes principais.
  - A acurácia será o total das imagens de teste reconhecidas corretamente, dividido pela quantidade total de imagens de teste, multiplicado por 100.
  
  Abaixo o resumo obtido por esta implementação:
  
  ![image](https://user-images.githubusercontent.com/63163264/104857913-62f19580-58fa-11eb-9346-a399d1d6ee3a.png)
  
