Projeto Crédito Rural Brasil com PySpark

# Relatório — Projeto Crédito Rural Brasil com PySpark

## 1. Problema e Dataset  
1. Problema: analisar a distribuição e evolução do crédito rural no Brasil, identificando padrões e perfis de estados/regiões.  
2. Dataset: dados públicos do Banco Central (SICOR), obtidos via API Olinda.  

## 2. Pré-processamento  
1. Tratamento de valores nulos (`na.fill(0)`).  
2. Remoção de duplicatas.  
3. Criação da coluna `VL_TOTAL` (soma das modalidades).  
4. Conversão de tipos e indexação de variáveis categóricas.  

## 3. Análise Exploratória (Spark SQL)  
1. Estados com maior volume de crédito rural.  
2. Evolução anual do crédito rural.  
3. Evolução mensal do crédito rural.  
4. Crédito por região.  
5. Programas e fontes de recurso mais relevantes.  
6. Modalidades líderes (custeio, investimento, comercialização, industrialização).  

## 4. Modelagem Preditiva  
1. Variável alvo: `FAIXA_CREDITO` (faixas de volume).  
2. Modelos treinados: Árvore de Decisão e Random Forest.  
3. Métricas utilizadas: acurácia e F1.  
4. Resultado: Random Forest apresentou melhor desempenho.  

## 5. Modelagem Descritiva (Clusterização)  
1. Técnica aplicada: K-Means com K=3.  
2. Avaliação: Silhouette Score satisfatório.  
3. Interpretação dos clusters:  
   - Cluster 0: estados com alto volume.  
   - Cluster 1: perfil intermediário e diversificado.  
   - Cluster 2: menor participação.  

## 6. Conclusões e Limitações  
1. Conclusões:  
   - Há concentração de crédito em determinadas regiões.  
   - Modalidades de custeio e investimento dominam os recursos.  
   - Evolução positiva ao longo dos anos.  
2. Limitações: dataset restrito a registros disponíveis via API; ausência de variáveis socioeconômicas complementares.  
3. Próximos passos: integrar dados de produtividade agrícola, clima e políticas públicas para análises mais completas.  


Limitações: dataset restrito a registros disponíveis via API; ausência de variáveis socioeconômicas complementares.

Próximos passos: integrar dados de produtividade agrícola, clima e políticas públicas para análises mais completas.
