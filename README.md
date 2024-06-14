# SQL--Proyecto consultas operaciones de financiación
Este es un proyecto realizado durante el Máster de Data Science, Big Data & Business Analytics, en el que una empresa financiera que concede préstamos en diferentes establecimientos para la adquisición de productos solicita el análisis de las operaciones realizadas durante el ejercicio 2015.Esta empresa financia las compras de los clientes de los comercios con los que trabaja teniendo estos que devolverlos durante un periodo posterior a la compra.

Los datos están distribuidos en 3 tablas:
+ merchants: recoge los establecimientos con los que trabaja la empresa financiera
+ orders: recoge las operaciones realizadas y cada una tiene un status en función del estado de la operacion, que puede ser: ACTIVE (Significa que el préstamo aún está en plazo para ser pagado), CLOSED (significa que el cliente pagó el préstamo), DELINQUENT (Significa que el cliente no pagó el préstamo y el plazo para pagar se
ha pasado) y CANCELLED (Significa que al final el préstamo no se realizó).
+ refunds: recoge las operaciones de cancelación del pedido por parte del cliente y devolución del importe al establecimiento (no todos los merchants aceptan reembolsos).

Este proyecto se basa en realizar las siguientes consultas:

1- Realizar una consulta donde se obtenga por país y estado de operación, el
total de operaciones y su importe promedio. La consulta debe cumplir las
siguientes condiciones:

  a. Operaciones posteriores al 01-07-2015
  b. Operaciones realizadas en Francia, Portugal y España.
  c. Operaciones con un valor mayor de 100 € y menor de 1500€
  
Ordenamos los resultados por el promedio del importe de manera descendente.

2- Realizar una consulta donde se obtengan los 3 países con el mayor número de
operaciones, el total de operaciones, la operación con un valor máximo y la
operación con el valor mínimo para cada país. La consulta debe cumplir las
siguientes condiciones:
  a. Excluimos aquellas operaciones con el estado “Delinquent” y “Cancelled”
  b. Operaciones con un valor mayor de 100 €

3- Realizar una consulta donde se obtenga, por país y comercio, el total
de operaciones, su valor promedio y el total de devoluciones. La consulta
debe cumplir las siguientes condiciones:
  a. Se debe mostrar el nombre y el id del comercio.
  b. Comercios con más de 10 ventas.
  c. Comercios de Marruecos, Italia, España y Portugal.
  d. Creamos un campo que identifique si el comercio acepta o no devoluciones.
  
Si no acepta (total de devoluciones es igual a cero) el campo debe contener el
valor “No” y si sí lo acepta (total de devoluciones es mayor que cero) el campo
debe contener el valor “Sí”. Llamaremos al campo “acepta_devoluciones”.
Ordenar los resultados por el total de operaciones de manera ascendente.
4- Realizar una consulta donde se va a traer todos los campos de las tablas operaciones y comercios. De la tabla devoluciones se va a traer el conteo de devoluciones por operación y la suma del valor de las devoluciones. Una vez se tenga la consulta anterior, se crea una vista con el nombre orders_view dentro del esquema prestamos_2015 con esta consulta.


