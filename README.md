# 🌙 Previsão da Qualidade do Sono: Impacto da Cafeína e Hábitos Diários

Este projeto tem como objetivo analisar e prever a qualidade do sono de indivíduos com base em diversos fatores, como consumo de cafeína, nível de stresse, atividade física e problemas de saúde. O modelo final auxilia na orientação de hábitos saudáveis e na personalização de experiências em plataformas de bem-estar.

##  Tecnologias e Ferramentas

- **Linguagem:** Python  
- **Bibliotecas:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn  
- **Modelos:** Regressão Logística e Random Forest (Classificação Multiclasse)

##  Estrutura do Projeto

O desenvolvimento do projeto seguiu as seguintes etapas fundamentais:

### 1. Análise Exploratória de Dados (EDA)
- Identificação de padrões e correlações.  
- Observou-se que as **horas de sono** e o **nível de stresse** são os principais indicadores da qualidade do descanso.

### 2. Pré-processamento e Engenharia de Features

- **Tratamento de Dados:**  
  - Preenchimento de valores nulos na coluna `Health_Issues` (assumindo `"Healthy"` para ausência de registo).

- **Feature Engineering:**  
  - Criação da métrica derivada `Caffeine_per_Hour` para entender a densidade de cafeína em relação ao tempo de sono.

- **Transformações:**  
  - `OneHotEncoder` para variáveis categóricas (`Occupation`, `Stress_Level`, etc.).  
  - `StandardScaler` para normalizar variáveis numéricas de diferentes escalas.  
  - *Label Mapping* para a variável alvo (`Sleep_Quality`), preservando a sua natureza ordinal.

### 3. Modelação e Avaliação

Foram testados dois algoritmos para um problema de classificação multiclasse (4 categorias):

- **Regressão Logística (Baseline):**  
  - Apresentou uma performance robusta de **99% de acurácia**, demonstrando que os dados são linearmente separáveis.

- **Random Forest:**  
  - Alcançou **99% de acurácia** no teste, capturando relações não-lineares complexas.

**Veredito:**  
A **Regressão Logística** foi selecionada como o modelo final devido à sua alta performance aliada à simplicidade e facilidade de interpretação dos coeficientes.

##  Como Executar o Projeto

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/Augu5t0/Cientista-de-Dados-N-vel-1
   ```
2. **Instale as dependências:**
    ```bash
    pip install -r requirements.txt
    ```