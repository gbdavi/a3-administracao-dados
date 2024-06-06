
# A3 - Análise de Dados

**Professores:**  Henrique Ruiz Poyatos Neto e Aran Bey Tcholakian Morales.

**Alunos:** Charles Freire Santana, Davi Gramm Bauer, Felipe Fernandes de Aquino, Joseph Bertola Leite, Patrick Azrael Silva Carvalho e Pedro Henrique Ostroski.

## Tema
 
 Analisar o impacto da dengue no Sistema Único de Saúde (SUS) e no PIB dos estados no período de 2014 a 2019.

## Base de Dados

 Para o desenvolvimento deste trabalho, utilizaremos três bases de dados:

1.  **Ocupação de Leitos:** Utilizamos o Portal de Dados Abertos do Governo Federal para apurar a ocupação de leitos no período de 2014 a 2019 em todo o território nacional.
2.  **Despesa com Saúde:** Utilizamos a base do IBGE para apurar o impacto financeiro com a ocupação dos leitos.
3.  **Dengue no Brasil:** Utilizamos o dataset “Brazil Dengue Dataset 2000-2019” disponível no Kaggle para obter a quantidade de casos no Brasil e qual é seu impacto nos leitos e na economia.

## KPIs:

Pretendemos desenvolver os seguintes KPIs:

1.  **Número de Casos:** a. Casos Novos b. Casos Acumulados c. Incidência d. Prevalência
2.  **Taxas de Mortalidade:** a. Taxa de Mortalidade Bruta b. Taxa de Mortalidade Específica por Doença
3.  **Internações Hospitalares:** a. Número de Internações b. Taxa de Ocupação de Leitos
4.  **Testes Diagnósticos:** a. Número de Testes Realizados b. Taxa de Positividade c. Tempo Médio para o Resultado do Teste
5.  **Impacto Social e Econômico:** a. Absenteísmo no Trabalho b. Mortes Evitáveis c. Custos Econômicos

## Ferramenta de Dados

Utilizaremos o Power BI para o tratamento dos dados e divulgação dos indicadores.

## Tratamento dos Dados

 Realizamos as seguintes ações nas bases de dados:

-   **Base da Dengue:** Promovemos a primeira linha a cabeçalho, alteramos os tipos de dados nas colunas numéricas e substituímos os erros gerados na alteração de tipo de dado nas colunas numéricas por 0.
-   **Base do PIB:** Excluímos as colunas inutilizadas, removemos os espaços desnecessários nos campos, alteramos o tipo nas colunas de PIB para numérico, removemos as primeiras linhas e algumas colunas que não tinham informações relevantes, promovemos a primeira linha a cabeçalho e renomeamos a coluna de locais.