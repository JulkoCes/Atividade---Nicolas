# Atividade---Nicolas
Códigos SQL

Aqui abaixo apresento os Códigos das duas atividades solicitadas:

ATIVIDADE 1

CREATE DATABASE principal;
USE principal

CREATE TABLE vendas(
id_vendas BIGINT NOT NULL PRIMARY KEY,
nome_cliente Varchar(30),
id_produto Varchar(30),
valor BIGINT,
quantia INT
);

INSERT INTO vendas (id_vendas, nome_cliente, id_produto, valor, quantia)
VALUES
(1, 'Carlos Felino', 'Bebidas', 2, 17.00),
(2, 'Davi Britto', 'Calabresa', 5, 58.00),
(3, 'Jon Bovi', 'Guitarra', 1, 6500.00),
(4, 'Oruam', 'trend', 1, 1000.00),
(5, 'Tom', 'sofa', 3, 3230.00);

UPDATE vendas
SET id_produto = 'Lentilha'
WHERE id_vendas = 3;

DELETE FROM vendas WHERE id_vendas = 4;

SET SQL_Safe_UPDATES = 0;

-------------

Atividade 2

CREATE DATABASE escolinha;
USE escolinha;

CREATE TABLE cursos (
  id_curso INT PRIMARY KEY,
  nome_curso VARCHAR(100) NOT NULL,
  duracao_meses INT NOT NULL,
  valor_mensal DECIMAL(10,2) NOT NULL
  ) AUTO_INCREMENT = 1;

CREATE TABLE alunos (
  id_aluno INT PRIMARY KEY,
  nome VARCHAR(100) NOT NULL,
  data_nascimento DATE NOT NULL,
  cpf VARCHAR(14) UNIQUE
);

INSERT INTO cursos (id_curso, nome_curso, duracao_meses, valor_mensal)
VALUES
(1, 'Educacao Infantil', 2, 300.00),
(2, 'Ensino Fundamental II', 9, 450.00),
(3, 'Ensino Medio', 3, 500.00),
(4, 'Ensino Superior', 4, 800.00);

INSERT INTO alunos (nome, data_nascimento, cpf)
VALUES
('João Silva', '2015-03-10', '123.456.789-00'),
('Maria Santos', '2016-07-22', '987.654.321-00'),
('Carlos Oliveira', '2014-01-15', '456.789.123-00');

CREATE USER 'professor'@'localhost' IDENTIFIED BY 'prof123';
CREATE USER 'secretaria'@'localhost' IDENTIFIED BY 'sec456';
CREATE USER 'administrador'@'localhost' IDENTIFIED BY 'admin789';
