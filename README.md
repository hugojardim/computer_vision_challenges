# Desafios de Visão Computacional

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![Open3D](https://img.shields.io/badge/Open3D-4B9B7A.svg?style=flat)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8.svg?style=flat)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626.svg?style=flat&logo=Jupyter&logoColor=white)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hugojardim/computer_vision_challenges/blob/main/icp_challenge/pipeline.ipynb)

Este repositório contém soluções para desafios de Visão Computacional, com foco em processamento 3D e reconhecimento facial.

## 🎯 Desafios

Este projeto é composto por dois desafios principais:

1.  **Alinhamento de Nuvens de Pontos com ICP**: Estimativa de trajetória de um veículo (odometria) a partir do alinhamento sequencial de nuvens de pontos 3D do dataset KITTI.
2.  **Busca de Pessoas com Máscara**: Um sistema de Machine Learning para buscar e identificar pessoas pela imagem do rosto, mesmo quando estão usando máscaras de proteção.

---

### Desafio 1: Alinhamento de Nuvens de Pontos com ICP

O principal objetivo deste desafio é o **alinhamento sequencial de nuvens de pontos 3D** do dataset KITTI para estimar a trajetória de um veículo. O notebook `icp_challenge/pipeline.ipynb` implementa um pipeline completo para resolver este problema.

#### 📝 Descrição do Pipeline

1.  **Carregamento de Dados**: Nuvens de pontos sequenciais do dataset KITTI e dados de `ground_truth` (trajetória real).
2.  **Pré-processamento**: Conversão das nuvens de pontos para o formato Open3D.
3.  **Alinhamento com ICP**: Aplicação do algoritmo **Iterative Closest Point (ICP)** para estimar a transformação entre nuvens de pontos consecutivas.
4.  **Estimativa de Trajetória**: Acumulação das transformações para reconstruir a trajetória do veículo.
5.  **Avaliação e Visualização**: Comparação da trajetória estimada com a `ground_truth` e visualização 3D dos resultados.

#### 📈 Resultados Esperados

O resultado final é uma visualização 3D que mostra a trajetória real (`ground_truth`), a trajetória estimada pelo pipeline e a sobreposição das nuvens de pontos alinhadas, permitindo uma avaliação completa da acurácia.

---

### Desafio 2: Busca de Pessoas por Rosto com Máscara

Este desafio foca na criação de um sistema de Machine Learning para identificar pessoas a partir de imagens de seus rostos, mesmo com a presença de máscaras faciais.

#### 📝 Descrição do Pipeline

1.  **Detecção Facial**: Localização de rostos nas imagens de entrada usando algoritmos robustos.
2.  **Extração de Features (Embeddings)**: Uso de uma Rede Neural Convolucional (CNN), FaceNet, para extrair um vetor de características único do rosto, focando em regiões não oclusas pela máscara (olhos, nariz, etc.).
3.  **Criação de Banco de Dados**: Armazenamento dos *embeddings* de um conjunto de imagens de referência.
4.  **Busca por Similaridade**: Ao receber uma nova imagem, o sistema extrai o *embedding* do rosto e o compara com o banco de dados usando métricas como a distância de cosseno para encontrar a correspondência mais próxima.

#### 📈 Resultados Esperados

O sistema deve ser capaz de retornar a identidade correta de uma pessoa em uma imagem de consulta, mesmo que ela esteja usando uma máscara, com um alto grau de precisão.

---

### 🛠️ Tecnologias e Bibliotecas

-   **Python**: Linguagem principal do projeto.
-   **Open3D / Trimesh**: Para processamento de dados 3D no desafio de ICP.
-   **OpenCV**: Para processamento de imagem e detecção facial.
-   **TensorFlow / PyTorch**: Para carregar e utilizar os modelos de deep learning de reconhecimento facial.
-   **NumPy**: Para manipulação eficiente de arrays e operações matemáticas.
-   **Matplotlib**: Para plotar gráficos e visualizações.
-   **Jupyter Notebook**: Para desenvolvimento interativo e documentação.

### 🚀 Como Executar

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/hugojardim/computer_vision_challenges.git
    cd computer_vision_challenges
    ```

2.  **Instale as dependências:**
    É recomendado usar um ambiente virtual. As dependências específicas de cada desafio podem ser encontradas nos respectivos notebooks.
    ```bash
    pip install open3d trimesh opencv-python tensorflow numpy matplotlib jupyter
    ```
    *Nota: A instalação de algumas bibliotecas pode variar dependendo do seu sistema operacional.*

3.  **Execute os Notebooks:**
    Navegue até a pasta do desafio desejado e execute o notebook principal.
    ```bash
    # Para o desafio de ICP
    jupyter notebook icp_challenge/pipeline.ipynb

    # Para o desafio de reconhecimento facial (exemplo)
    # jupyter notebook face_mask_search/face_recognition.ipynb
    ```
    Ou execute diretamente no Google Colab usando o badge no topo do README.

### ✒️ Autor

-   **Hugo Jardim** - [hugojardim](https://github.com/hugojardim)
