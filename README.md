# 📊 Análise de Dados — Varejo Online

---

## Sumário Executivo

Utilizando Python e Pandas, extraí e limpei dados de transações de um varejo online e construí um dashboard visual para acompanhar o desempenho comercial. Após identificar os produtos e países com maior impacto na receita, recomendo que a equipe comercial foque seus esforços nos 10 produtos que concentram a maior parte do faturamento, e nos meses de maior volume de vendas para planejar campanhas e estoque com mais precisão.

---

## Problema de Negócio

O time comercial não tinha visibilidade clara sobre quais produtos geravam mais receita, quais países concentravam mais pedidos e como as vendas se comportavam ao longo do tempo. Sem essa visão, decisões de estoque, marketing e metas ficavam baseadas em feeling ao invés de dados.

**Perguntas que este projeto responde:**
1. Quais são os 10 produtos mais vendidos?
2. Como as vendas evoluíram mês a mês?
3. Quais produtos concentram a maior parte da receita?
4. Quantos pedidos, clientes e países foram atendidos?

---

## Metodologia

1. Leitura do dataset `varejoonline.csv` com encoding `latin-1`
2. Inspeção dos dados: shape, tipos, valores únicos, duplicatas e estatísticas descritivas
3. Limpeza: remoção de linhas duplicadas (5.268 removidas de 541.909)
4. Criação de coluna `Receita` = `Quantity × UnitPrice`
5. Agrupamentos por produto, país e mês para alimentar os gráficos
6. Construção do dashboard visual com Matplotlib

---

## Habilidades

**Python:** Pandas, Matplotlib, Numpy, limpeza de dados, agrupamentos, visualização

**Análise de Dados:** Estatística descritiva, análise de receita, séries temporais, ranking de produtos

---

## Resultados e Recomendação de Negócio

O dashboard revelou que:

- **541.909 transações** foram registradas, com **5.268 duplicatas** removidas
- O portfólio tem **4.070 produtos** distintos vendidos em **38 países**
- Os **Top 10 produtos** concentram uma parcela significativa da receita total
- As vendas apresentam **crescimento ao longo do ano**, com pico nos meses finais

Com base na análise, recomendo:

1. Priorizar estoque e campanhas nos **Top 10 produtos de maior receita**
2. Planejar ações comerciais para os **meses de menor volume** de vendas
3. Focar esforços de expansão nos **países com maior número de pedidos**
4. Automatizar o monitoramento mensal com atualização do dashboard

---

## Próximos Passos

1. Adicionar filtros interativos ao dashboard (por país e período)
2. Construir modelo de previsão de vendas mensais
3. Análise de churn de clientes com base na frequência de compras
4. Integrar com banco de dados para atualização automática dos dados

---

## 📁 Estrutura do Projeto

```
Kmeans/
├── main.py                # Código principal do dashboard
├── varejoonline.csv       # Dataset com as transações
├── dashboard_varejo.png   # Dashboard completo
├── resultado_analise.png  # Gráfico de resultados para o README
└── README.md              # Documentação do projeto
```

---

## 🗂️ Sobre o Dataset

| Coluna      | Descrição                    |
|-------------|------------------------------|
| InvoiceNo   | Número da fatura             |
| StockCode   | Código do produto            |
| Description | Descrição do produto         |
| Quantity    | Quantidade vendida           |
| InvoiceDate | Data da venda                |
| UnitPrice   | Preço unitário               |
| CustomerID  | ID do cliente                |
| Country     | País do cliente              |

---

## 🛠️ Tecnologias

![Python](https://img.shields.io/badge/Python-3.14-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.x-purple?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.x-orange)
