https://clck.ru/FBXYD

SHOW databases;

CREATE DATABASE test;
DROP DATABASE test;

USE test;

CREATE TABLE people
(
    id INT AUTO_INCREMENT,
    name VARCHAR(30),
    email VARCHAR(30),
    PRIMARY KEY (id)
);

DESC people;

INSERT INTO people VALUES (1, 'Andrey', 'and.rey.q@ya.ru');

SELECT * FROM people;

SELECT * FROM people 
WHERE name LIKE '%y';

UPDATE people SET
email = 'TEST@TEST.RU'
WHERE name = 'Andrey';

ALTER TABLE people
ADD COLUMN id INT AUTO_INCREMENT FIRST,
ADD PRIMARY KEY (id);

ALTER TABLE people
ADD COLUMN age VARCHAR(30) AFTER email;

???
CREATE TABLE sport
(
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(30) NOT NULL,
    user_id INT,
    FOREIGN KEY (user_id) REFERENCES people (id)
);