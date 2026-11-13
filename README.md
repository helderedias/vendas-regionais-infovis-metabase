# Dashboard Interativo: Vendas Regionais — 3º Trimestre 2026

Projeto desenvolvido para a disciplina de **Visualização de Dados** (Curso Superior de Tecnologia em Gestão de Dados — **UFPI**), sob orientação do docente **Iúre de Sousa Fé**.

**Autores:**
* Hélder Estevão Dias
* Aluísio Alves Lima

---

## Objetivo e Arquitetura

Desenvolver um painel analítico interativo no **Metabase** conectado a uma base de dados **PostgreSQL 12** (`Vendas Regionais InfoVis`), permitindo a exploração multidimensional de indicadores comerciais do 3º trimestre de 2026 por período, estado, município, categoria, canal de venda e campanha promocional.

### Camadas da Solução
* **Banco de Dados (PostgreSQL 12):** Tabela transacional `vendas_regionais` e visão analítica `vw_vendas_analitico` com métricas derivadas de preço e faturamento.
* **Camada Semântica e Queries (Metabase):** Combinação de perguntas visuais e consultas SQL parametrizadas com filtros de campo dinâmicos (`{{data_venda}}`, `{{estado}}`, `{{municipio}}`, `{{categoria}}`, `{{canal}}`).
* **Visualização e Interatividade:** 4 cartões de KPI, 4 gráficos analíticos e 1 tabela detalhada com suporte a **filtros globais**, **cross-filtering**, **drill-down / drill-up** e **drill-through**.

---

## Principais Resultados Analíticos (3º Trimestre 2026)

* **Desempenho Consolidado:** Receita realizada de **R$ 1,1 milhão** distribuída em **2.134 vendas**, com ticket médio de **R$ 493,46** nas transações concluídas e taxa global de cancelamento de **3,35%**.
* **Concentração Regional:** O **Piauí (PI)** lidera a geração de receita com **R$ 682,4 mil** (**62,0%** do faturamento total, 1.334 pedidos e ticket médio de **R$ 511,57**), seguido pelo **Ceará (CE)** e **Maranhão (MA)**.
* **Liderança por Categoria e Omnichannel:** **Eletrônicos** representa a principal vertical de receita (**R$ 482,4 mil**), com distribuição equilibrada entre **Loja física (26,94%)**, **Marketplace (25,59%)**, **Site (25,09%)** e **Aplicativo (22,38%)**.
* **Eficiência Promocional:** As campanhas **Volta às aulas** e **Promoção de agosto** concentram a maior parcela do volume faturado no trimestre.

---

## Recursos Interativos Implementados

1. **Visão Geral Executiva:** KPIs consolidados, ranking estadual, evolução semanal (receita vs. cancelamentos), desempenho por campanha e composição por categoria/canal.
2. **Filtros Globais Encadeados:** Filtragem simultânea em todos os 9 cartões do painel por Período, Estado, Município, Categoria e Canal.
3. **Cross-filtering (Filtragem Cruzada):** Seleção direta sobre barras de Estado, Categoria ou Canal atualiza dinamicamente o restante do dashboard.
4. **Drill-down / Drill-up:** Navegação hierárquica partindo do nível estadual até município, categoria e produto, com retorno imediato aos níveis superiores.
5. **Drill-through:** Consulta granular aos registros individuais na tabela analítica `vw_vendas_analitico`.

---

## Documentação Completa

O relatório acadêmico completo com as capturas de tela comentadas está disponível em [`relatorio_vendas_regionais_infovis.pdf`](relatorio_vendas_regionais_infovis.pdf).
