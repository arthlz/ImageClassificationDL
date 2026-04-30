# Desafio de Classificação de Superfícies de Vias - Voxar Labs 2026

Este repositório contém a solução para o desafio de classificação de imagens de superfícies de vias, focado na identificação de três categorias principais: Asphalt, Belgian Blocks e Off-road. O projeto prioriza não apenas o desempenho do modelo, mas a estruturação crítica do problema e a interpretação fundamentada dos resultados.

----
📋 Visão Geral do Problema

O dataset fornecido apresenta condições visuais desafiadoras que simulam cenários reais de direção, incluindo:  

    Variações de iluminação (cenários diurnos e noturnos).  

    Condições climáticas adversas (chuva e ruído visual).  

    Heterogeneidade de captura (diferentes dispositivos e ângulos).  

    Desbalanceamento severo entre as classes.

-----

🚀 Metodologia e Solução

A abordagem adotada baseia-se em Transfer Learning, com intervenções guiadas por uma Análise Exploratória de Dados (EDA) quantitativa.  
Diagnósticos Principais

Antes da modelagem, foram identificados três pontos críticos:
    
  1. **Desbalanceamento severo**: o pdf enviado explica que o dataset está altamente desbalanceado, logo os modelos terão uma tendência a ignorar classes minoritárias.

  2. **Variações de captura**: iluminação variável (chuva, noite, sol direto), múltiplos dispositivos de captura e ângulos de câmera.
    
  3. **Ambiguidade visual**: asphalt molhado pode assemelhar-se a belgian_blocks; offroad com lama pode parecer asphalt escuro.

-----

# Estrutura do repositório
```text
  📁 Road-Surface-Classification/               # Raiz do repositório
  ├── 📂 dataset_voxar/                   # Diretório de dados
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
# Intervenções Experimentais

Foram realizados experimentos fundamentados em hipóteses científicas:  

    Weighted Loss: Implementado para mitigar o viés em direção à classe majoritária.  

    Data Augmentation Estratégica: Aplicação de transformações que respeitam a natureza física dos dados de via.  

    Investigação de Arquitetura: Comparação de performance entre modelos pré-treinados e ajustes de hiperparâmetros.

# Reprodutibilidade(Pelo vscode):
   ```
   Todo o código foi produzido e rodou localmente no python 3.10.7
   ```

1. Clone o repositório
   ```bash
   git clone https://github.com/arthlz/Road-Surface-Classification.git
   ```
   
2. Acesse a pasta do projeto
   ```pasta
   cd Road-Surface-Classification
   ```

3. Baixe a pasta "dataset" presente no link
   ```dataset
   Extraia os arquivos baixados e coloque-os na raiz do projeto dentro de uma pasta chamada dataset
   Se baseie na estrutura do repositório para arrumar a pasta
   ```

4. No terminal, crie um ambiente virtual e ative-o
   ```Venv
    python -m venv venv <- Cria o ambiente virtual
   
    - Dispositivos Windows:
    .\venv\Scripts\activate -< Ativa o ambiente virtual
   
    - Dispositivos Linux/Mac:
    source venv/bin/activate <- Ativa o ambiente virtual
   ```

5. Instale os requerimentos necessários:
   ```bash
   pip install -r requirements.txt
   ```

6. Abra e execute o arquivo principal.

# Opção principal para Reprodutibilidade:

Entre no google colab e execute o notebook: 🔗 [**Colab**](https://colab.research.google.com/drive/1OJ0W3QY2TvE6Ix1OJ7l00k_2t5PPvdJw?usp=sharing)
