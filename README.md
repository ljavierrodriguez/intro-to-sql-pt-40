# INTRO TO SQL

## DML (Data Manipulation Language)

- SELECT (buscar o consultar)
- INSERT (ingresar o guardar)
- UPDATE (actualizar)
- DELETE (borrar o eliminar)

### SELECT

```sql 
-- Sintaxis:
-- SELECT * FROM nombre_de_la_tabla;

SELECT * FROM users;

SELECT id, username, password from users;

SELECT * FROM invoices WHERE date_invoice <= '2020-03-11 23:59:59'

```

### INSERT 

```sql
-- Sintaxis:
-- INSERT INTO nombre_table (field1, field2, ... fieldn) 
-- VALUES (value1, value2, ... valuen)

INSERT INTO users (username, password) VALUES ('lrodriguez', '123456');

```

### UPDATE

```sql

-- Sintaxis:
-- UPDATE nombre_table SET field1=value, field2=value2 WHERE condicion

UPDATE users SET username='lrodriguez@4geeks.co' WHERE id=1 or username='lrodriguez';

```

### DELETE

```sql
-- Sintaxis:
-- DELETE FROM nombre_tabla WHERE condicion

DELETE FROM users WHERE id = 1;
DELETE FROM users WHERE registered_date <= '2021-10-30'

```


### UNIONES

```sql

SELECT * FROM users AS a
JOIN profiles as b ON b.user_id = a.id

SELECT * FROM users AS a
JOIN posts as b ON b.user_id = a.id


SELECT * FROM users AS a
LEFT JOIN posts as b ON b.user_id = a.id