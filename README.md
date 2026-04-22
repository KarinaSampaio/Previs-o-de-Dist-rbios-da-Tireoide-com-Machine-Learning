# 🧠 Previsão de Distúrbios da Tireoide com Machine Learning

## 📌 Objetivo

Este projeto tem como objetivo desenvolver um modelo de machine learning capaz de identificar distúrbios da tireoide com base em dados clínicos e laboratoriais.

---

## 📊 Sobre os dados

O dataset contém informações médicas de pacientes, incluindo:

* Dados demográficos (idade, sexo)
* Condições clínicas (doença, gravidez, etc.)
* Exames laboratoriais (TSH, T3, TT4, FTI, entre outros)

---

## ⚠️ Principais desafios encontrados

* Valores ausentes representados como `"?"`
* Tipos de dados incorretos (numéricos como `object`)
* Variáveis sem variabilidade
* Dataset desbalanceado

---

## 🧹 Pré-processamento

* Substituição de `"?"` por `NaN`
* Conversão de tipos numéricos
* Remoção de colunas sem informação (ex: TBG)
* Codificação de variáveis categóricas
* Pipeline com:

  * Imputação (median / most frequent)
  * Padronização
  * One-Hot Encoding

---

## 🤖 Modelos utilizados

* Regressão Logística
* Random Forest
* Gradient Boosting

---

## 📈 Resultados

* **ROC AUC ≈ 1.00**
* **Accuracy ≈ 99%+**
* Excelente separação entre classes

---

## 🔍 Análise crítica

Apesar do alto desempenho, foi identificado que:

* A variável **TSH** possui alto poder preditivo isolado (**AUC ≈ 0.99**)
* Ao remover o TSH:

  * O desempenho cai significativamente (**AUC ≈ 0.85**)
  * O modelo perde capacidade de identificar a classe minoritária

👉 Isso indica que o problema é fortemente dependente de exames laboratoriais.

---

## 📊 Principais insights

* TSH é a variável mais importante
* Variáveis clínicas têm menor impacto isolado
* O problema é altamente separável

---

## 🧠 Conclusão

O modelo apresenta excelente desempenho, mas sua eficácia está diretamente ligada à presença de variáveis altamente informativas. Isso reforça a importância da interpretação crítica em projetos de machine learning, especialmente na área da saúde.

---

## 🚀 Tecnologias utilizadas

* Python
* Pandas
* Scikit-learn
* Matplotlib

---

## 📁 Estrutura do projeto

* `Projeto_Final.ipynb` → análise completa
* `data/` → dataset
* `README.md` → documentação

---

## 👨‍💻 Autor

Projeto desenvolvido para fins educacionais (EBAC) com foco em prática de ciência de dados aplicada.
