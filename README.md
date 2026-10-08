Markdown
# 🎮 Videogame Market Analytics — Análise Estratégica & Testes de Hipóteses

![Python](https://img.shields.io/badge/Python-3873A9?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-ffffff?style=for-the-badge&logo=matplotlib&logoColor=black)
![Seaborn](https://img.shields.io/badge/Seaborn-7DB0DD?style=for-the-badge&logo=seaborn&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

---

## 📌 Visão Geral & Problema de Negócio

Este projeto assume o papel de um **Analista de Dados** atuando para a loja online de jogos eletrônicos **Ice**.

Simulando o cenário de **dezembro de 2016**, o objetivo principal é realizar um diagnóstico profundo sobre os dados históricos de vendas globais de videogames para identificar padrões de sucesso comercial, avaliar o comportamento e ciclo de vida de plataformas e gêneros, e **fundamentar a alocação de orçamento de marketing, planejamento financeiro e estoque para o ano de 2017**.

### Questões Estratégicas Respondidas:
1. Quais plataformas estão em ascensão e quais já atingiram o fim de seu ciclo de vida comercial?
2. Como as avaliações da crítica e dos usuários impactam o volume de vendas globais de um jogo?
3. Quais são os perfis regionais de consumo (América do Norte, Europa e Japão) em termos de plataformas, gêneros e classificação etária (ESRB)?
4. Existe diferença estatisticamente significativa entre as avaliações médias dos usuários para plataformas concorrentes (Xbox One vs. PC) e entre gêneros populares (Action vs. Sports)?

---

## 🛠️ Tecnologias & Ferramentas

* **Linguagem de Programação:** Python 3.x
* **Manipulação e Tratamento de Dados:** `Pandas`, `NumPy`
* **Visualização de Dados:** `Matplotlib`, `Seaborn`
* **Estatística Inferencial & Testes de Hipóteses:** `SciPy` (`scipy.stats`)
* **Ambiente de Desenvolvimento:** Jupyter Notebook

---

## 📂 Estrutura do Repositório

```text
├── games.csv              # Dataset histórico de vendas, avaliações e classificações de jogos
├── notebook.ipynb         # Notebook principal com tratamento de dados, EDA, perfil regional e testes $t$
└── README.md              # Documentação executiva do projeto
