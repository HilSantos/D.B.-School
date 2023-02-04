# D.B.-School

CREATE TABLE Pupil (
PRIMARY KEY (ID_INT),
id_int not null auto_increment,
nome VARCHAR(50) not null,
e-mail VARCHAR(35) not null,
endereco VARCHAR(50) null
);

SELECT * FROM Pupil,
insert into Pupil (id, nome, matricula, email, endereco, telefone) values
(01, 'João Carlos', 1234, 'Jcarlos@gmail.com', 'Rua 13 de maio', '(11)7825-4489');

insert into Pupil (id, nome, matricula, email, endereco, telefone) values
(02, 'José Vitor', 2345, 'Jvitor@gmail.com', 'Rua da Saudade', '(11)7825-6589');

insert into Pupil (id, nome, matricula, email, endereco, telefone) values
(03, 'Paulo André', 3456, 'Pandr@gmail.com', 'Rua do Sol', '(11)7825-4495');
