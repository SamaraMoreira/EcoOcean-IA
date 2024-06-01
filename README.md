## EcoOcean
# Conjunto de Dados "Poluição da Água nos Países da UE"

Este conjunto de dados fornece informações sobre a poluição da água nos países da União Europeia, incluindo fatores como turismo, taxa de alfabetização e disposição de resíduos. Os dados abrangem o período de 1990 a 2020.

- **Link**: [Conjunto de Dados de Poluição da Água](https://www.kaggle.com/datasets/hydramst/water-pollution)

## Colunas
- **Código**: Código único do determinante controlado.
- **Ano**: Ano da seleção dos dados.
- **Período**: Período do ano para seleção de dados.
- **ID**: Identificador internacional único do corpo d'água.
- **País**: Informações do país geradas usando coordenadas.
- **Turistas**: Número médio de turistas no país de 1990 a 2020.
- **Estabelecimentos**: Número de estabelecimentos próximos às coordenadas indicadas.
- **Taxa**: Taxa de alfabetização no país de 2010 a 2018.
- **Alimento**: Percentual de resíduos alimentares.
- **Vidro**: Percentual de resíduos de vidro.
- **Metal**: Percentual de resíduos de metal.
- **Outros**: Percentual de outros resíduos.
- **Papel**: Percentual de resíduos de papel.
- **Plástico**: Percentual de resíduos de plástico.
- **Couro**: Percentual de resíduos de couro.
- **Resíduos Verdes**: Percentual de resíduos verdes.
- **Reciclagem de Resíduos**: Percentual de lixo processado.
  
- **Análise:**
  - Após análise dos gráficos e informações geradas, foi observado que os países com os maiores registros de lixo são:
    1. France
    2. Spain
    3. United Kingdom
---
## Conjunto de Dados "Avaliação da Poluição Costeira"

### Visão Geral
Este conjunto de dados avalia os níveis de poluição ao longo das áreas costeiras. Ele inclui vários fatores ambientais, como pH do solo, pH da água, salinidade, temperatura e níveis de poluição.

- **Link**: [Conjunto de Dados de Avaliação da Poluição Costeira](https://www.kaggle.com/datasets/tzachymorad/shore-pollution-assessment)

### Colunas
- **Mês**: Mês em que a amostra foi coletada.
- **Estação**: Estação do ano em que a amostra foi coletada.
- **Costa**: Localização da amostra na costa.
- **Nível de Poluição**: Nível de poluição na amostra.
- **Número da Amostra**: Número da amostra.
- **Matéria Orgânica%**: Percentual de matéria orgânica na amostra.
- **Número Médio de Espécies de Nematoides 1 por Grama de Solo**: Número médio de espécies de nematoides 1 por grama de solo.
- **Número Médio de Turbilhões por Grama de Solo**: Número médio de Turbilhões por grama de solo.
- **Número Médio de Foraminíferos por Grama de Solo**: Número médio de foraminíferos por grama de solo.
- **Número Médio de Espécies de Nematoides 2 por Grama de Solo**: Número médio de espécies de nematoides 2 por grama de solo.
- **pH da Água**: pH da água.
- **pH do Solo**: pH do solo.
- **OC**: Índice de carbono orgânico.
- **Salinidade da Água**: Salinidade da água.
- **Salinidade do Solo**: Salinidade do solo.
- **P**: Fósforo na amostra.
- **Sólidos Totais Dissolvidos**: Sólidos totais dissolvidos na amostra.
- **PP**: Índice PP.
- **Condução**: Condutividade elétrica.
- **ORP**: Potencial de oxirredução (ORP).
- **Resistência Específica**: Resistência específica.
- **Temperatura**: Temperatura em Celsius.
- **Condutividade**: Condutividade.
- **H**: Hidrogênio na amostra.
- **C-A**: Índice C-A.
- **C-B**: Índice C-B.
- **C-C**: Índice C-C.
---
### Integração de Dados

- **União dos Datasets:**
  - Com base nos países identificados com os maiores registros de lixo no conjunto de dados "Water Pollution in EU Countries", esses países foram considerados como as costas no conjunto de dados "Coast Pollution Assessment".
  - Os nomes dos países foram substituídos por suas numerações correspondentes, conforme listado acima.
  - Assim, conseguimos relacionar os registros de lixos com o nível de poluição.
---
## Análise

### Primeira Hipótese: Tendências Temporais
Observamos padrões sazonais na coleta de resíduos, com picos em janeiro, março e maio, e uma diminuição significativa durante os meses intermediários, retomando apenas em agosto.

### Segunda Hipótese: Correlação de Variáveis Ambientais com Níveis de Poluição
- **pH**: O pH da água tem uma correlação negativa moderada com os níveis de poluição, indicando uma redução na poluição com o aumento do pH da água.
- **Salinidade**: Tanto a salinidade da água quanto a do solo exibem correlações negativas significativas com os níveis de poluição, sugerindo uma possível redução nos níveis de poluição em ambientes mais salinos.
- **Temperatura e Condutividade**: A temperatura e a condutividade mostram correlações fracas a moderadas com os níveis de poluição, indicando uma possível redução nos níveis de poluição com o aumento da condutividade.

### Relação entre Coleta de Resíduos e Níveis de Poluição
- Observamos fortes correlações positivas entre certos tipos de resíduos, como metal, plástico, resíduos orgânicos e reciclagem de resíduos, sugerindo que esses tipos são frequentemente coletados juntos.
- Também observamos correlações negativas entre vidro e outros tipos de resíduos, indicando diferentes padrões de coleta.

### Análise da Relação entre Número de Turistas e Coleta de Resíduos
- Uma correlação positiva forte foi observada entre o número de turistas e vários tipos de resíduos, sugerindo que áreas com mais turistas tendem a produzir mais resíduos.
- Uma correlação negativa foi observada entre o número de turistas e resíduos metálicos, sugerindo que áreas com mais atividade turística têm menos desses resíduos.

Essas análises destacam a importância da gestão eficaz de resíduos e políticas de sustentabilidade, especialmente em áreas turísticas, visando promover práticas mais sustentáveis.


## Modelo de Machine Learning

O Random Forest é um modelo de aprendizado de máquina que utiliza uma combinação de múltiplas árvores de decisão para fazer previsões. Ele é conhecido por sua capacidade de lidar com conjuntos de dados complexos e grandes, além de ser menos propenso a overfitting em comparação com modelos lineares, como a Regressão Linear.

Neste caso, o Random Forest conseguiu ajustar-se melhor aos dados, resultando em previsões mais precisas em comparação a outros modelos. Isso pode ser devido à natureza não linear dos dados ou à presença de interações complexas entre as features.

Essas são as características mais importantes, classificadas pelo nosso modelo com base em suas importâncias:

1. **glass**: Esta característica tem uma importância de aproximadamente 0.31, sugerindo que a participação de resíduos de vidro está fortemente associada à predição da variável de interesse.

2. **paper**: Com uma importância próxima a 0.29, a participação de resíduos de papel também é uma característica significativa na predição da variável de interesse.

3. **turistas**: Com uma importância de cerca de 0.27, o número médio de turistas parece ser uma das características mais importantes, indicando uma forte relação entre o número de turistas e a poluição.

4. **Total dissolved solids**: Esta característica tem uma importância de aproximadamente 0.02, sugerindo que os sólidos totais dissolvidos também desempenham um papel na predição da poluição.

5. **green_waste**: Com uma importância semelhante à dos sólidos dissolvidos totais, em torno de 0.02, a participação de resíduos verdes também é uma característica significativa.

6. **food**: A participação de resíduos alimentares tem uma importância em torno de 0.02, sugerindo sua contribuição para a predição da variável de interesse.

7. **plastic**: Com uma importância semelhante à de resíduos alimentares, em torno de 0.02, a participação de resíduos plásticos também é relevante.

8. **other**: Esta característica tem uma importância de cerca de 0.01, indicando que outros tipos de resíduos também têm um papel na predição da poluição.

9. **Water Salinity**: Com uma importância de aproximadamente 0.01, a salinidade da água também é uma característica relevante.

10. **waste_recycling**: Com uma importância próxima a 0.01, a participação de resíduos recicláveis também é uma característica significativa na predição da poluição.

Essas informações são úteis para entender quais características têm maior influência na predição da poluição e podem orientar futuras estratégias de monitoramento e mitigação.
