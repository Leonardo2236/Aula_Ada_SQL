# Aula_Ada_SQL
Primeira aula prática pela ADA Tech de SQL, utilizando o SGBD PostgreSQL

---Criação de tabela

CREATE TABLE aulaa_ada.estudos.filmes (

filme_id SERIAL NOT NULL,
titulo VARCHAR(40),
genero1 VARCHAR(40),
genero2 VARCHAR(40),
genero3 VARCHAR(40)	

)
--- Consulta da tabela
SELECT * FROM estudos.filmes

--- Inserindo dados na tabela
INSERT INTO estudos.filmes(
titulo,
genero1,
genero2,
genero3)
VALUES
('Matrix', 'Ficcao Cientifica', 'Ação', 'Aventura'),
('Gladiador', 'Ação', 'Aventura', 'Drama'),
('Suspiria', 'Terror', 'Sobrenatural', 'Ação'),
('Senhor dos anéis', 'Aventura', 'Fantasia', 'Ação')	

----Alterar algum dado da tabela
UPDATE estudos.filmes
SET genero3 = 'Drama'
WHERE filme_id = 4

----Deletar a tabela
DROP TABLE estudos.filmes

---Correção Exercício 1
CREATE TABLE estudos.funcionarios(
	
funcionario_id SERIAL PRIMARY KEY,
nome VARCHAR (40),
departamento VARCHAR (30),
cargo VARCHAR (30),
senioridade VARCHAR (30),
salario NUMERIC (16,2)
)

---Exercicio 2
CREATE TABLE estudos.vendas(
pedido_id SERIAL PRIMARY KEY,
produto_id INTEGER NOT NULL,
nome_poduto VARCHAR (40),
quantidade INTEGER,
valor_unidade NUMERIC (16,2)	
)

SELECT * FROM estudos.funcionarios

--INSERIR DADOS TABELA FUNCIONARIO
INSERT INTO estudos.funcionarios VALUES
(1,'João Paulo','RH','Analista','Junior',2000),
(2,'Lúcia','RH','Analista','Pleno',3000),
(3,'Rosana','RH','Analista','Senior',4000),
(4,'Elisabete','RH','Coordenador','Liderança',5000),
(5,'Amanda','RH','Gerente','Gerência',7000),
(6,'Rafael','Analytics','Analista','Junior',3000),
(7,'Pedro','Analytics','Analista','Pleno',5000),
(8,'Lucas','Analytics','Analista','Pleno',5000),
(9,'Luiz Antônio','Analytics','Analista','Senior',7000),
(10,'Giovanni','Analytics','Analista','Senior',7000),
(11,'Nadia','Analytics','Coordenador','Liderança',9000),
(12,'Carmen','Analytics','Gerente','Gerência',11000),
(13,'Maurício','Dados','Analista','Pleno',5000),
(14,'Bruno Silva','Dados','Analista','Senior',8000),
(15,'Andressa','Dados','Cientista','Junior',5000),
(16,'José de Sousa','Dados','Cientista','Junior',6500),
(17,'Helena','Dados','Cientista','Pleno',7000),
(18,'Bruna','Dados','Cientista','Pleno',7000),
(19,'Bruno Pereira','Dados','Cientista','Pleno',8000),
(20,'Bianca','Dados','Cientista','Senior',11000),
(21,'Murilo','Dados','Coordenador','Liderança',12000),
(22,'Gisele','Dados','Coordenador','Liderança',14000),
(23,'Paulo','Dados','Gerente','Gerência',18000),
(24,'Wesley','Dados','Engenheiro','Junior',6000),
(25,'Vagner','Dados','Engenheiro','Pleno',9000),
(26,'Léticia','Dados','Engenheiro','Pleno',9000),
(27,'Sandro','Dados','Engenheiro','Senior',11000),
(28,'Enzo','Dados','Engenheiro','Senior',12000),
(29,'Lavinia','Dados','Engenheiro','Senior',12000),
(30,'Andrei','Dev','Engenheiro de Software','Junior',4000),
(31,'George','Dev','Engenheiro de Software','Junior',4000),
(32,'Caio','Dev','Engenheiro de Software','Pleno',5000),
(33,'Edna','Dev','Engenheiro de Software','Pleno',5000),
(34,'Debora','Dev','Engenheiro de Software','Pleno',6500),
(35,'Luiza','Dev','Engenheiro de Software','Pleno',6000),
(36,'Pedro Henrique','Dev','Engenheiro de Software','Pleno',6000),
(37,'Willian','Dev','Engenheiro de Software','Senior',7000),
(38,'Viviane','Dev','Engenheiro de Software','Senior',9000),
(39,'Mnnuel','Dev','Coordenador','Liderança',8000),
(40,'Lurdes','Dev','Coordenador','Liderança',9500),
(41,'Hygor','Dev','Gerente','Gerência',10000),
(42,'Ana Paula','Financeiro','Analista','Junior',2000),
(43,'Luciana','Financeiro','Analista','Junior',2000),
(44,'Lorena','Financeiro','Analista','Junior',2500),
(45,'Sara','Financeiro','Analista','Junior',2500),
(46,'Cintia','Financeiro','Analista','Pleno',3000),
(47,'Karina','Financeiro','Analista','Pleno',3000),
(48,'Camila','Financeiro','Analista','Senior',3500),
(49,'Afonso','Financeiro','Coordenador','Liderança',4500),
(50,'Cibele','Financeiro','Gerente','Gerência',5000);

--LIMITAR 10 LINHAS
SELECT * FROM estudos.funcionarios
ORDER BY funcionario_id DESC
LIMIT 8
