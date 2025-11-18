# Redes Neurais – Classificação do Dataset Iris 🌸🤖

Este repositório contém um experimento de **rede neural artificial** aplicada ao clássico **dataset Iris**, amplamente utilizado para introdução a problemas de **classificação supervisionada** em Machine Learning.

O objetivo é treinar um modelo capaz de classificar automaticamente o tipo de flor Iris a partir de características físicas (medidas das sépalas e pétalas).

---

## 🎯 Objetivos do Projeto

- Carregar e explorar o dataset **Iris**.
- Realizar o **pré-processamento** dos dados (normalização e codificação dos rótulos).
- Construir, treinar e avaliar um modelo de **rede neural feedforward** usando **TensorFlow/Keras**.
- Visualizar os dados e o desempenho do modelo com **gráficos**.

---

## 📊 Dataset Iris

O dataset Iris é composto por:

- **150 amostras** de flores.
- **3 classes** (espécies):
  - *Setosa*
  - *Versicolor*
  - *Virginica*
- **4 atributos de entrada**:
  - Comprimento da sépala
  - Largura da sépala
  - Comprimento da pétala
  - Largura da pétala

No notebook, o dataset é carregado diretamente da biblioteca `sklearn.datasets` por meio da função `load_iris()`.

---

## 🧠 Arquitetura da Rede Neural

O modelo é implementado com **Keras (TensorFlow)** usando a API `Sequential`.  
De forma geral, a arquitetura é:

- Camada de entrada: 4 neurônios (um para cada atributo)
- 1 ou mais **camadas densas ocultas** com função de ativação `relu`
- Camada de saída: 3 neurônios (um para cada classe), com ativação `softmax`

Configurações principais:

- **Função de perda:** `categorical_crossentropy`
- **Otimização:** `Adam`
- **Métrica:** `accuracy` (acurácia)
- **Divisão dos dados:** treino e teste com `train_test_split`

---

## 🛠️ Tecnologias Utilizadas

- **Python**
- **Jupyter Notebook**
- **TensorFlow / Keras**
- **Scikit-learn**
- **NumPy**
- **Matplotlib**

---

## 🔍 Etapas Implementadas no Notebook

No arquivo `Redes_Neurais.ipynb` são realizadas as seguintes etapas:

1. **Importação das bibliotecas** necessárias.
2. **Carregamento do dataset Iris** com `load_iris()`.
3. **Visualização dos dados** com:
   - Redução de dimensionalidade usando **PCA** (2 componentes)
   - Gráfico de dispersão das classes.
4. **Pré-processamento**:
   - Padronização dos dados com `StandardScaler()`.
   - Codificação dos rótulos com `to_categorical()`.
   - Divisão em treino e teste com `train_test_split()`.
5. **Construção do modelo de rede neural** com `Sequential()` e camadas `Dense`.
6. **Compilação e treinamento do modelo** com `model.fit()`.
7. **Avaliação do modelo** no conjunto de teste com `model.evaluate()`.
8. **Geração de gráficos**:
   - Evolução da **perda (loss)**.
   - Evolução da **acurácia** ao longo das épocas.
9. **Previsões** no conjunto de teste e comparação entre valores reais e previstos.

---

## ▶️ Como Executar o Projeto

### 1. Clonar o repositório

```bash
git clone https://github.com/SEU_USUARIO/redesneurais-iris.git
cd redesneurais-iris
