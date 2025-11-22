
# SQL_Basic
SQL Study to Data science Students.




![GitHub repo size](https://img.shields.io/github/repo-size/iuricode/README-template?style=for-the-badge)
![GitHub language count](https://img.shields.io/github/languages/count/iuricode/README-template?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/iuricode/README-template?style=for-the-badge)
![Bitbucket open issues](https://img.shields.io/bitbucket/issues/iuricode/README-template?style=for-the-badge)
![Bitbucket open pull requests](https://img.shields.io/bitbucket/pr-raw/iuricode/README-template?style=for-the-badge)

---

### Introduction to SQL Basic Concepts for Data Science 
Fundamental concepts essential for anyone who wants to work with data analysis.

---


🔹 sqlliteonline.com
---
🔹 Using Select to filter a information
---

```
Select * from TABELA;
SELECT * FROM tabelafornecedores WHERE país_de_origem = 'China'
Valores únicos
SELECT DISTINCT cliente from tabelapedidos;

If you don't know the exactly name you also can search with

Select * from tabelafornecedores where pais_de_origem like 'china%';


SELECT * FROM Clientes WHERE Idade > 30 AND Sexo <> 'Masculino';

SELECT * FROM tabelaprodutos WHERE preco_de_compra BETWEEN 200 AND 600 ORDER BY nome_do_produto;

SELECT * FROM livros WHERE (genero LIKE '%ficção científica%' OR genero LIKE '%fantasia%') AND ano_publicacao > 2000 AND editora IS NULL ORDER BY ano_publicacao DESC LIMIT 20;
```

---
🔹Creating Table
---
```
CREATE TABLE tabelaclientes (
  ID_Cliente INT PRIMARY KEY,
  Nome_Cliente VARCHAR (250),
  Informacoes_de_Contato VARCHAR (250)
);

```
🔹 Altering a Table
---
```
ALTER TABLE tabelaclientes ADD Endereço_Cliente VARCHAR (250);
ALTER TABLE nome_da_tabela DROP COLUMN coluna_antiga;


UPDATE tabelaclientes SET informacoes_de_contato = 'j.santos@email.com', 
endereço_cliente = 'Rua dos paralelepipedos, 30 '
WHERE id_cliente = 2;

UPDATE tabelapedidos SET status = 'Enviado' WHERE status = 'Processando';


DELETE FROM tabelafornecedores WHERE pais_de_origem = 'Turquia';


```
🔹 Foreign key is connected to the primary key of another table
---
```
CREATE TABLE tabelaprodutos (
  ID_Produto INT PRIMARY KEY,
  Nome_do_Produto VARCHAR (250),
  Descrição TEXT,
  Categoria INT,
  Preco_de_Compra DECIMAL (10,2),
  Unidade VARCHAR (50),
  Fornecedor INT,
  Data_de_Inclusao DATE,
  FOREIGN KEY (Categoria) REFERENCES tabelacategorias (id_categoria),
  FOREIGN KEY (Fornecedor) REFERENCES tabelafornecedores (id)
);
```


🔹 Insert new Information
---
```
INSERT INTO LivrosClássicos (id_livro, titulo_livro, autor, ano_publicacao)
VALUES ('1', 'Moby Dick', 'Herman Melville', '1851'),
('2', 'João Santos', 'joao.santos@provedor.com', 'Rua dos pinheiros, 25');
```

### Adjustments and improvements.

The project is still under development, and the upcoming updates will focus on the following tasks:

- [x] Advanced courses about SQL

The following tools were used in the construction of the project:

- [Python](<https://www.python.org/doc//>)
- [Google colab](<https://colab.google/>)



## 🤝 Creator

<table>
  <tr>
    <td align="center">
      <a href="#" title="Thales Farias">
        <img src="grecia.jpg" width="100" alt="Foto do Thales Farias no GitHub"/><br>
        <sub>
          <b><a href="https://www.linkedin.com/in/thalesfreirefarias/" target="_blank">Thales Farias</b>
        </sub>
      </a>
    </td>
  </tr>
</table>

