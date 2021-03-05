
# GUIA BÁSICO DE SQL <img src="https://raw.githubusercontent.com/gusantos1/icons/main/iconsql.png" width="40%">

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
  <p style="color:red">* Seleciona todas as colunas.</p>
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
  comentários sobre o código.
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
  WHERE condicao; : igual -> =  diferente -> <>
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

<table>
<p align="center"><img align="center"><h2>COUNT</h2></p>
<tr>
<!-- Tabela code sql -->
<td>

  ```sql
  SELECT count(coluna)
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
  comentários sobre o código.
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
  SELECT TOP quantidade colunaN
  FROM tabela;

  SELECT TOP quantidade *
  FROM tabela;
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




