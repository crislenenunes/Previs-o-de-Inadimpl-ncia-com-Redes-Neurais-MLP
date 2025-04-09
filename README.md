# 🧠💳 Modelo Preditivo com Redes Neurais MLP  
### 🎯 Previsão de Inadimplência em Cartões de Crédito

Este repositório contém um projeto de aplicação de redes neurais multicamadas (MLP) para prever a inadimplência de clientes de cartão de crédito com base em dados reais.  
O objetivo é treinar um modelo de **classificação binária** utilizando variáveis como limite de crédito, histórico de pagamento, idade, escolaridade, entre outras.

> 📌 Projeto desenvolvido durante o **Bootcamp de Inteligência Artificial LLM da SoulCode**.

---

## 🛠 Tecnologias Utilizadas

- Python 3  
- Pandas  
- NumPy  
- Scikit-learn  
- TensorFlow / Keras  
- Imbalanced-learn (SMOTE)  
- Matplotlib  
- Google Colab  
- GitHub  

---

## 🧠 O que o código faz?

### 📂 Carregamento do Dataset

- Conjunto de dados público de inadimplência de clientes de cartão de crédito.
- A variável-alvo `default.payment.next.month` indica se o cliente foi inadimplente (`1`) ou não (`0`).

### 🔍 Análise Exploratória e Limpeza dos Dados

- Remoção de colunas irrelevantes e inconsistentes.  
- Tratamento de valores nulos.  
- Conversão de variáveis categóricas com One-Hot Encoding.  
- Normalização dos dados com Min-Max.  
- Balanceamento de classes com **SMOTE** para evitar viés do modelo.

### 🤖 Modelagem com Rede Neural MLP

- Separação dos dados em treino e teste (80/20).  
- Criação de um modelo com camadas ocultas, ativação ReLU e função sigmoide na saída.  
- Uso de Dropout para reduzir overfitting.  
- Otimização com o otimizador **Adam**.  
- **Early stopping** aplicado para melhorar a generalização.

---

## 📈 Avaliação do Modelo

### ✅ Principais Métricas

| Métrica        | Classe 0 | Classe 1 |
|----------------|----------|----------|
| Precisão       | 0.82     | 0.79     |
| Recall         | 0.78     | 0.83     |
| F1-Score       | 0.80     | 0.81     |
| Acurácia Geral | 0.80     | -        |
| AUC-ROC        | 0.85     | -        |

### 📊 Matriz de Confusão

```
              precision    recall  f1-score   support

           0       0.82      0.78      0.80      4676
           1       0.79      0.83      0.81      4665

    accuracy                           0.80      9341
   macro avg       0.80      0.80      0.80      9341
weighted avg       0.80      0.80      0.80      9341
```

### 📌 Interpretação

- O modelo teve **bom desempenho**, com **acurácia geral de 80%**.  
- Demonstrou eficiência para prever inadimplentes (classe 1), com **recall de 83%**.  
- O **AUC-ROC de 0.85** mostra ótima capacidade de separação entre as classes.  
- O uso do SMOTE ajudou a balancear as classes, melhorando a qualidade da predição.

---

## 📊 Gráficos Gerados

- Matriz de Confusão  
- Gráficos de Precisão, Recall e F1-score  
- Curva ROC  
- Gráfico de perda e acurácia durante o treinamento  

---

## 🚀 Como Executar o Projeto

1. Clone este repositório:

```bash
git clone https://github.com/seu-usuario/previsao-inadimplencia-mlp
```

2. Instale as dependências (caso rode localmente):

```bash
pip install pandas numpy scikit-learn tensorflow imbalanced-learn matplotlib seaborn
```

3. Execute o notebook no Jupyter Notebook ou Google Colab:  
👉 [Acessar no Google Colab](https://colab.research.google.com/drive/1HOd95xVDk5H7rBmd4bV_X1ZBoQyBMhM0?usp=sharing)


## 📜 Licença

Projeto educacional, desenvolvido durante o **Bootcamp de IA LLM da SoulCode**.  
Distribuído sob licença **gratuita para fins educacionais e não comerciais**.
