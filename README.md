-- Criação da tabela com estrutura adequada --
CREATE TABLE Pupil (
    id_int INT NOT NULL AUTO_INCREMENT,
    nome VARCHAR(50) NOT NULL,
    matricula INT NOT NULL UNIQUE,
    email VARCHAR(35) NOT NULL,
    endereco VARCHAR(50),
    telefone VARCHAR(15),
    PRIMARY KEY (id_int)
);

-- Inserção de dados (sem especificar o id, pois é auto-increment) --
INSERT INTO Pupil (nome, matricula, email, endereco, telefone) VALUES
('João Carlos', 1234, 'Jcarlos@gmail.com', 'Rua 13 de maio', '(11)7825-4489'),
('José Vitor', 2345, 'Jvitor@gmail.com', 'Rua da Saudade', '(11)7825-6589'),
('Paulo André', 3456, 'Pandr@gmail.com', 'Rua do Sol', '(11)7825-4495');

-- Inserção de mais registros --
INSERT INTO Pupil (nome, matricula, email, endereco, telefone) VALUES
('Ana Paula', 4567, 'Anapaula@gmail.com', 'Avenida Central', '(11)7826-1234'),
('Carlos Eduardo', 5678, 'Ceduardo@gmail.com', 'Travessa das Flores', '(11)7826-5678');

-- Consulta de todos os registros --
SELECT * FROM Pupil;

-- Atualizar o telefone de um aluno específico (exemplo: João Carlos) --
UPDATE Pupil
SET telefone = '(11)9999-9999'
WHERE nome = 'João Carlos';

-- Excluir um registro (exemplo: aluno com matrícula 2345) --
DELETE FROM Pupil
WHERE matricula = 2345;

-- Consultar registros após atualização e exclusão --
SELECT * FROM Pupil;

-- Criar um índice para facilitar buscas por nome --
CREATE INDEX idx_nome ON Pupil(nome);

-- Buscar alunos cujo nome contém 'Paulo' --
SELECT * FROM Pupil
WHERE nome LIKE '%Paulo%';

-- Buscar aluno com matrícula específica --
SELECT * FROM Pupil
WHERE matricula = 4567;

-- Inserir um novo aluno usando uma instrução preparada (exemplo de uso de variáveis) --
-- (Caso esteja usando uma ferramenta que suporte variáveis) --
-- SET @nome = 'Maria Clara'; --
-- SET @matricula = 6789; --
-- SET @email = 'MariaClara@gmail.com'; --
-- INSERT INTO Pupil (nome, matricula, email, endereco, telefone) VALUES (@nome, @matricula, @email, 'Rua das Palmeiras', '(11)7826-9876'); --

-- Visualizar estrutura da tabela --
DESCRIBE Pupil;
