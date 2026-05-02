# 🚌 Desafio de Classificação de Superfícies de Vias(Asphalt, Belgian_blocks e Offroad)

Este repositório contém a solução para o desafio de classificação de imagens de superfícies de vias, focado na identificação de três categorias principais: **Asphalt, Belgian Blocks e Off-road**. O projeto aplica técnicas de **Deep Learning** e **Visão Computacional** para identificar padrões de pavimentação em condições reais de captura, priorizando a interpretabilidade do modelo e o tratamento de dados desbalanceados.

----
# 📋 Visão Geral do Problema

O **objetivo** é classificar imagens em três categorias distintas:

- `Asphalt`: Superfícies asfálticas uniformes.  

- `Belgian Blocks`: Pavimentos de paralelepípedo (comumente confundidos com asfalto em baixa resolução).  

- `Off-road`: Superfícies não pavimentadas (terra, cascalho, areia).

O dataset fornecido apresenta condições visuais desafiadoras que simulam cenários reais de direção, incluindo:  

- Variações de iluminação (cenários diurnos e noturnos).  

- Condições climáticas adversas (chuva e ruído visual).  

- Heterogeneidade de captura (diferentes dispositivos e ângulos).  

- Desbalanceamento severo entre as classes.

-----

## 🚀 Metodologia e Solução

A solução utiliza **Transfer Learning** com arquiteturas consagradas pré-treinadas no ImageNet, permitindo extrair características complexas mesmo com um volume limitado de dados.

### 1. Estratégia de Treino
* **Pré-processamento**: Redimensionamento para 256px seguido de um `CenterCrop` de 224px para focar na textura central da via.
* **Data Augmentation**: Uso de `ColorJitter`, `RandomHorizontalFlip` e rotações para aumentar a capacidade de generalização.
* **Tratamento de Desbalanceamento**: Implementação de **Weighted Random Sampler** e pesos na função de perda (CrossEntropyLoss).

### 2. Experimentos Realizados

| Experimento | Arquitetura | Foco Técnico |
| :--- | :--- | :--- |
| **01 (Baseline)** | **ResNet-18** | Estabelecimento de métricas base sem pesos. |
| **02** | **ResNet-50** | Introdução de **Weighted Loss** e rede mais profunda. |
| **03** | **ResNet-50** | Intensificação de Data Augmentation para cenários noturnos/chuva. |
| **04** | **EfficientNet-B0** | Otimização de parâmetros e eficiência computacional. |

---
-----

## Estrutura do repositório
```text
  📁 Road-Surface-Classification/               # Raiz do repositório
  ├── 📂 dataset/                   # Diretório de dados
  │   ├── 📂 test/                        # Conjunto de teste
  │   │   ├── 📂 asphalt                  # Amostras de asfalto
  │   │   ├── 📂 belgian_blocks           # Amostras de paralelepípedos
  │   │   └── 📂 offroad                  # Amostras off-road
  │   └── 📂 train/                       # Conjunto de treinamento
  │       ├── 📂 asphalt                  # Amostras de asfalto
  │       ├── 📂 belgian_blocks           # Amostras de paralelepípedos
  │       └── 📂 offroad                  # Amostras off-road
  ├── ⚙️ venv/                            # Ambiente virtual (ignorado pelo Git)
  ├── 📄 .gitignore                       # Filtro de arquivos do Git
  ├── 📓 Desafio_IC_Voxar_Labs_2026.ipynb # Notebook principal
  ├── 📖 README.md                        # Documentação do projeto
  └── 📋 requirements.txt                 # Dependências do Python
```

-----

## Reprodutibilidade(Não será disponibilizado o dataset, mas o código está presente abaixo):

Entre no google colab e execute o notebook: 🔗 [**Colab**](https://colab.research.google.com/drive/1OJ0W3QY2TvE6Ix1OJ7l00k_2t5PPvdJw?usp=sharing)

-----------

## 💻Programador:

<table align="center">
  <tr>
    <td align="center">
      <a href="https://github.com/arthlz">
        <img src="https://avatars.githubusercontent.com/u/173482833?v=4" width="120px;" alt="Arthur Luz"/><br>
        <sub><b>Arthur Luz</b></sub>
      </a>
    </td>
  </tr>
</table>

-------

## 🖥️ Tecnologias Utilizadas:
<div align="left">
  <!-- Linguagem Principal -->
  <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" />
  <!-- Framework de Deep Learning -->
  <img src="https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=pytorch&logoColor=white" />
  <!-- Manipulação de Dados -->
  <img src="https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white" />
  <!-- Machine Learning e Métricas -->
  <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white" />
  <!-- Visão Computacional -->
  <img src="https://img.shields.io/badge/opencv-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white" />
  <!-- Visualização -->
  <img src="https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black" />
  <img src="https://img.shields.io/badge/Seaborn-444876?style=for-the-badge&logo=python&logoColor=white" />
  <!-- Ambiente e Ferramentas -->
  <img src="https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252" />
  <img src="https://img.shields.io/badge/Jupyter-F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white" />
</div>
