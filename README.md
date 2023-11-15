# novo_hospital
Criamos um novo banco de dados de um hospital

para esse novo banco de dados usamos os seguintes comandos:

CREATE DATABASE hospital_banco;

drop database hospital_banco;

use hospital;

create table medicos ( 
id_medicos int primary key,
nome_medico varchar (100),
especialidade varchar (100)
);

select * from medicos;


INSERT INTO medicos (id_medicos, nome_medico, especialidade)
VALUES
(1,'Dr. João Silva', 'Clinica Geral'),

(2,'Dra. Maria Santos', 'Pediatria'),

(3,'Dr. Carlos Oliveira', 'Gastroenterologia'),

(4,'Dra. Ana Pereira', 'Dermatologia'),

(5,'Dr. Pedro Rocha', 'Cardiologia'),

(6,'Dra. Laura Mendes', 'Gastrenterologia '),

(7,'Dr. Rafael Almeida', 'Pediatria'),

(8,'Dra. Beatriz Nunes', 'Clinica Geral'),

(9,'Dr. Bruno Costa', 'Clinica Geral'),

(10,'Dra. Camila Rodrigues', 'Clinica Geral'),

(11,'Dra. Roberta Magalhaes', 'Pediatria'),

(12,'Dra. Bruna Alves', 'Pediatria'),

(13,'Dra. Gbriela Porttinari', 'Clinica Geral'),

(14,'Dr. Josefino de Oliveira', 'Gastrenterologia'),

(15,'Dr. Claudio Gomes', 'Gastrenterologia');

create table pacientes (
id_paciente int primary key,
nome_paciente varchar(100),
data_de_nascimento date,
convenio varchar(100)
);

create table consultas (
id_consulta int primary key,
id_medico int,
nome_paciente varchar(100),
convenio varchar(100),
data_da_consulta date,
medicamento int
);


create table internacoes (
id_internacao int primary key,
nome_paciente varchar(100),
data_de_internacao date,
data_de_alta date,
previsao_de_alta date,
quarto varchar (100),
enfermeiro varchar (100)
);

create table quartos (
id_quarto int primary key,
tipo_de_quarto varchar(100)
);

create table enfermeiros (
id_enfermeiro int primary key, 
nome_enfermeiro varchar(100)
);


INSERT INTO pacientes (id_paciente, nome_paciente, data_de_nascimento, convenio)
VALUES
(1, 'José Silva', '1990-05-15', 'Convênio A'),

(2, 'Maria Oliveira', '1985-08-22', 'Convênio B'),

(3, 'Ana Santos', '2000-02-10', 'Convênio C'),

(4, 'Carlos Pereira', '1975-11-30', 'Convênio A'),

(5, 'Patrícia Rocha', '1995-04-18', 'Convênio B'),

(6, 'Felipe Almeida', '1980-07-25', 'Convênio C'),

(7, 'Laura Costa', '1998-09-12', 'Convênio A'),

(8, 'Rafael Nunes', '1992-12-05', 'Convênio B'),

(9, 'Camila Mendes', '1987-03-08', 'Convênio C'),

(10, 'Bruno Rodrigues', '1978-06-20', 'Convênio A'),

(11, 'Gilmar Toledo', '1970-12-29', 'Convênio A'),

(12, 'Thiago Alvez', '1978-03-25', 'Convênio A'),

(13, 'Cezar Menoti', '1988-06-08', 'Convênio A'),

(14, 'Fabio Menoti', '1988-06-08', 'Convênio A'),

(15, 'Emerson Madruga', '1999-09-19', 'Convênio A');


INSERT INTO consultas (id_consulta, id_medico, nome_paciente, convenio, data_da_consulta, medicamento)
VALUES
(1, 1, 'José Silva', 'Convênio A', '2015-03-10', 1),

(2, 15, 'Maria Oliveira', 'Convênio B', '2016-06-22', 20),

(3, 10, 'Ana Santos', 'Convênio C', '2017-01-15', 3),

(4, 7, 'Carlos Pereira', 'Convênio A', '2018-04-05', 14),

(5, 5, 'Patrícia Rocha', 'Convênio B', '2019-09-28', 55),

(6, 6, 'Felipe Almeida', 'Convênio C', '2020-12-10', 67),

(7, 12, 'Laura Costa', 'Convênio A', '2021-05-18', 37),

(8, 7, 'Rafael Nunes', 'Convênio B', '2022-01-02', 18),

(9, 9, 'Camila Mendes', 'Convênio C', '2016-07-14', 9),

(10, 10, 'Bruno Rodrigues', 'Convênio A', '2017-11-30', 11),

(11, 15, 'Bruno Rodrigues', 'Convênio A', '2017-12-10', 11),

(12, 2, 'Thiago Alvez', 'Convênio A', '2021-09-30', 10),

(13, 8, 'Cezar Menoti', 'Convênio A', '2020-01-20', 10),

(14, 11, 'Patrícia Rocha', 'Convênio B', '2021-04-06', 10),

(15, 14, 'Bruno Rodrigues', 'Convênio A', '2019-11-30', 17),

(16, 3, 'Laura Costa', 'Convênio A', '2016-12-31', 9),

(17, 5, 'Emerson Madruga', 'Convênio A', '2019-07-13', 18),

(18, 4, 'Emerson Madruga', 'Convênio A', '2019-07-23', 20),

(19, 13, 'Emerson Madruga', 'Convênio A', '2019-08-03', 13),

(20, 14, 'Gilmar Toledo', 'Convênio A', '2018-09-30', 10);

INSERT INTO internacoes (id_internacao, nome_paciente, data_de_internacao, data_de_alta, previsao_de_alta, quarto, enfermeiro)
VALUES
(1, 'José Silva', '2015-06-10', '2015-06-15', '2015-06-14', 'Apartamento', 'Eliane Martins'),

(2, 'Maria Oliveira', '2016-08-25', '2016-09-01', '2016-08-28', 'Quarto Duplo', 'Giusep Lamborguini'),

(3, 'Ana Santos', '2017-03-18', '2017-03-25', '2017-03-22', 'Enfermaria', 'Douglas Ferreira'),

(4, 'Carlos Pereira', '2018-06-05', '2018-06-12', '2018-06-10', 'Apartamento', 'Gisely Alvez'),

(5, 'Patrícia Rocha', '2019-10-22', '2019-11-01', '2019-10-28', 'Quarto Duplo', 'Mercedes da Silva'),

(6, 'Felipe Almeida', '2020-01-15', '2020-01-25', '2020-01-22', 'Enfermaria', 'Beatriz Cunha'),

(7, 'Laura Costa', '2021-07-08', '2021-07-18', '2021-07-15', 'Apartamento', 'Melissa Maia'),

(8, 'Fabio Menoti', '2020-01-08', '2020-01-20', '2020-01-20', 'Quarto Duplo', 'Willians Smith'),

(9, 'Emerson Madruga', '2019-07-18', '2019-07-30', '2019-07-27', 'Apartamento', 'Monalisa Albertina');


INSERT INTO quartos (id_quarto, tipo_de_quarto)
VALUES
(1, 'Apartamento'),

(2, 'Quarto Duplo'),

(3, 'Enfermaria');

INSERT INTO enfermeiros (id_enfermeiro, nome_enfermeiro)
VALUES
(1, 'Eliane Martins'),

(2, 'Gisely Alvez'),

(3, 'Maria Clara'),

(4, 'Jhonatan Souza'),

(5, 'Stefany Lais'),

(6, 'Melissa Maia'),

(7, 'Beatriz Cunha'),

(8, 'Gabriel Ferrari'),

(9, 'Douglas Ferreira'),

(10, 'Giusep Lamborguini'),

(11, 'Mercedes da Silva'),

(12, 'Monalisa Albertina'),

(13, 'Willians Smith');

select * from internacoes;

select * from enfermeiros;

select * from consultas;

select * from pacientes;

select * from quartos;

INSERT INTO internacoes (id_internacao, nome_paciente, data_de_internacao, data_de_alta, previsao_de_alta, quarto, enfermeiro)
VALUES
(10, 'José Silva', '2019-06-10', '2019-06-15', '2019-06-14', 'Apartamento', 'Eliane Martins'),

(11, 'Emerson Madruga', '2018-05-11', '2018-05-15', '2019-05-14', 'Apartamento', 'Willians Smith');


