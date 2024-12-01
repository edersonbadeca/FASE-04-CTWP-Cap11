Aqui está o README traduzido para o português, adaptado para o contexto acadêmico:

---

# **Classificação Automatizada de Grãos com Machine Learning**

Este projeto automatiza a classificação de grãos de trigo utilizando algoritmos de Machine Learning. Com base no **"Seeds Dataset"** do UCI Machine Learning Repository, exploramos técnicas de pré-processamento de dados, treinamento de modelos de classificação, otimização de hiperparâmetros e avaliação de desempenho.

---

## **Contexto do Problema**

Em cooperativas agrícolas de pequeno porte, a classificação de grãos é realizada manualmente por especialistas, o que pode ser ineficiente e propenso a erros. Este projeto automatiza esse processo, melhorando a precisão e eficiência.

O dataset contém 210 amostras de grãos de trigo pertencentes a três variedades:
- **Kama**
- **Rosa**
- **Canadian**

Cada amostra é descrita por características físicas do grão, permitindo a criação de modelos preditivos.

---

## **Detalhes do Conjunto de Dados**

O conjunto de dados possui 7 características e 1 rótulo (a classe):
- **Características**:
  - Área do grão.
  - Perímetro do grão.
  - Compacidade:

$$
\text{Compacidade} = \frac{4 \pi \times \text{Área}}{\text{Perímetro}^2}
$$
  - Comprimento do Núcleo: Comprimento do eixo principal do grão.
  - Largura do Núcleo: Comprimento do eixo secundário do grão.
  - Coeficiente de Assimetria: Medida da assimetria do grão.
  - Comprimento do Sulco: Comprimento do sulco central do grão.
- **Rótulo**:
  - Variedade do trigo (1 para Kama, 2 para Rosa, 3 para Canadian).

---

## **Detalhes da Implementação**

### **Metodologia**
Este projeto segue a metodologia **CRISP-DM**:
1. **Entendimento dos Dados**: Exploração e visualização do dataset.
2. **Preparação dos Dados**: Limpeza, normalização e divisão dos dados em conjuntos de treino e teste.
3. **Modelagem**: Treinamento de múltiplos modelos de classificação.
4. **Avaliação**: Comparação do desempenho dos modelos usando métricas.
5. **Resultados**: Apresentação dos insights e do melhor modelo.

---

### **Etapas Realizadas**

#### **1. Pré-processamento dos Dados**
- **Exploração**: Visualizamos a distribuição dos dados com histogramas, gráficos de dispersão e KDEs.
- **Normalização**: As características foram padronizadas usando:
  $$
  Z = \frac{X - \mu}{\sigma}
  $$
  onde 𝜇 é a média e σ é o desvio padrão.
- **Tratamento de Valores Ausentes**: Não foram encontrados valores ausentes.

#### **2. Treinamento de Modelos de Machine Learning**
Modelos utilizados:
- **K-Nearest Neighbors (KNN)**:
  - Hiperparâmetro: 𝑘 (número de vizinhos).
  - Métrica de distância: Euclidiana.
- **Support Vector Machine (SVM)**:
  - Kernels: Linear, Polinomial, RBF.
  - Regularização (𝐶): Controle de margem e erro.
  - Gamma (γ): Coeficiente do kernel.
- **Random Forest**:
  - Número de árvores $$ n^{\text{estimators}} $$

  - Profundidade máxima $$ d_{\text{max}} $$

#### **3. Otimização de Hiperparâmetros**
Utilizamos o **GridSearchCV** para otimizar os hiperparâmetros:
$$
\text{Acurácia} = \frac{\text{Previsões Corretas}}{\text{Total de Previsões}}
$$
O Grid Search avaliou todas as combinações possíveis de hiperparâmetros para encontrar a melhor configuração.

#### **4. Avaliação**
Os modelos foram avaliados utilizando:
- **Matriz de Confusão**:
  $$
  \begin{bmatrix}
  \text{VP} & \text{FP} \\
  \text{FN} & \text{VN}
  \end{bmatrix}
  $$
- **Métricas**:
  - Precisão: $$ \frac{\text{VP}}{\text{VP} + \text{FP}} $$
  - Recall: $$ \frac{\text{VP}}{\text{VP} + \text{FN}} $$
  - F1-Score: $$ 2 \times \frac{\text{Precisão} \times \text{Recall}}{\text{Precisão} + \text{Recall}} $$

---

### **Resultados Obtidos**
| Modelo           | Acurácia (%) | Melhores Hiperparâmetros          |
|------------------|--------------|-----------------------------------|
| KNN              | 96.7         | $$ k = 5 $$                      |
| SVM              | 97.8         | $$ C = 1, \gamma = \text{scale}, \text{kernel} = \text{rbf} $$ |
| Random Forest    | 98.5         | $$ n_{\text{estimators}} = 150, d_{\text{max}} = 30 $$ |

---

## **Instruções de Uso**

### **1. Clone o Repositório**
```bash
git clone <link-do-repositorio>
```

### **3. Execute o Notebook**
Abra o [notebook](./src/FASE_04_CTWP_Cap11.ipynb) em Jupyter ou Google Colab e execute as células para reproduzir a análise e o treinamento dos modelos.

---

## **Conclusões**

Este projeto demonstra a eficácia do Machine Learning na automação da classificação de grãos:
- **Random Forest** apresentou a maior acurácia, com **98.5%**.
- Técnicas de visualização ajudaram a entender os padrões e relações entre as características.
- A otimização de hiperparâmetros melhorou significativamente o desempenho dos modelos.
