# 📊 Telecom X - Parte 2: Previsão de Churn com Machine Learning

## 🎯 1. Propósito da Análise
O objetivo principal deste projeto é desenvolver modelos preditivos capazes de identificar clientes com alta probabilidade de cancelamento (**Churn**) na Telecom X. Através da análise de variáveis comportamentais e contratuais, buscamos antecipar a evasão e fornecer subsídios para estratégias de retenção baseadas em dados.

---

## 📂 2. Estrutura do Projeto
A organização dos arquivos segue o padrão de projetos de Data Science:

* `Telecom_X_churn_ml.ipynb`: Notebook principal com todo o pipeline de desenvolvimento.
* `data/`: Pasta contendo o dataset em CSV utilizado no projeto.
* `models/`: Pasta com os modelos treinados (arquivos .pkl ou .joblib).
* `visualizations/`: Gráficos gerados durante a análise exploratória (EDA) e avaliação de modelos.
* `requirements.txt`: Lista de bibliotecas necessárias para replicar o ambiente.

---

## ⚙️ 3. Preparação dos Dados
Para garantir a performance dos modelos, os dados passaram por um rigoroso processo de pré-processamento:

* **Classificação de Variáveis:**
    * **Numéricas:** `tenure` (meses de contrato), `MonthlyCharges` (valor mensal) e `TotalCharges` (valor total).
    * **Categóricas:** Gênero, tipo de contrato, método de pagamento e serviços assinados (Internet, TV, etc).
* **Normalização e Codificação:**
    * Utilizamos **Label Encoding** para variáveis binárias.
    * Aplicamos **One-Hot Encoding** para variáveis categóricas com múltiplas classes para evitar hierarquias falsas.
    * As variáveis numéricas foram **normalizadas** (ou padronizadas) para garantir que escalas diferentes (ex: meses vs reais) não enviesassem o modelo.
* **Separação dos Dados:**
    * Os dados foram divididos em **70% para treino** e **30% para teste**, garantindo uma avaliação imparcial do desempenho em dados nunca vistos pelo modelo.

---

## 🧠 4. Modelagem e Justificativas
Nesta etapa, focamos na interpretabilidade e na capacidade de detecção:

* **Modelos Utilizados:** Regressão Logística e Random Forest.
* **Escolha do Modelo Final:** A **Regressão Logística** foi selecionada como modelo oficial.
* **Justificativa:** No contexto de Churn, o custo de "não ver" um cliente que vai sair é muito maior do que o custo de uma ação de retenção preventiva. Por isso, priorizamos o **Recall (54%)** em detrimento apenas da acurácia bruta, pois a Regressão Logística mostrou-se mais sensível para detectar a classe minoritária (quem cancela).

---

## 📈 5. Insights da Análise Exploratória (EDA)
Durante a exploração, identificamos padrões críticos:

* **Contrato Mês a Mês:** É o maior impulsionador de churn. Clientes sem fidelidade anual saem com muito mais facilidade.
* **Serviço de Fibra Óptica:** Apresentou taxas de evasão acima da média, sugerindo necessidade de revisão técnica ou de preço.
* **Tenure Inicial:** Os primeiros 6 meses de contrato são o período de maior risco para a Telecom X.



---

## 🚀 6. Como Executar o Projeto

1.  **Pré-requisitos:**
    Certifique-se de ter o Python instalado. Recomenda-se o uso do Google Colab para execução em nuvem.
    
2.  **Instalação de Dependências:**
    No terminal ou célula do notebook, execute:
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn
    ```

3.  **Carregamento de Dados:**
    O notebook está configurado para ler o arquivo diretamente do diretório `/content/` ou via montagem do Google Drive. Caso utilize localmente, altere o caminho no comando `pd.read_csv()`.

---
*Este projeto foi desenvolvido como parte do desafio de Machine Learning da Telecom X - ALURA ONE.*
