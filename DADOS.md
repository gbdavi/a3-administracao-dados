
# Dados utilizados

## [Pasta com arquivos prontos](https://drive.google.com/drive/folders/1kFDYWXZu2kvP17e8iDi5GEih5xzYjrWm?usp=sharing)

## [Dados sobre a dengue (2000 - 2019)](https://www.kaggle.com/datasets/raomuhammadsaeedali/brazil-dengue-dataset-2000-2019)

## [Dados sobre leitos (2014 - 2019)](https://dados.gov.br/dados/conjuntos-dados/hospitais-e-leitos)

1. Expandir a aba ***Recursos***;
2. Baixar os arquivos ***Leitos 20xx*** do ano de 2014 até 2019;
3. Agrupar os arquivos em um único arquivo.

### Código PowerShell para agrupar os arquivos no Windows

```ps1
$outputFile = "leitos14-19.csv"
$inputFiles = @("Leitos_2014.csv", "Leitos_2015.csv", "Leitos_2016.csv", "Leitos_2017.csv", "Leitos_2018.csv", "Leitos_2019.csv")
$headerWritten = $false

foreach ($file in $inputFiles) {
    Write-Output "Processing $file..."

    $content = Get-Content -Path $file

    if (-not $headerWritten) {
        $content | Out-File -FilePath $outputFile -Encoding utf8 -Append
        $headerWritten = $true
    } else {
        $content[1..$content.Length] | Out-File -FilePath $outputFile -Encoding utf8 -Append
    }
}

Write-Output "Merge complete! Output file: $outputFile"
```

## [Dados sobre o PIB do Brasil (2002 - 2021)](https://www.ibge.gov.br/estatisticas/economicas/contas-nacionais/9054-contas-regionais-do-brasil.html?=&t=downloads)

1. Baixar zip do caminho: ***2021***  &rarr; ***xls*** &rarr; ***Especiais_2002_2021_xls.zip***;
2. Extrair zip;
3. Utilizar o arquivo ***tab01.xls***.
