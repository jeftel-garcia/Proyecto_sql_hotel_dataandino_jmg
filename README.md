# Análisis de Fuga Financiera y Cancelaciones Hoteleras (SQL / Databricks)

Proyecto en **Databricks (Spark SQL)** para el holding **DataAndino**, enfocado en auditar la calidad de datos, cuantificar pérdidas por cancelaciones y perfilar el comportamiento de reserva para renegociar contratos con agencias.

## Problema de Negocio
* **Comisiones sin penalidad:** Pago de **USD 1.5** por reserva captada por agencias intermediarias (TA/TO), incluso si se cancela[cite: 9].
* **Costo operativo hundido:** Pérdida de **USD 120** por cancelaciones realizadas con menos de 3 días de anticipación[cite: 9].

## Stack y Técnicas SQL
* **Entorno:** Databricks (Spark SQL)
* **Limpieza y DML:** `CREATE TABLE`, `INSERT INTO ... SELECT`, `UPDATE` con subconsultas y `DELETE` para depurar errores de captura y estandarizar registros.
* **Modelado y Consultas:** `INNER JOIN`, `LEFT JOIN`, `FULL OUTER JOIN`, agregaciones y `CASE WHEN` para auditar comprobantes, detectar reservas sin ejecutivo asignado y evaluar riesgo por ventana de anticipación.

## Hallazgos Clave
* **Fuga en agencias (TA/TO):** Concentran la mayoría de reservas y cancelaciones sin penalidad por anulación.
* **Indicadores de compromiso:** Huéspedes con hijos, solicitudes especiales o cambios en su reserva cancelan considerablemente menos.
* **Riesgo por propiedad:** El costo promedio de cancelación es mayor en hoteles tipo Resort frente a los de ciudad; las cancelaciones tardías impiden la reventa del inventario.
* **Recomendación:** Renegociar contratos bajo esquemas de reserva efectiva e implementar depósitos previos.
