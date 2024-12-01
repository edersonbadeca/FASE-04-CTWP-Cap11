# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="assets/logo.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

# Implementando algoritmos de Machine Learning com Scikit-learn

## Grupo 54

## 👨‍🎓 Integrantes: 
- <a href="https://www.linkedin.com/in/caiorcastro/">Caio Rodrigues Castro</a> 
- <a href="https://www.linkedin.com/in/ederson-badeca/">Ederson Luiz Badeca dos Santos</a> 
- <a href="https://www.linkedin.com/in/digitalmanagerfelipesoares/">Felipe Soares Nascimento</a>
- <a href="https://www.linkedin.com/in/lfhillesheim/">Lucas Ferreira Hillesheim</a>

## 👩‍🏫 Professores:
### Tutor(a) 
- <a href="https://www.linkedin.com/in/lucas-gomes-moreira-15a8452a/">Lucas Gomes</a>
### Coordenador(a)
- <a href="https://www.linkedin.com/in/profandregodoi/">André Godoi Chiovato</a>

## 📜 Descrição

O projeto consiste na automação da classificação de grãos de trigo utilizando algoritmos de Machine Learning. Baseado no **"Seeds Dataset"** do UCI Machine Learning Repository, aplicamos as etapas da metodologia **CRISP-DM** para explorar, processar e modelar os dados, além de otimizar hiperparâmetros dos modelos.

### Objetivo
Automatizar a classificação de três variedades de trigo (**Kama, Rosa e Canadian**) com base em características físicas, como área, perímetro e coeficiente de assimetria, utilizando algoritmos como KNN, SVM e Random Forest.

### Principais Etapas:
1. **Pré-processamento dos Dados**:
   - Normalização: 
\[
     Z = \frac{X - \mu}{\sigma}
\]
   - Visualização com histogramas, gráficos de dispersão e KDE.
2. **Modelagem**:
   - Algoritmos: KNN, SVM e Random Forest.
   - Otimização de hiperparâmetros com GridSearchCV.
3. **Avaliação**:
   - Métricas utilizadas: Precisão, Recall, F1-Score, Matriz de Confusão.
   - Resultados:
     | Modelo         | Acurácia (%) |
     |----------------|--------------|
     | KNN            | 96.7         |
     | SVM            | 97.8         |
     | Random Forest  | 98.5         |

---

## 🔧 Como executar o código

### Pré-requisitos
- Python 3.9 ou superior.
- Bibliotecas: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`.

### Passos para execução
1. Clone o repositório:
   ```bash
   git clone <link-do-repositorio>
   cd <diretorio-do-projeto>
   
Utilize Jupyter Notebook ou Google Colab para executar o arquivo .ipynb.