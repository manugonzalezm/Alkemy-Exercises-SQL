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

### Tema 3 (Queries)

Creación de la tabla y sus campos:

`CREATE TABLE PROFESOR (
  id INT NOT NULL PRIMARY KEY,
  nombre VARCHAR(45) NOT NULL,
  apellido VARCHAR(45) NOT NULL,
  fecha_nacimiento DATE NOT NULL,
  salario INT NOT NULL
);

INSERT INTO PROFESOR VALUES
(1,"Juan","Pérez",'1990-06-06',55000),
(2,"María Emilia","Paz",'1984-07-15',72000),
(3,"Martín","Correa",'1987-12-07',63000),
(4,"Lucía","Díaz",'1991-02-24',45000),
(5,"Raúl","Martínez",'1980-10-15',85000),
(6,"Mabel","Ríos",'1982-06-12',83000);`

1.
`SELECT nombre, apellido, fecha_nacimiento FROM PROFESOR ORDER BY fecha_nacimiento ASC;`

2.
`SELECT * FROM PROFESOR WHERE SALARIO >= 65000;`

3.
`SELECT * FROM PROFESOR WHERE (fecha_nacimiento) BETWEEN ('1980-01-01') AND ('1989-12-31') order by fecha_nacimiento;`

4.
`SELECT * FROM PROFESOR LIMIT 5;`

5.
`SELECT * FROM PROFESOR WHERE apellido LIKE "P%";`

6.
`SELECT * FROM PROFESOR WHERE ((fecha_nacimiento) BETWEEN ('1980-01-01') AND ('1989-12-31')) AND salario > 80000;`
