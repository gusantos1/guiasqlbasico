
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
  Comando básico para selecionar o conteúdo de N colunas. O conteúdo das linhas é o retorno da função. </br>
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
  Desconsidera dados duplicados dentro de uma tabela.</br>
  Vale lembrar da função <strong>Set</strong> em Python que elimina a repetição de dados num iterável.
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
  FROM tabela
  WHERE idade > 18;
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  É a forma de se montar uma estrutura condicional no SQL.</br>
  Os operadores lógicos são os mesmos da maioria das linguagens, com a ressalva de:</br>
  igual: <strong>=</strong></br>
  diferente: <strong><></strong>
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
  É um contador que funciona como a função len/length de outras linguagens.</br>
  Na primeira função -> Retorna o número total de linhas dentro da colunaN.</br>
  Na segunda função -> Retorna o número total de linhas dentro da coluna desconsiderando dados duplicados.</br>
  Na terceira função -> retorna a quantidade total de todas as linhas (somatório de linhas de todas as colunas).
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
  Define a quantidade de retorno de linhas.
  Na primeira função -> Retorna 12 linhas da colunaN.
  Na segunda função -> Retorna 10 linhas de todas (*) as colunas.
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
  ORDER BY colunaM asc/desc
  ```
</td>
<!-- Tabela comentário-->
<td>
<p>
  comentários sobre o código.
</p>
</td>
</tr>
</table>

</div>




