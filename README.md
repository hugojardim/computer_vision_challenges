#  desafios-de-visao-computacional

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![Open3D](https://img.shields.io/badge/Open3D-4B9B7A.svg?style=flat)
![Trimesh](https://img.shields.io/badge/Trimesh-E94E36.svg?style=flat)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626.svg?style=flat&logo=Jupyter&logoColor=white)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hugojardim/computer_vision_challenges/blob/main/icp_challenge/pipeline.ipynb)

Este repositório contém soluções para desafios de Visão Computacional, com foco principal no processamento e alinhamento de dados 3D, como nuvens de pontos.

## 챌린지 1: Alinhamento de Nuvens de Pontos com ICP

O principal desafio abordado neste projeto é o **alinhamento sequencial de nuvens de pontos 3D** do dataset KITTI. O objetivo é estimar a trajetória de um veículo (odometria) através do alinhamento sucessivo de "frames" de nuvens de pontos capturados por um sensor LiDAR.

O notebook `icp_challenge/pipeline.ipynb` implementa um pipeline completo para resolver este problema.

### 📝 Descrição do Pipeline

1.  **Carregamento de Dados**: As nuvens de pontos sequenciais do dataset KITTI e os dados de `ground_truth` (trajetória real) são carregados.
2.  **Pré-processamento**: As nuvens de pontos são convertidas para o formato do Open3D e preparadas para o alinhamento.
3.  **Alinhamento com ICP**: O algoritmo **Iterative Closest Point (ICP)** é aplicado para estimar a transformação (rotação e translação) entre nuvens de pontos consecutivas.
4.  **Estimativa de Trajetória**: As transformações estimadas são acumuladas para reconstruir a trajetória do veículo.
5.  **Avaliação**: A trajetória estimada é comparada com a trajetória `ground_truth` para avaliar a precisão do algoritmo.
6.  **Visualização**: Os resultados, incluindo as nuvens de pontos alinhadas e a comparação das trajetórias, são visualizados em 3D.

### 🛠️ Tecnologias e Bibliotecas

-   **Python**: Linguagem principal do projeto.
-   **Open3D**: Uma biblioteca moderna para processamento de dados 3D. Utilizada para visualização e implementação do ICP.
-   **Trimesh**: Biblioteca para carregar e manipular malhas 3D e nuvens de pontos (arquivos `.obj`).
-   **NumPy**: Para manipulação eficiente de arrays e operações matemáticas.
-   **Matplotlib**: Para plotar gráficos 2D/3D, como a comparação das trajetórias.
-   **Jupyter Notebook**: Para desenvolvimento interativo e documentação do processo.

### 🚀 Como Executar

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/hugojardim/computer_vision_challenges.git
    cd computer_vision_challenges
    ```

2.  **Instale as dependências:**
    O notebook `icp_content/pipeline.ipynb` contém os comandos de instalação. É recomendado usar um ambiente virtual.
    ```bash
    pip install open3d trimesh numpy matplotlib jupyter
    ```
    *Nota: A instalação do `open3d` pode variar dependendo do seu sistema operacional e hardware.*

3.  **Estrutura de Dados:**
    Certifique-se de que o dataset KITTI esteja na pasta `KITTI-Sequence/` e o arquivo `ground_truth.npy` esteja no diretório raiz do desafio, conforme esperado pelo notebook.

4.  **Execute o Notebook:**
    Abra e execute o notebook principal para ver todo o processo.
    ```bash
    jupyter notebook icp_challenge/pipeline.ipynb
    ```
    Ou execute diretamente no Google Colab usando o badge no topo do README.

### 📈 Resultados Esperados

O resultado final é uma visualização 3D que mostra:
-   A trajetória real (`ground_truth`).
-   A trajetória estimada pelo pipeline de ICP.
-   Uma sobreposição das nuvens de pontos alinhadas.

Isso permite uma avaliação qualitativa e quantitativa da acurácia da odometria estimada.

## ✒️ Autor

-   **Hugo Jardim** - [hugojardim](https://github.com/hugojardim)
