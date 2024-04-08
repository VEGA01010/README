# README
EXERCICIO INNER, JOIN E ALIASES
CREATE TABLE Cidades (
    id INTEGER PRIMARY KEY,
    nome VARCHAR(60) NOT NULL,
    populacao INTEGER
);

CREATE TABLE Alunos (
    id INTEGER PRIMARY KEY,
    nome VARCHAR(60) NOT NULL,
    data_nasc TEXT,
    cidade_id INTEGER,
    FOREIGN KEY (cidade_id) REFERENCES Cidades(id)
);

INSERT INTO Cidades VALUES (1, 'Arraial dos Tucanos', 42632);
INSERT INTO Cidades VALUES (2, 'Springfield', 13820);
INSERT INTO Cidades VALUES (3, 'Hill Valley', 27383);
INSERT INTO Cidades VALUES (4, 'Coruscant', 19138);
INSERT INTO Cidades VALUES (5, 'Minas Tirith', 31394);

INSERT INTO Alunos VALUES (1, 'Immanuel Kant', '2010-04-22', 4);
INSERT INTO Alunos VALUES (2, 'Alan Turing', '1912-06-23', 3);
INSERT INTO Alunos VALUES (3, 'George Boole', '2002-01-01', 1);
INSERT INTO Alunos VALUES (4, 'Lynn Margulis', '1991-08-12', 3);
INSERT INTO Alunos VALUES (5, 'Nicola Tesla', '2090-01-08', null);
INSERT INTO Alunos VALUES (6, 'Ada Lovelace', '1978-05-28', 4);
INSERT INTO Alunos VALUES (7, 'Claude Shannon', '1982-10-15', 3);
INSERT INTO Alunos VALUES (8, 'Charles Darwin', '2010-02-06', null);
INSERT INTO Alunos VALUES (9, 'Marie Curie', '2007-07-12', 3);
INSERT INTO Alunos VALUES (10, 'Carl Sagan', '2000-11-20', 1);
INSERT INTO Alunos VALUES (11, 'Tim Berners-Lee', '1973-12-05', 4);
INSERT INTO Alunos VALUES (12, 'Richard Feynman', '1982-09-12', 1);

SELECT *
FROM Alunos
INNER JOIN Cidades
ON Cidades.id = Alunos.cidade_id;
