# SQL_SAMPLES

Um Exemplo de queries em SQL que fiz recentemente

Em resumo, o código executa uma consulta otimizada que combina informações sobre vendedores, produtos vendidos, valores faturados e comissões. Ele fornece um resultado final que mostra os melhores vendedores, os produtos mais vendidos e outras métricas relevantes, tudo isso em conformidade com os critérios de filtragem e ordenação especificados.

Etapa 1: Subconsulta TAB1

-> Essa etapa seleciona informações dos vendedores, incluindo o ano, o nome, a quantidade vendida, o valor faturado, a comissão e outros dados relevantes.
-> Utiliza funções de agregação (SUM, FORMAT) e operações de janela (OVER PARTITION BY) para calcular os valores agregados e formatá-los adequadamente.
-> A subconsulta TAB1 é usada como uma fonte de dados na consulta principal.

Etapa 2: Subconsulta TAB2

-> Nesta etapa, são selecionados os produtos mais vendidos para cada vendedor em cada ano, juntamente com informações como o nome do produto, a quantidade vendida e o ranking.
-> Utiliza funções de janela (RANK, OVER PARTITION BY) para classificar os produtos com base na quantidade vendida.
-> A subconsulta TAB2 é usada como uma fonte de dados na consulta principal.

Etapa 3: Consulta principal

-> Combina os resultados das subconsultas TAB1 e TAB2 usando uma junção interna (INNER JOIN) com base na chave.
-> Seleciona as colunas específicas a serem exibidas no resultado final da consulta.
-> Aplica filtros e ordena os resultados, limitando o ranking dos produtos mais vendidos até o terceiro lugar.
-> Os valores são formatados e apresentados de maneira adequada, usando funções como FORMAT e CONVERT.



Diagrama

![image](https://user-images.githubusercontent.com/69773007/208420601-62bdd62e-69a2-45e9-a899-f9b61eb424ee.png)

Neste banco de dados do curso Alura, conforme o diagrama acima, efetuei uma pesquisa que retorna a seguinte tabela abaixo:
Tabela resultado:

![image](https://user-images.githubusercontent.com/69773007/208420710-05a21790-7888-4d1f-a0f0-e06b17b33c41.png)

Nesta tabela resultado onde pode ser consultado no repositório desse projeto a consulta original, tive que utilizar subqueries, agregações gerais e também com Over e Partition By a fim de gerar os resultados bem como encerrar a consulta com um Rank personalizável onde é possível alterar facilmente a quantidade de resultados  desejada.

NO primeiro exemplo primeiro criei duas views e posteriormente fiz o relacionamento entre elas:

![image](https://user-images.githubusercontent.com/69773007/208421391-40bd3642-e2e2-4bc0-85e8-907179b0a101.png)

Chamando as Views:
![image](https://user-images.githubusercontent.com/69773007/208421458-b77df198-92f9-4294-b34b-e2c078e7d4d3.png)

Nesse segundo exemplo, fiz a mesma tabela final, porém sem a criação de views intermediárias, apenas usando subqueries e também relacionando elas por meio de joins:

![image](https://user-images.githubusercontent.com/69773007/208421626-7ab604b6-99d9-411d-a160-f7d554c5bcce.png)

 O código SQL fornecido possui três etapas principais e tem como função geral realizar uma consulta otimizada em um banco de dados. Aqui está um resumo das etapas e da função geral do código:
 

