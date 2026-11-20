# Análisis de Fuga Financiera y Cancelaciones Hoteleras (SQL / Databricks)

Proyecto en **Databricks (Spark SQL)** para el holding **DataAndino**, enfocado en auditar datos, cuantificar pérdidas por cancelaciones y perfilar reservas para renegociar contratos con agencias.

## Problema de Negocio
* **Comisiones:** Pago de **USD 1.5** por reserva captada vía agencias (TA/TO), incluso si se cancela.
* **Costo operativo:** Pérdida de **USD 120** por cancelaciones con menos de 3 días de anticipación.

## Stack y Técnicas SQL
* **Entorno:** Databricks (Spark SQL)
* **Limpieza y DML:** `CREATE TABLE`, `INSERT INTO ... SELECT`, `UPDATE` con subconsultas y `DELETE`.
* **Consultas:** `INNER JOIN`, `LEFT JOIN`, `FULL OUTER JOIN`, agregaciones y `CASE WHEN`.

## Hallazgos Clave
* **Agencias (TA/TO):** Concentran la mayoría de reservas y cancelaciones sin penalidad.
* **Compromiso:** Huéspedes con hijos, solicitudes especiales o cambios en su reserva cancelan menos.
* **Propiedades:** Mayor costo de cancelación en Resort; cancelaciones tardías impiden reventa.
* **Acción:** Renegociar comisiones por reserva efectiva e implementar depósitos previos.
