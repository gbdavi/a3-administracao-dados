
# Dados utilizados

## [Pasta com arquivos prontos](https://drive.google.com/drive/folders/1kFDYWXZu2kvP17e8iDi5GEih5xzYjrWm?usp=sharing)

## [Dados sobre a dengue (2000 - 2019)](https://www.kaggle.com/datasets/raomuhammadsaeedali/brazil-dengue-dataset-2000-2019)

## [Dados sobre leitos (2014 - 2019)](https://dados.gov.br/dados/conjuntos-dados/hospitais-e-leitos)

1. Expandir a aba ***Recursos***;
2. Baixar os arquivos ***Leitos 20xx*** do ano de 2014 até 2019;
3. Agrupar os arquivos em um único arquivo e fazer tratamento.

### Código Python para agrupar e tratar os dados

```py
import os
import pandas
import numpy


# Listar todos os arquivos csv
files = [file for file in os.listdir() if file[-4:] == ".csv"]

# Juntar arquivos
filesDf = []
for csv in files:
    filesDf.append( pandas.read_csv(csv) )
df = pandas.concat(filesDf)

# Pegar dados do ultimo mes do ano
df = df.loc[df["COMP"] % 100 == 12]
df["ANO"] = numpy.floor( df["COMP"] / 100 ).astype("int")

# Salvar dataframe em csv
df.to_csv("Leitos anual.csv", index=False)
```

## [Dados sobre o PIB do Brasil (2002 - 2021)](https://www.ibge.gov.br/estatisticas/economicas/contas-nacionais/9054-contas-regionais-do-brasil.html?=&t=downloads)

1. Baixar zip do caminho: ***2021***  &rarr; ***xls*** &rarr; ***Especiais_2002_2021_xls.zip***;
2. Extrair zip;
3. Utilizar o arquivo ***tab01.xls***.
