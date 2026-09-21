# Dashboard E-commerce - Análise de Performance
<img width="1328" height="743" alt="image" src="https://github.com/user-attachments/assets/67c1a849-c32b-43b6-87e0-5d153e865f44" />






---
### **Sobre o projeto**
Este projeto foi desenvolvido como forma de fixar aprendizados práticos em análise de dados e criação de dashboards no [Power BI](https://app.powerbi.com/home), a partir da aula da professora [Leticia Smirelli](http://www.youtube.com/watch?v=XRA5vd8_mhQ). 
O painel consiste em uma análise completa das vendas de uma loja online (e-commerce), permitindo visualizar de forma interativa os principais indicadores de performance (KPIs) e o comportamento das vendas ao longo do tempo.

---
### Ferramentas utilizadas
- **Microsoft Power BI Desktop**: Utilizado para a modelagem, criação das medidas e construção da interface visual do dashboard.
- **Power Query**: Utilizado para o processo de ETL (Extração, Tratamento e Carregamento dos dados), garantindo a limpeza e estruturação correta da base.
- **Microsoft Excel**: Utilizado como a fonte de dados primária, contendo as planilhas de histórico de vendas e o cadastro detalhado dos produtos.

---
### Processos e Técnicas Aplicadas 
- **ETL (Extração, Tratamento e Carregamento)**: Os dados brutos foram importados e tratados no Power Query. O processo incluiu a remoção de linhas nulas/em branco, promoção da primeira linha a cabeçalho, exclusão de colunas irrelevantes, categorização dos tipos de dados (como número decimal fixo para valores monetários) e extração do número e nome abreviado dos meses para análises temporais.
- **Modelagem de Dados**: Na criação de um relacionamento entre as tabelas, foi estabelecida uma cardinalidade de "1 para muitos" (1:N) relacionando a tabela dimensão de cadastro de produtos (valores únicos) com a tabela fato de histórico de vendas (valores repetidos) utilizando a chave em comum "código do produto".

 ---
 ### Indicadores Chave de Performance (KPIs)
 O painel superior apresenta cartões que destacam as métricas gerais do negócio:
- Faturamento Total: R$ 4.57 Milhões.
- Produtos: 15 produtos únicos no catálogo.
- Quantidade de Itens Vendidos: 30 Mil itens.
- Total de Clientes: 5447 clientes distintos.
- Total de Pedidos: 9932 pedidos realizados.

---
### Visualizações e Análises
- **Faturamento ao longo do tempo** (Gráfico de Área): Demonstra a evolução do faturamento mês a mês com uma linha suavizada, permitindo identificar a sazonalidade e picos de vendas.
- **Valor Total por categoria de produto** (Gráfico de Barras): Funciona como um ranking dos produtos mais vendidos, classificados por suas respectivas categorias (Calçados, Acessórios e Bolsas). Identifica, por exemplo, a "Sandália Linus Violeta" como o principal produto.
- **Representatividade de vendas por canal** (Gráfico de Rosca): Analisa a proporção do faturamento vindo de diferentes plataformas. Os dados indicam que o Website domina com 84.63% das vendas, enquanto o Mobile App representa 15.37%.
- **Matriz de Detalhamento**: Uma tabela expansível que lista o desempenho por categoria e nome do produto, cruzando os dados de quantidade vendida e valor total. Utiliza formatação condicional de barras de dados nativa do Power BI para evidenciar os maiores volumes rapidamente.

---
### Filtros e Interatividade   
- **Período de Análise**: Filtro de datas em formato de controle deslizante, permitindo a análise de uma janela de tempo específica (como 01/01/2020 a 30/12/2020).
- **Segmentação de Dados Avançada**: Filtros em lista suspensa (dropdown) para Cod. Produto e Categoria, contando com uma função de barra de pesquisa ativada para localizar itens rapidamente num catálogo extenso.
- **Filtros Cruzados**: O dashboard é 100% interativo, então ao clicar em qualquer barra, fatia de gráfico ou item da matriz, todos os outros visuais e KPIs se adaptam automaticamente para refletir o dado selecionado.
