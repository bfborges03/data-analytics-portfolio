# Modelo de Priorização de Desvios Orçamentários em G&A

## Sobre o projeto

Este projeto explora o uso de análise de dados e Machine Learning para apoiar a identificação e a priorização de desvios entre valores orçados e realizados nas despesas de G&A (*General & Administrative*).

A proposta é transformar dados históricos de fechamento financeiro em informações que auxiliem a área de FP&A a identificar contas que merecem maior atenção, considerando a magnitude dos desvios, sua recorrência e a volatilidade dos valores ao longo do tempo.

## Objetivos

- Analisar a variação entre valores orçados e realizados.
- Identificar desvios relevantes com base em critérios estatísticos.
- Desenvolver um modelo de classificação para apoiar a priorização de desvios.
- Agrupar contas por características de comportamento, utilizando técnicas de clustering.
- Gerar uma tabela de priorização para apoiar a análise financeira.

## Metodologia

O notebook está organizado nas seguintes etapas:

1. **Preparação dos dados:** estruturação de informações por departamento, conta contábil e período.
2. **Engenharia de atributos:** criação de variáveis relacionadas à recorrência de desvios e à volatilidade das contas.
3. **Identificação de desvios relevantes:** definição de um critério estatístico baseado no percentil 80 da magnitude dos desvios.
4. **Classificação:** aplicação de Regressão Logística como modelo de classificação e geração de scores para apoiar a priorização.
5. **Segmentação:** utilização do algoritmo K-Means para agrupar contas com comportamentos semelhantes.
6. **Priorização:** consolidação dos resultados em uma tabela ordenada por score.

## Tecnologias utilizadas

- Python
- Pandas
- Scikit-learn
- Google Colab
- Google Sheets / BigQuery como fontes alternativas previstas no código

## Dados

O notebook contempla uma base sintética para simulação e teste do fluxo analítico, além de alternativas para leitura de dados de Google Sheets ou BigQuery, mediante configuração.

Os resultados obtidos com dados sintéticos são demonstrativos e não representam resultados financeiros reais de uma organização.

## Como executar

1. Abra o notebook `modelo_priorizacao_desvios.ipynb` neste repositório.
2. Selecione a opção de abrir ou executar no Google Colab.
3. Autorize o acesso à sua conta Google, quando solicitado.
4. Configure a fonte de dados desejada.
5. Execute as células na sequência apresentada.

Para utilizar dados reais, configure a fonte e as permissões necessárias antes da execução.

## Resultados esperados

O fluxo analítico produz indicadores de variação orçamentária, atributos de comportamento das contas, classificação de desvios e uma tabela final de priorização.

A solução é um protótipo analítico para apoiar a investigação financeira. Os scores devem ser interpretados como indicadores do modelo, e não como garantia de risco financeiro ou de impacto monetário.

## Próximos passos

- Avaliar o desempenho do classificador com métricas adequadas.
- Revisar a convergência e a preparação das variáveis do modelo.
- Validar os critérios de relevância com especialistas de FP&A.
- Testar a abordagem com dados reais autorizados.
- Evoluir a solução para apoiar rotinas recorrentes de acompanhamento orçamentário.
