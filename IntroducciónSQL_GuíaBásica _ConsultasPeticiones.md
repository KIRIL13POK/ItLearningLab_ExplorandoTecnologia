# Introducción a SQL: Guía Básica de Consultas y Peticiones

![imgSQLInicio](https://www.dataquest.io/wp-content/uploads/2021/12/why-sql-consumes-so-much-memory-header.webp)

***SQL (Structured Query Language)*** es un lenguaje de programación diseñado para administrar y manipular bases de datos relacionales. Se utiliza para realizar diversas operaciones en una base de datos, como la creación, modificación, eliminación y recuperación de datos.

***

### Creación de SQL:

**Año**: Década de 1970

**Creadores**: Donald D. Chamberlin y Raymond F. Boyce

**El Propósito**: Facilitar la interacción con bases de datos relacionales.

**El Objetivo Principal**: Permitir a los usuarios manipular y consultar datos eficientemente sin preocuparse por detalles técnicos.

### Desarrollo Inicial:

El primer sistema de gestión de bases de datos relacionales en utilizar SQL fue IBM System R en la década de 1970. Sin embargo, no fue hasta 1979 cuando Chamberlin y Boyce publicaron un artículo que presentaba la idea de SQL como un lenguaje de consulta relacional. Este artículo estableció los fundamentos conceptuales de SQL y definió gran parte de su sintaxis.

### Estandarización y Popularidad:

Con el tiempo, SQL fue adoptado por varias compañías y sistemas de gestión de bases de datos, lo que llevó a su estandarización. En 1986, el Instituto Nacional Estadounidense de Estándares (ANSI) adoptó SQL como estándar oficial. Más tarde, en 1987, la Organización Internacional de Normalización (ISO) también adoptó SQL como estándar internacional.

### Primeros Usos:
El primer sistema de gestión de bases de datos en implementar SQL comercialmente fue Oracle en 1979. Otros sistemas populares que adoptaron SQL incluyen IBM DB2 y Microsoft SQL Server. A medida que la tecnología de bases de datos relacionales se expandía, SQL se convirtió en el lenguaje dominante para gestionar datos en sistemas relacionales.

### Expansión y Evolución:
Con el tiempo, SQL evolucionó para abarcar más operaciones y capacidades, como transacciones, integridad de datos, funciones de agregación, vistas y procedimientos almacenados. Además, se introdujeron variantes específicas del sistema de gestión de bases de datos, lo que llevó a algunas diferencias en la sintaxis y las funciones admitidas.

Hoy en día, SQL sigue siendo la base fundamental para interactuar con bases de datos relacionales, y su uso se ha expandido a una variedad de aplicaciones, desde aplicaciones empresariales hasta aplicaciones web y análisis de datos. Su historia rica y su continua relevancia en el mundo tecnológico lo convierten en un lenguaje esencial para cualquier persona interesada en la gestión y manipulación de datos.

***

# Conceptos clave para empezar

* **Base de datos:** Una colección organizada de datos relacionados que se almacenan de manera estructurada. Puede contener tablas, vistas, procedimientos almacenados y más.

    ![BaseDeDatos](https://static.wikia.nocookie.net/sistemadeinformacionadministrativa/images/4/48/Las-mejores-bases-de-datos-de-email-de-espa%C3%B1a-1.jpg/revision/latest/scale-to-width-down/1000?cb=20181003224342&path-prefix=es)

* **Tabla:** Una estructura que almacena datos en filas y columnas. Cada fila representa un registro y cada columna representa un campo de datos específico.

* **Consulta SELECT:** Se utiliza para recuperar datos de una tabla. Puedes especificar las columnas que deseas recuperar y agregar condiciones para filtrar los resultados.
    ```SQL
    
    SELECT Nombre, Puesto FROM Empleados WHERE Salario > 50000;

    ```
    *Esta consulta seleccionará los nombres y puestos de trabajo de los empleados cuyos salarios sean mayores a 50000.*

    

* **Consulta INSERT:** Permite agregar nuevos registros a una tabla.
    ```SQL

    INSERT INTO Empleados (Nombre, Puesto, Salario) VALUES ( 'Ana', 'Analista', 60000);

    ```
    *Esta consulta insertará un nuevo registro en la tabla "Empleados" con el nombre "Ana", el puesto "Analista" y un salario de 60000.*

* **Consulta UPDATE:** Utilizada para modificar los datos existentes en una tabla.
    ```SQL

    UPDATE Empleados SET Salario = 55000 WHERE ID = 2 ;

    ```
    *Esta consulta actualizará el salario del empleado con ID 2 y lo cambiará a 55000.*

* **Consulta DELETE:** Sirve para eliminar registros de una tabla.
  ```SQL

    DELETE FROM Empleados WHERE ID = 3;

  ```
  *Esta consulta eliminará el registro del empleado con ID 3 de la tabla "Empleados".*

* **CLAUSULA WHERE:** Se utiliza en las consultas para filtrar los resultados según una condición especificada.
    ```SQL

    SELECT Nombre, Puesto FROM Empleados WHERE Puesto = 'Desarrollador';

    ```
    *Esta consulta seleccionará los nombres y puestos de trabajo de los empleados que tienen el puesto "Desarrollador".*

* **CLAUSULA ORDER BY:** Utilizada para ordenar los resultados de una consulta en función de una o más columnas.
    ```SQL

    SELECT Nombre, Salario FROM Empleados ORDER  BY Salario DESC;

    ```
    *Esta consulta seleccionará los nombres y salarios de los empleados, ordenados de manera descendente según el salario.*
* **CLAUSULA GROUP BY:** Permite agrupar filas que tengan el mismo valor en una o varias columnas, a menudo utilizada con funciones de agregación como SUM, COUNT, AVG, etc.
    ```SQL

    SELECT Puesto, AVG(Salario) FROM Empleados  GROUP BY Puesto;

    ```
    *Esta consulta calculará el promedio de salario para cada puesto de trabajo y mostrará los resultados agrupados por puesto.*

* **JOIN:** Utilizado para combinar datos de dos o más tablas en función de una relación definida entre ellas.

    ```SQL

    SELECT  Empleados, Nombre, Departamentos.Nombre
    FROM Empleados
    JOIN Departamentos ON Empleados.DepartamentoID = DepartamentosID

    ```
    *Esta consulta combinará la información de las tablas "Empleados" y "Departamentos" utilizando la columna "DepartamentoID", mostrando los nombres de los empleados junto con los nombres de sus respectivos departamentos.*
* **Índices:** Estructuras que mejoran la velocidad de búsqueda y recuperación de datos en una base de datos al crear referencias rápidas a las filas.

    *Los índices no se expresan con una consulta directa, pero son estructuras que mejoran la velocidad de búsqueda en una tabla, como se muestra en el ejemplo de creación de un índice para la columna "Nombre".*

* **Transacciones:** Secuencias de operaciones que se ejecutan como una unidad indivisible. Pueden ser confirmadas (commit) o deshechas (rollback).

    ```SQL

    START TRANSACTION;
    UPDATE CuentaBancaria SET Saldo = Saldo - 100 WHERE ID = 1 ;
    UPDATE CuentaBancaria SET Saldo = Saldo + 100 WHERE ID = 2 ;
    COMMIT;

    ```
    *Estas consultas forman una transacción en la que se resta 100 de la cuenta con ID 1 y se suma 100 a la cuenta con ID 2, asegurando que ambas operaciones se realicen como una unidad indivisible.*

* **Vistas:** Consultas predefinidas que actúan como tablas virtuales, lo que permite ver los datos de formas específicas sin alterar los datos reales.

    ```SQL

    CREATE VIEW EmpleadosConSalarioMayor AS
    SELECT Nombre, Puesto, FROM Empleados WHERE Salario > 55000;
    ```
    *Esta consulta crea una vista llamada "EmpleadosConSalarioMayor" que contendrá los nombres y puestos de empleados cuyos salarios sean mayores a 55000.*

* **Procedimientos almacenados:** Conjunto de instrucciones SQL que se almacenan en la base de datos y se pueden invocar con un nombre para realizar operaciones específicas.
    ```SQL

    CREATE PROCEDURE ActualizarSalario(IN empleadoID INT, IN nuevo salario DECIMAL)
    BEGIN
        UPDATE Empleados SET Salario = nuevoSalario WHERE ID = empleadoID;
    END;
    ```

    *Este ejemplo crea un procedimiento almacenado llamado "ActualizarSalario" que acepta un ID de empleado y un nuevo salario como parámetros, y luego actualiza el salario del empleado correspondiente en la tabla "Empleados".*
