# 📊 Telecom X – Projeto de Previsão de Churn
**Analista de Machine Learning:** Leonardo Farias  
**Contexto:** ALURA ONE | TECH FOUNDATION - Especialização Data Science

---

## 🎯 Objetivo do Projeto
Desenvolver modelos preditivos capazes de identificar clientes com alta probabilidade de evasão (**Churn**) na Telecom X, permitindo a antecipação de problemas e a criação de estratégias de retenção personalizadas.

## 🧠 Metodologia e Modelagem
O projeto percorreu as etapas de limpeza de dados, engenharia de atributos (encoding e normalização) e treinamento de modelos de classificação. Comparamos dois algoritmos principais:

| Métrica | Regressão Logística | Random Forest |
| :--- | :---: | :---: |
| **Acurácia** | **80%** | 77% |
| **Recall (Churn)** | **54%** | 44% |
| **Precisão** | 62% | 58% |

> **Decisão Técnica:** Optamos pela **Regressão Logística** devido ao seu **Recall superior**. No cenário de Churn, identificar o maior número possível de clientes em risco (mesmo com alguns alarmes falsos) é mais valioso para o negócio do que ignorar clientes que de fato cancelarão.

## 🔍 Principais Insights (Feature Importance)
A análise das variáveis revelou os fatores que mais influenciam a decisão do cliente:

* **🛡️ Retenção:** Contratos de longo prazo (1 ou 2 anos) e maior tempo de casa (*Tenure*) são os maiores aliados da fidelidade.
* **⚠️ Risco:** Clientes com **Fibra Óptica** e faturas mensais elevadas têm maior propensão à evasão, indicando sensibilidade a preço ou insatisfação com o serviço premium.



## 💡 Estratégias de Retenção Propostas
Com base nos dados, sugerimos:
1.  **Conversão de Contratos:** Incentivos para migrar clientes "mês a mês" para planos anuais.
2.  **Foco em Fibra Óptica:** Auditoria técnica e pesquisas de satisfação específicas para usuários desta tecnologia.
3.  **Monitoramento de Bill Shock:** Alertas preventivos para clientes com aumentos súbitos no valor da fatura.

## 🛠️ Tecnologias Utilizadas
* **Python** (Pandas, Scikit-Learn, Matplotlib, Seaborn)
* **Google Colab**
* **Git/GitHub** para versionamento

---
*Este projeto faz parte do portfólio de Data Science de Leonardo Farias.*
