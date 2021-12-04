# Alkemy-Exercises-SQL

### Tema 1 (Manipulación)

1.
`CREATE TABLE CURSO (
  codigo INT NOT NULL PRIMARY KEY,
  nombre VARCHAR(45) NOT NULL,
  descripcion VARCHAR(45),
  turno VARCHAR(45) NOT NULL
);`

2.
`ALTER TABLE CURSO ADD cupo INT;`

3.
`INSERT INTO CURSO (codigo, nombre, descripcion, turno, cupo)
VALUES 
(101,"Algoritmos","Algoritmos y Estructuras de Datos","Mañana",35),
(102,"Matemática Discreta","","Tarde",30);`

`SELECT * from CURSO;`

4.
`INSERT INTO CURSO (codigo, nombre, descripcion, turno, cupo)
VALUES (103,null,"curso vacío","Mañana",32);`

![Nombre nulo](https://user-images.githubusercontent.com/77683363/144724136-f76bd906-ab90-436f-98c7-f1f0439eab9b.png)

5.
`INSERT INTO CURSO (codigo, nombre, descripcion, turno, cupo)
VALUES (101,"Repetido","curso repetido","Mañana",25);`

![id repetida](https://user-images.githubusercontent.com/77683363/144724142-deb9ceaf-854e-4c0b-8676-7916399675af.png)

6.
`UPDATE CURSO SET cupo = 25;`

7.
`DELETE FROM CURSO WHERE codigo = 101;`

### Tema 2 (Tipos de Join)


