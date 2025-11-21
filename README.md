# 💬 Análise de Sentimentos em Texto (NLP)

## 💡 Visão Geral do Projeto

Este projeto demonstra a aplicação de **Processamento de Linguagem Natural (NLP)** para classificar o sentimento expresso em textos (como comentários e feedback de clientes) nas categorias **Positivo, Negativo e Neutro**. O objetivo é comparar a eficácia de modelos de Machine Learning Clássico vs. Deep Learning na compreensão do contexto e da semântica da linguagem.

O resultado é uma ferramenta crítica para a **Análise de Dados de Clientes** e a **Monitorização de Marca**.

---

## ⚙️ Metodologia e Arquitetura

O projeto foi dividido em duas fases para ilustrar a evolução das técnicas de NLP:

### 1. Fase Clássica (Linha de Base)

| Componente | Técnica | Objetivo |
| :--- | :--- | :--- |
| **Pré-processamento** | CountVectorizer (Bag-of-Words) | Converte texto em vetores de frequência de palavras. |
| **Modelo** | Multinomial Naive Bayes | Classificador probabilístico simples e eficiente para vetores esparsos. |
| **Resultado** | Baixa precisão em dados limitados | Demonstra a fragilidade de BoW/Naive Bayes ao lidar com semântica e contexto. |

### 2. Fase Deep Learning (Solução Final)

A arquitetura de Deep Learning é essencial para capturar o contexto temporal e a semântica de frases complexas.

| Camada | Função no Processamento de Linguagem |  |
| :--- | :--- | :--- |
| **Tokenização/Padding** | Converte palavras em sequências numéricas de tamanho fixo. | |
| **Embedding Layer** | Mapeia palavras para vetores densos (embeddings), capturando o significado real (semântica). | |
| **LSTM (RNN)** | Camada Recorrente que entende a **ordem** e o **contexto** das palavras (ex: negação). | |
| **Camada Densa (Saída)** | Mapeia o contexto aprendido pela LSTM para a classificação final (Positivo/Negativo/Neutro). | |

---

## ✅ Resultados e Conclusão

| Previsão | Modelo Clássico (Naive Bayes) | Modelo Deep Learning (LSTM) |
| :--- | :--- | :--- |
| **Comentário de Teste** | "O produto é incrível, superou todas as expectativas!" | "O produto é incrível, superou todas as expectativas!" |
| **Sentimento Previsto** | **Neutro** (Incorreto) | **Positivo** (Correto) |

A transição para a arquitetura LSTM resolveu o problema de classificação, provando que o **Deep Learning é superior para tarefas de compreensão textual (NLP)**, pois é capaz de inferir a intenção real ("incrível", "superou") mesmo com *datasets* pequenos, devido à sua capacidade de processar a sequência do texto.

---
