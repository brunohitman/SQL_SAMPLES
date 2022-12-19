# SQL_SAMPLES
some sample SQL queries that I'm currently developing



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

