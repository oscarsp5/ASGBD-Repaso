<h1>💻 Estructuras</h1>

<h2>⌨ Cursores/Procedimientos Almacenados</h2>

<p>Es una porcion de codigo que puedes guardar y reutilizar, se usa cuando repites la misma tarea repetidas veces, siendo un buen metodo para encapsular codigo</p>

<h4>Estrucutura:</h4>

```sql
delimiter //
CREATE PROCEDURE nombreprocedimiento (in varEntrada tipo,out varSalida tipo)
begin
	select * from tabla;
end //
delimiter;
```

<h4>Ejemplo:</h4>

## Eventos

```sql
DROP EVENT IF EXISTS ofertas_31_dic$$
CREATE EVENT ofertas_31_dic ON SCHEDULE
EVERY 1 YEAR
STARTS "2021-12-31 05:00:00" -- current_timestamp() + INTERVAL 1 minute
ENDS current_timestamp() + INTERVAL 1 minute|year|month
DO
BEGIN
    -- Contenido
END
```

## Triggers
```sql
CREATE TRIGGER nombre_trigger {BEFORE|AFTER} {INSERT|UPDATE|DELETE}
ON nombre_tabla
FOR EACH ROW
BEGIN
END$$
```
