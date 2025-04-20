## Descrição do Projeto

Este projeto é composto por dois desafios práticos em visão computacional e ciência de dados, com foco em algoritmos fundamentais e pipelines de machine learning.

**Desafio 1: Implementação Manual do Algoritmo ICP para Análise de Rotas de Automóveis**

O objetivo deste desafio é implementar, do zero, o algoritmo Iterative Closest Point (ICP) para análise e alinhamento de rotas de automóveis. O ICP é um algoritmo amplamente utilizado para registrar e alinhar nuvens de pontos, minimizando a diferença entre dois conjuntos de pontos em 2D ou 3D. No contexto deste projeto, cada rota de automóvel será representada como uma nuvem de pontos, e o ICP será utilizado para alinhar trajetórias distintas, permitindo comparações precisas entre diferentes percursos.

Principais etapas do ICP:

- Seleção de um conjunto de pontos de referência (rota base) e um conjunto de pontos fonte (rota a ser alinhada).
- Para cada ponto da rota fonte, encontrar o ponto mais próximo na rota de referência.
- Estimar a melhor transformação (rotação e translação) que minimize a distância entre os pares de pontos correspondentes.
- Aplicar a transformação à rota fonte e repetir o processo até a convergência, ou seja, até que as diferenças sejam minimizadas.
- O resultado é uma transformação refinada que alinha as duas rotas de forma ótima[1].

**Desafio 2: Pipeline Completo para Detecção Facial com e sem Máscara**

O segundo desafio consiste em desenvolver um pipeline completo de machine learning para detecção facial, capaz de classificar se uma pessoa está usando máscara ou não. O pipeline deve ser implementado do zero, abrangendo as seguintes etapas:

- **ETL (Extract, Transform, Load):** Coleta, pré-processamento e preparação dos dados de imagens faciais.
- **Treinamento:** Desenvolvimento e treinamento de um modelo de classificação (por exemplo, CNN) para distinguir rostos com máscara de rostos sem máscara.
- **Inferência:** Implementação de um sistema de inferência capaz de realizar predições em imagens inéditas, avaliando a presença ou ausência de máscara.

O objetivo é construir todas as etapas do pipeline, desde a ingestão dos dados até a avaliação do modelo, promovendo uma compreensão aprofundada de cada fase do fluxo de trabalho em projetos de visão computacional.

---

Este projeto proporciona uma experiência prática e abrangente, unindo a implementação de algoritmos clássicos e o desenvolvimento de soluções completas em machine learning.
