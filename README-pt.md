Segmentação de Clientes com K-Means
==================================

Este projeto foi pensado para demonstrar habilidades relevantes para **times de Data Science em bancos e fintechs**.

- **Visão de negócio**: os resultados de clusterização são traduzidos em linguagem de negócio (risco, engajamento, oportunidade de receita), e não ficam apenas em métricas técnicas.  
- **Boas práticas de modelagem**: uso de normalização, escolha justificada do número de clusters e validação com métricas adequadas de clusterização.  
- **Comunicação clara**: visualizações e personas que permitem que áreas não técnicas (CRM, Risco, Produtos) entendam rapidamente os segmentos.  
- **Aplicabilidade real**: o código está organizado para ser facilmente adaptado a bases internas de cartão/crédito e integrado em pipelines analíticos ou projetos de CRM, risco e marketing.  

## Objetivo

- Agrupar clientes com base no comportamento de uso do cartão.  
- Avaliar o número ideal de clusters com **Inércia (WCSS)** e **Silhouette Score**.  
- Traduzir clusters técnicos em **segmentos de negócio acionáveis**.  

## Fonte dos Dados

Os dados foram obtidos no Kaggle, no desafio **“Credit Card Dataset for Clustering”**.  
A base resume o comportamento de uso de cerca de **9.000 portadores de cartão de crédito ativos** ao longo dos últimos **seis meses**.  

## Pipeline do Projeto

1. **Limpeza e exploração de dados**  
   - Tratamento de valores ausentes, outliers e geração de estatísticas descritivas.  

2. **Padronização das variáveis**  
   - Utilização de `StandardScaler` para padronizar as variáveis numéricas.  

3. **Definição do número de clusters (K)**  
   - Uso da curva do cotovelo (**WCSS**) e do **Silhouette Score**.  

4. **Treinamento do modelo**  
   - Aplicação do **K-Means** e criação da coluna `CLUSTER`.  

5. **Análise dos clusters**  
   - Estatísticas médias por cluster e visualizações (gráficos de barras, gráfico radar).  

## RESULTADOS:

### Cluster 0 – High Spenders (Altos Gastadores)

Alto volume de compras e pagamentos, boa taxa de pagamento total e forte potencial para ofertas premium e aumento de limite.  

### Cluster 1 – Low Engagers (Baixo Engajamento)

Baixo uso do cartão, valores moderados e foco em campanhas de ativação e aumento de engajamento.  

### Cluster 2 – Cash Advance Users (Usuários de Saque)

Uso intenso de saque em dinheiro, menor uso em compras e baixa taxa de pagamento total, relevante para gestão de risco e políticas de crédito.
