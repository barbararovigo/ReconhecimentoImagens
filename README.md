# Reconhecimento de Imagens

Este trabalho refere-se ao trabalho final da disciplina: Aprendizado de Máquina II - Aprendizado Não Supervisionado, do curso de Especialização em Data Science, da FURB - Universidade Regional de Blumenau. O objetivo é aplicar a Análise de Componentes Principais (ACP) ou Principal Component Analysis (PCA) para o reconhecimento de imagens, neste caso, faces humanas.

Neste repositório temos:
  - Uma pasta com o nome  **ORL2**, com 410 imagens, de 70 x 80 pixels, 8 bits, sendo 10 imagens de cada pessoa com diferentes expressões faciais. As imagens estão organizadas de forma sequencial e seu nome descreve seu id e label. Ex: imagem 20_2.jpg: 20 refere-se ao id e 2 o seu label. Desta forma, o label 2 possui 10 ids que correspondem as 10 fotos da pessoa 2. 
  - Arquivo fonte **Recimages.ipynb** implementado através da ferramenta online _https://colab.research.google.com/_. O link direto no colab é:https://colab.research.google.com/drive/1iQHI16nmkksi2PoUa5FME4D5jYR09vXW?usp=sharing
  
Objetivos do trabalho:
  - Separar cada uma das 10 imagens em: 7 imagens para treino e 3 imagens para teste, ou seja, 70% das imagens serão usadas para treinar o algoritmo e 30% para testar se o mesmo reconhece aquela face (as imagens tanto de treino quanto de testes devem ser sorteadas aleatoriamente).
  - Foi utilizada a linguagem Python, porém foi optado em realizar os cálculos passo a passo. Em algumas etapas foi utilizado o OPENCV.
  - A pasta ORL2 foi adicionada ao diretório raiz do Google Drive, e no colab foi optado por MontarDrive
  
  
  

  

