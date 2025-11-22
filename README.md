Projeto de Análise de E-commerce: Receita e Logística

## 1. Objetivo

O propósito deste projeto é atuar como o Time de Dados de um e-commerce brasileiro para fornecer à diretoria respostas analíticas e estatisticamente confiáveis sobre a saúde financeira e a eficiência operacional da empresa.

O objetivo final é entregar um Relatório Analítico (PDF/MD) e um notebook Python/SQL reprodutível que contemple:
* Análise Descritiva e Exploratória de Dados (EDA).
* Tratamento Estatístico (Inferência: Intervalos de Confiança).
* Geração de KPIs (Key Performance Indicators) acionáveis.

---

## 2. Abordagem e Metodologia

Estruturamos o trabalho em um pipeline robusto para garantir a integridade, qualidade e reprodutibilidade dos resultados.

O pipeline de análise segue um fluxo de trabalho em camadas:

1.  **Ingestão e Integração de Dados:** Processo de leitura, validação de esquema (chaves) e unificação das fontes dimensionais e fatos.
2.  **Preparação e Enriquecimento:** Padronização de tipos de dados (Datas/Numéricos) e criação de variáveis derivadas cruciais para o negócio (Atraso, Tempo de Entrega, Participação do Frete).
3.  **Análise e Validação Estatística:** Aplicação de Análise Exploratória (EDA) e testes de inferência para quantificar métricas-chave com rigor estatístico.
4.  **Entrega de Insights:** Tradução dos achados estatísticos em conclusões de negócio claras para o Sumário Executivo.

---

## 3. Estrutura do Repositório

O repositório está organizado para garantir a clareza e a reprodutibilidade do projeto.

* `data/`: Arquivos CSV brutos foRrnecidos.
* `notebooks/`: Arquivo principal de desenvolvimento e análise (`main_analysis.ipynb`).
* `reports/`: Destinado ao Relatório Final e materiais de apoio.

---

## 4. Fontes de Dados

A análise é baseada em 5 arquivos CSV que contêm o histórico de transações e dimensões de negócio:

| Arquivo | Entidade Principal | Chaves de Conexão |
| :--- | :--- | :--- |
| `FACT_Orders.csv` | Transações e Fatos (Nível de Item) | Ponto de partida para a análise. |
| `DIM_Delivery.csv` | Detalhes Logísticos | `Delivery_Id` |
| `DIM_Customer.csv` | Detalhes do Cliente | `Customer_Id` |
| `DIM_Shopping.csv` | Itens e Preços (por Linha de Pedido) | Ligação com `FACT_Orders` por ID. |
| `DIM_Products.csv` | Descrição de Produtos | `Product_Name` (Nome do Produto) |