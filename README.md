# Análisis de Fuga Financiera y Cancelaciones Hoteleras (SQL / Databricks)

Proyecto desarrollado en **Databricks (Spark SQL)** para el holding **DataAndino**, enfocado en cuantificar pérdidas por cancelaciones de reservas y respaldar la renegociación de contratos con agencias de marketing[cite: 13].

## Problema de Negocio
* **Comisiones sin penalidad:** Pago de **USD 1.5** por reserva generada vía agencia, incluso si se cancela[cite: 13].
* **Costo operativo hundido:** Pérdida de **USD 120** por cada cancelación con menos de 3 días de anticipación[cite: 13].

## Stack y Técnicas SQL
* **Entorno:** Databricks (Spark SQL)
* **Limpieza y DML:** `CREATE TABLE`, `INSERT INTO ... SELECT` y `UPDATE` con subconsultas para depurar errores de captura[cite: 3, 7, 10].
* **Consultas y Modelado:** `INNER JOIN`, `LEFT JOIN` y segmentación condicional con `CASE WHEN` para auditar clientes y cuantificar el impacto financiero[cite: 1, 2, 4, 5, 13].

## Resultado
Estandarización de la base de reservas y cuantificación exacta de la fuga económica por canal para la toma de decisiones comerciales[cite: 13].
