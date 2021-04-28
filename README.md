
# <img src="https://raw.githubusercontent.com/gusantos1/icons/main/iconsql.png" width="15%">  GUIA BÁSICO DE SQL PARA PROGRAMADORES

---
Esse repositório contém comandos básicos de SQL para você manipular um banco de dados de forma objetiva.</br>Os comentários contidos em cada função podem trazer analogias com linguagens de programação para melhor entendimento.

---

<div align="center">
<table>
<p align="center"><img align="center"><h2>SELECT</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
    SELECT coluna1, coluna2, colunaN
    FROM tabela

    SELECT *
    FROM tabela;
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li>Comando básico para selecionar o conteúdo de N colunas. O conteúdo das linhas é o retorno da função.</li>
  <p style="color:#FF0000"><strong>(*)</strong> Seleciona todas as colunas.</p>
</p>
</td>
</tr>
</table>


<table>
<p align="center"><img align="center"><h2>DISTINCT</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT DISTINCT coluna1, coluna2, colunaN
  FROM tabela;
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li>Desconsidera dados duplicados dentro de uma tabela.</li>
  <li>Vale lembrar da função <strong>Set</strong> em Python que elimina a repetição de dados num iterável.</li>
</p>
</td>
</tr>
</table>

<table>
<p align="center"><img align="center"><h2>WHERE</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT coluna1, coluna2, colunaN
  FROM tabela
  WHERE condicao;

  SELECT Nome, idade
  FROM pessoas.alunos
  WHERE idade > 18;
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li>É a forma de se montar uma estrutura condicional no SQL.</li>
  <li>Os operadores lógicos são os mesmos da maioria das linguagens de programação, com a ressalva de:</li>
  <ol>
  <li>igual: <strong>=</strong></li>
  <li>diferente: <strong><></strong></li>
  </ol>
  <li>Na função ao lado -> Retorna o nome e idade de alunos maiores de 18 anos.</li>
</p>
</td>
</tr>
</table>


<table>
<p align="center"><img align="center"><h2>COUNT</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT count(colunaN)
  FROM tabela;

  SELECT count(DISTINCT coluna)
  FROM tabela;

  SELECT count(*)
  FROM tabela;
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li>É um contador que funciona como a função len/length de outras linguagens de programação.</li>
  <li>Na primeira função -> Retorna o número total de linhas dentro da colunaN.</li>
  <li>Na segunda função -> Retorna o número total de linhas dentro da coluna desconsiderando dados duplicados.</li>
  <li>Na terceira função -> retorna a quantidade total de todas as linhas (somatório de linhas de todas as colunas).</li>
</p>
</td>
</tr>
</table>


<table>
<p align="center"><img align="center"><h2>TOP</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT TOP 12 colunaN
  FROM tabela;

  SELECT TOP 10 *
  FROM tabela;
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li>Define a quantidade de retorno de linhas.</li>
  <li>Na primeira função -> Retorna 12 linhas da colunaN.</li>
  <li>Na segunda função -> Retorna 10 linhas de todas (*) as colunas.</li>
</p>
</td>
</tr>
</table>


<table>
<p align="center"><img align="center"><h2>ORDER BY</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT colunaN
  FROM tabela
  ORDER BY colunaM asc/desc;

  SELECT TOP 10 Nome, Preco
  FROM produtos.disponiveis
  ORDER BY Preco desc;
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li>Essa função ordena os resultados obtidos de uma coluna.</li>
  <li>Em algumas linguagens é similar as funções <strong>sorted()</strong> e <strong>reverse()</strong>, pois ordena de forma crescente e decrescente tanto pra números e alfabeto.</li>
  <li>A função ao lado -> Retorna o nome e o preço dos 10 primeiros produtos mais caros.</li>
</p>
</td>
</tr>
</table>


<table>
<p align="center"><img align="center"><h2>BETWEEN</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT id_mercadoria, preco
  FROM produtos.preco
  WHERE preco BETWEEN 200 and 880;
  
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li> É basicamente uma condição lógica atrelada ao WHERE para comparação de mínimo e máximo.</li>
  <li> Equivale a fazer valor <strong> >= </strong> condicao and valor <strong> <= </strong> condicao.</li>
  <li> A função ao lado -> Retorna o id e o preço de todas as mercadorias entre 200 e 880, inclusive.</li>
</p>
</td>
</tr>
</table>


<table>
<p align="center"><img align="center"><h2>IN</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT *
  FROM pessoas.dados
  WHERE nascimento in (1992, 2000, 2011);
  
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li> O IN traz o sentido de "Contém" tais elementos.</br>Em uma estrutura condição como no python, usamos o in para verificar se um valor está contido em algo. Nesse caso podemos pensar o inverso. </li>
  <li> Uma estrutura condicional usando WHERE e uma série de OR também trará o mesmo retorno para condição.</li>

  <li> A função ao lado -> Retorna todos os dados de pessoas nascidas nos anos de 1992, 2000 e 2011.</li>
</p>
</td>
</tr>
</table>


<table>
<p align="center"><img align="center"><h2>LIKE</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT *
  FROM pessoas.dados
  WHERE Sobrenome LIKE 'SA%';
  
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li> O LIKE funciona para encontrar um dado em determina coluna mesmo não obtendo os caracteres completos. A idéia é similar ao método <strong>find()</strong> contido no python. </li>
  <li> A função ao lado -> Retorna todos os dados de pessoas que contém 'San' no sobrenome, podendo ser: Santos, Santiago,Sampaio, etc.</li>
</p>
</td>
</tr>
</table>


<table>
<p align="center"><img align="center"><h2>MIN MAX SUM AVG</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT MIN (vunitario) FROM produtos.precos;
  SELECT MAX (vunitario) FROM produtos.precos;
  SELECT SUM (vunitario) FROM produtos.precos;
  SELECT AVG (vunitario) FROM produtos.precos;
  
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li> As funções desse tópico são comuns em bibliotecas Math entre várias linguagens de progração: Mínimo, Máximo, Somatório e Média.</li>
  <li> As funções ao lado -> Retornam o mínimo, o máximo, o somatório e a média de todos os valores na coluina de 'Valores Unitários'.</li>
</p>
</td>
</tr>
</table>


<table>
<p align="center"><img align="center"><h2>GROUP BY</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT Naturalidade, COUNT(nome)
  FROM pessoas.dados
  GROUP BY Naturalidade;
  
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li> O GROUP BY possui uma finalidade interessante, é comum o uso desse método com uma função de agregação(count, sum) para visualização de dados por grupo. </li>
  <li> A função ao lado -> Agrupa por Naturalidade e atribui o número total de pessoas por região.</li>
</p>
</td>
</tr>
</table>


<table>
<p align="center"><img align="center"><h2>HAVING</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT Peixes, sum(Pfinal) as 'Total'
  FROM Mercadorias.peixes
  GROUP BY Peixes
  HAVING sum(Pfinal) BETWEEN 200 and 400;
  
  
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li> O HAVING é uma condicional para ser aplicada após o GROUP BY. </li>
  <li> Ele funciona como um filtro <strong>APÓS</strong> o group by</li>
  <li> A função ao lado -> Cria um grupo(tabela) com o nome dos Peixes e outra com o Total que é o somatório do preço final de cada; e retorna aqueles em que o valor Pfinal estiver entre 200 e 400, inclusive.</li>
</p>
</td>
</tr>
</table>


<table>
<p align="center"><img align="center"><h2>INNER JOIN</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT p.BusinessEntityID,p.FirstName, p.LastName, pe.EmailAddress
  FROM person.Person as p
  INNER JOIN Person.EmailAddress as pe on p.BusinessEntityID = pe.BusinessEntityID;  
  
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li> O INNER JOIN é uma forma de concatenção de dados entre as tabelas.</li>
  <li> É possível concatenar informações a apartir de uma coluna que esteja presente nas duas tabelas. </li>
  <li> É importante o uso da AS para diferenciar os atributos.</li>
</p>
</td>
</tr>
</table>


<table>
<p align="center"><img align="center"><h2>TIPOS DE JOIN</h2></p>
<tr>

<td>
<div style="text-align:center">
  <img src="https://github.com/gusantos1/guiasqlbasico/blob/main/inner.png" width="100%">
  <img src="https://github.com/gusantos1/guiasqlbasico/blob/main/left.png" width="100%">
  <img src="https://github.com/gusantos1/guiasqlbasico/blob/main/fullouter.png" width="100%">
  <img src="https://github.com/gusantos1/guiasqlbasico/blob/main/sqldiagrams.png" width="100%">
</div>
</td>
</tr>
</table>


<table>
<p align="center"><img align="center"><h2>UNION</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT Mercadoria, Valor
  FROM tabela.lojaA
  UNION
  SELECT Mercadoria, Valor
  FROM  tabela2.lojaB
  
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li> O UNION é uma forma de unir dados de tipos iguais.</li>
  <li> Não se trata de concatenção, e sim de por na mesma coluna dados de tipos iguais. </li>
  <li> A função ao lado -> Cria uma coluna Mercadoria, com todos os nomes das duas tabelas e Valor, com todos os valores das duas tabelas.</li>
</p>
</td>
</tr>
</table>


<table>
<p align="center"><img align="center"><h2>DATEPART</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT MercadoriaID,DATEPART(month, validadeDoProduto) as validade
  FROM tabela.lojaA
  
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  <li>O DATEPART é uma função para manipulação de dados do tipo data.</li>
  <li>Vamos compará-la com o uso do <strong>datetime</strong> presente no python.</li>
  <li>A função ao lado -> Retornará duas colunas: O id da mercadoria e o mês de validade.</li>
</p>
</td>
</tr>
</table>



<table>
<p align="center"><img align="center"><h2>MANIPULAÇÃO DE STRINGS</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT CONCAT(FirstName, ``, LastName)
  FROM Person.Person
  
  SELECT UPPER(FirstName), LOWER(LastName)
  FROM Person.Person

  SELECT LEN(FirstName)
  FROM Person.Person

  SELECT SUBSTRING(FirstName, 1, 3) -- FATIAMENTO
  FROM Person.Person

  SELECT REPLACE(FirstName, 'Clark', 'Ralph')
  FROM Person.Person
  ```
</td>
<!-- Tabela comentário-->
<td>

</td>
</tr>
</table>







</div>




