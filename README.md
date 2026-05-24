# Dog Breed Classifier — Classificador de Raças de Cães

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SEU_USUARIO/dog-breed-classifier/blob/main/DogBreedClassifier_FIAP.ipynb)

> **Disciplina:** Disruptive Architectures: IoT, IOB & Generative IA  
> **Instituição:** FIAP | **Sprint:** 1º Sprint

---

## Sobre o Projeto

Classificador de raças de cães usando **Visão Computacional** com **YOLOv8**, capaz de identificar **10 raças** a partir da câmera em tempo real, com output visual sobreposto via **OpenCV**.

##  Integrantes
 
| Nome | RM | Turma |
| :--- | :--- | :--- |
| Diego Andrade | 566385 | 2TDSPO |
| Grazielle Alencar | 561529 | 2TDSPO |
| Julia Altino | 564870 | 2TDSPO |

---

## Raças Identificadas

| Classe | Raça |
|--------|------|
| `Beagle` | Beagle |
| `Boxer` | Boxer |
| `Bulldog` | Bulldog |
| `Dachshund` | Dachshund (Salsicha) |
| `German_Shepherd` | Pastor Alemão |
| `Golden_Retriever` | Golden Retriever |
| `Labrador_Retriever` | Labrador Retriever |
| `Poodle` | Poodle |
| `Rottweiler` | Rottweiler |
| `Yorkshire_Terrier` | Yorkshire Terrier |

---

## Estrutura do Repositório

```
dog-breed-classifier/
│
├── DogBreedClassifier_FIAP.ipynb   # Notebook principal (Colab)
├── README.md                        # Este arquivo
│
└── datasets/                 
    ├── train/                       # Imagens de treinamento por raça
    │   ├── Beagle/
    │   ├── Boxer/
    │   ├── Bulldog/
    │   └── ...
    ├── valid/                       # Imagens de validação
    ├── test/                        # Imagens de teste
    ├── README.dataset.txt
    └── README.roboflow.txt
```

---

## Tecnologias Utilizadas

| Tecnologia | Função |
|------------|--------|
| **YOLOv8** (Ultralytics) | Treinamento e classificação de imagens |
| **OpenCV** | Processamento e output visual |
| **Google Colab + GPU T4** | Ambiente de execução |
| **GitHub** | Repositório do dataset e código-fonte |

---

## Como Executar

**1.** Clique no badge **Open in Colab** no topo deste README

**2.** Habilite a GPU: `Ambiente de execução > Alterar tipo de ambiente > GPU (T4)`

**3.** Execute as células em ordem:

| Seção | O que faz |
|-------|-----------|
| Seção 1 | Instala o Ultralytics (YOLOv8) |
| Seção 2 | Importa as bibliotecas |
| Seção 3 | Clona o repositório com o dataset |
| Seção 4 | Treina o modelo com as imagens |
| Seção 5 | Carrega o `best.pt` gerado |
| Seção 6 | Configura os nomes das raças |
| Seção 7 | Define a função de câmera |
| **Seção 8** | **Pipeline completo: câmera → classificação → output visual** |
| Seção 9 | Validação com imagens do dataset (sem câmera) |

---

## Resultado Esperado

Após capturar a foto pela webcam, o output visual exibe:

```
┌─────────────────────────────────────┐
│  GOLDEN RETRIEVER (94.3%)           │  ← barra verde (alta confiança)
│                                     │
│         [foto do cachorro]          │
│                                     │
└─────────────────────────────────────┘
```

Cor da barra:
- 🟢 **Verde** — confiança ≥ 70%
- 🟠 **Laranja** — confiança entre 45% e 70%
- 🔴 **Vermelho** — confiança < 45%

---

## Próximos Passos (Sprints Futuros)

- Dashboard em tempo real via protocolo MQTT
- Expansão do dataset com mais raças

---
