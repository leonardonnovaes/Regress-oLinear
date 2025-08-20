# 📘 Estudos de Machine Learning - Regressão Linear

Este repositório contém meus estudos em **Machine Learning**, aplicados a um problema de **Regressão Linear**.  
O objetivo é construir um modelo capaz de **prever o consumo de uma unidade**, utilizando como base um conjunto de dados com variáveis diversas.

---

## 🔎 Desafio

O desafio proposto foi o seguinte:

- O **consumo** é calculado a partir da diferença entre os valores das variáveis `final` e `inicial`.  
- O **primeiro modelo** deve considerar **todas as variáveis** (inclusive a variável categórica `bloco`).  
- A partir do primeiro modelo, devem ser verificadas as variáveis cujo **coeficiente é estatisticamente igual a zero** (`p-valor > 0.05`).  
- Essas variáveis devem ser **retiradas** e o modelo deve ser refeito apenas com as variáveis **estatisticamente significativas**.  
- O conjunto de dados possui **valores nulos** e **valores inválidos** (ex: consumos negativos) que devem ser tratados para evitar erros no modelo.

---

## ⚙️ Etapas do Projeto

1. **Carregamento e análise exploratória dos dados**
   - Identificação das colunas disponíveis.  
   - Cálculo do consumo (`final - inicial`).  
   - Análise inicial de valores faltantes e possíveis inconsistências.  

2. **Tratamento de dados**
   - Remoção/tratamento de valores nulos.  
   - Eliminação de valores inválidos (como consumos negativos e `price = 0`).  
   - Codificação de variáveis categóricas (`bloco`) em variáveis dummies.  

3. **Construção do primeiro modelo**
   - Utilização de todas as variáveis disponíveis (`price`, `month`, `year`, `apartment` e blocos A–G).  
   - Ajuste com **Regressão Linear**.  
   - Avaliação dos coeficientes e **p-valores** usando `statsmodels`.  

4. **Refinamento do modelo**
   - Remoção das variáveis com `p-valor > 0.05` (ex.: `bloco-G` e outras).  
   - Construção de um novo modelo apenas com variáveis estatisticamente significativas.  
   - Comparação da performance entre os modelos.  

---

## 📊 Resultados Obtidos

- O **primeiro modelo** apresentou coeficientes não significativos em algumas variáveis (p > 0.05).  
- Após o **refinamento**, o modelo final manteve o **R²** praticamente estável, mas ficou **mais interpretável e consistente**, considerando apenas variáveis realmente relevantes.  
- O processo evidenciou a importância de:
  - Tratar dados nulos e inconsistentes antes da modelagem.  
  - Utilizar análise estatística (p-valores) para eliminar variáveis irrelevantes.  
  - Comparar modelos para validar a melhoria na interpretação.  

---

## 🛠️ Tecnologias utilizadas

- **Python 3**  
- **Pandas** → Manipulação e limpeza dos dados.  
- **NumPy** → Operações matemáticas.  
- **Statsmodels / Scikit-learn** → Construção e avaliação dos modelos de regressão linear.  
- **Matplotlib / Seaborn** → Visualizações gráficas.  

---

## 🚀 Objetivo de Aprendizado

Este projeto faz parte dos meus **estudos de Machine Learning**, com foco em:

- Compreensão do processo de **modelagem estatística**.  
- Interpretação de **coeficientes e p-valores**.  
- Tratamento de **dados reais com inconsistências**.  
- Construção de modelos de regressão linear mais robustos e interpretáveis.  

---
