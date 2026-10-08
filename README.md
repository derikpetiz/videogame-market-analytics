# 🎮 Videogame Market Analytics: Análise de Mercado & Testes de Hipóteses

---

## 📌 Contexto & Objetivo
A Ice é uma loja online de videogames que vende para todo o mundo. O objetivo deste projeto é realizar uma Análise Exploratória de Dados (EDA) e testes de hipóteses estatísticas sobre dados históricos de vendas de jogos até dezembro de 2016, com o fim de identificar padrões de sucesso comercial, perfis regionais de consumo e prever as tendências de mercado para planejar o orçamento e a logística do ano de 2017.

---

## 📊 Análise Visual & Principais Insights

- Identificação do ciclo de vida das plataformas de jogos e seleção do período recente (2013–2016) como janela analítica relevante para projeção de 2017.
- Mapeamento das divergências culturais de consumo entre América do Norte, Europa e Japão.

---

### 1. Ciclo de Vida e Tendência de Vendas das Plataformas
![Vendas Totais por Plataforma](assets/videogame_sales_by_platform.png)

- **Hipótese:** As plataformas de jogos possuem um ciclo de vida útil limitado e consoles da nova geração (PS4 e Xbox One) estão no pico de crescimento, enquanto a geração anterior está em declínio acentuado.
- **Conclusão:** O ciclo de vida médio de um console até o declínio total é de **8 a 10 anos**, com o pico de vendas ocorrendo entre **4 e 6 anos** após o lançamento. Para o planejamento de 2017, **PS4** e **Xbox One** despontam como as plataformas mais lucrativas e em fase de sustentação de vendas.

---

### 2. Impacto das Avaliações da Crítica vs. Usuários nas Vendas
![Avaliações da Crítica e Vendas no PS4](assets/videogame_critic_vs_sales.png)

- **Hipótese:** Avaliações altas de críticos especializados e de usuários possuem forte correlação positiva com o volume total de vendas globais de um jogo.
- **Conclusão:** A pontuação da crítica (`critic_score`) apresenta uma correlação positiva moderada com as vendas ($r \approx 0,40$), atuando como um importante vetor de atração comercial. Por outro lado, a nota dos usuários (`user_score`) possui correlação próxima de zero, demonstrando que a avaliação do público final não determina diretamente o volume faturado de um título.

---

### 3. Distribuição das Vendas por Gênero nos Mercados Regionais (NA, EU, JP)
![Participação de Gêneros por Região](assets/videogame_regional_genres.png)

- **Insight Chave:** Os mercados da **América do Norte (NA)** e **Europa (EU)** são extremamente semelhantes, com absoluta liderança dos gêneros **Action** e **Shooter** e preferência por jogos de classificação etária **M (Mature 17+)**. Em contrapartida, o mercado do **Japão (JP)** exibe um comportamento único, dominado por consoles portáteis (**Nintendo 3DS**), gênero **Role-Playing (RPG)** e títulos sem classificação ESRB devido à regulação local.

---

## 🔎 Metodologia & Etapas
1. **Tratamento e Limpeza de Dados:**
   - Padronização dos nomes das colunas para letras minúsculas.
   - Conversão e tratamento do valor `'tbd'` (To Be Determined) na coluna `user_score` para `NaN` e alteração do tipo para `float64`.
   - Preenchimento de dados ausentes na coluna de classificação `rating` com a categoria `'Unknown'` para preservar a representatividade do mercado japonês.
   - Cálculo do total de vendas globais multiplicando e somando as colunas regionais (`NA_sales`, `EU_sales`, `JP_sales`, `Other_sales`).

2. **Análise Exploratória (EDA):**
   - Avaliação do volume de lançamentos por ano e identificação do período relevante (2013–2016).
   - Análise de dispersão, média e mediana de vendas por plataforma, evidenciando a presença de *blockbusters* que elevam a média em relação à mediana.
   - Construção do perfil de cliente para cada região (NA, EU, JP): top 5 plataformas, top 5 gêneros e distribuição por classificação ESRB.

3. **Teste de Hipóteses Estatísticas:**
   - **Hipótese 1 (Xbox One vs. PC):** 
     - $H_0$: As classificações médias dos usuários para as plataformas Xbox One e PC são iguais.
     - $H_1$: As classificações médias dos usuários para as plataformas Xbox One e PC são diferentes.
     - *Resultado:* Não rejeitamos $H_0$ ($p\text{-value} = 0,1476 > 0,05$). As avaliações médias de usuários entre Xbox One e PC são estatisticamente equivalentes.
   - **Hipótese 2 (Gêneros Action vs. Sports):**
     - $H_0$: As classificações médias dos usuários para os gêneros Action e Sports são iguais.
     - $H_1$: As classificações médias dos usuários para os gêneros Action e Sports são diferentes.
     - *Resultado:* Rejeitamos $H_0$ ($p\text{-value} = 1,45 \times 10^{-20} < 0,05$). O gênero Action possui avaliações médias de usuários significativamente superiores ao gênero Sports.

---

## 🛠️ Tecnologias e Ferramentas Utilizadas
- **Linguagem:** Python
- **Bibliotecas:** Pandas, NumPy, Matplotlib, Seaborn, SciPy (`scipy.stats`)
- **Ambiente:** Jupyter Notebook

---

## 🚀 Como Executar o Projeto
1. Clone o repositório:
   ```bash
   git clone [https://github.com/derikpetiz/videogame-market-analytics.git](https://github.com/derikpetiz/videogame-market-analytics.git)
   cd videogame-market-analytics
