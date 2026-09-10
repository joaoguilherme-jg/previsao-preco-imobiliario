
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/joaoguilherme-jg/previsao-preco-imobiliario/blob/main/Housing.ipynb)

Este projeto consiste na implementação prática do **Capítulo 2** do livro *"Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow"* de Aurélien Géron.

O objetivo é construir um modelo de regressão para prever o preço mediano de imóveis na Califórnia com base em dados do censo de 1990.

---

## Fluxo do Projeto

1. **Amostragem Estratificada:** Divisão dos dados em treino e teste garantindo a representatividade das faixas de renda (`income_cat`).
2. **Análise Exploratória:** Visualização geográfica e matriz de correlação das variáveis.
3. **Engenharia de Atributos:** Criação de novas métricas (cômodos por domicílio, quartos por cômodo e população por domicílio).
4. **Pré-processamento Automatizado:** Uso de `ColumnTransformer` para:
   * Imputação de valores ausentes pela mediana (`SimpleImputer`).
   * Codificação binária da variável de texto `ocean_proximity` (`OneHotEncoder`).
   * Padronização de escala das variáveis numéricas (`StandardScaler`).
5. **Treinamento e Ajuste Fino:**
   * Treinamento do modelo **Random Forest Regressor**.
   * Avaliação por Validação Cruzada (*10-fold Cross-Validation*).
   * Otimização de hiperparâmetros via **`GridSearchCV`**.

---

## Como Executar

### Online
Clique no botão **Open in Colab** no topo deste README para rodar o notebook interativamente na nuvem sem precisar instalar nada.

### Localmente
1. Clone este repositório, e depois crie e ative um ambiente virtual:

python3 -m venv my_env
source my_env/bin/activate  # Linux/macOS
my_env\Scripts\activate   # Windows

2. Instale as dependências e abra o Jupyter:

pip install pandas numpy matplotlib scikit-learn jupyter
jupyter notebook Housing.ipynb

---
