# Especificación del Caso de Uso: Registrar Reserva

Se documenta este caso de uso en dos niveles de detalle: **trazo fino** (paso a paso, formato esencial) y **trazo grueso** (resumen ejecutivo).

## Trazo fino

| Campo | Detalle |
|---|---|
| **ID** | 1 |
| **Nombre** | Registrar reserva |
| **Actor principal** | Encargado de reservas (ER) |
| **Actor secundario** | Gestor de mail, entidad bancaria |
| **Tipo** | Concreto |
| **Objetivo** | Registrar una nueva reserva en el sistema, previamente verificando la agenda, y registrando datos del pasajero, fechas de estadía, cabaña asignada, cantidad de personas y método de pago. |
| **Precondición** | Usuario logueado y sesión activa. |

### Curso normal

1. El sistema solicita seleccionar fecha de ingreso, fecha de egreso y cantidad de personas.
2. El ER selecciona las fechas de ingreso/egreso y la cantidad de personas.
3. El sistema verifica la disponibilidad según la cantidad y fechas seleccionadas.
4. El sistema busca y muestra las cabañas disponibles con su precio correspondiente.
5. El sistema solicita seleccionar una cabaña.
6. El ER selecciona una cabaña.
7. El sistema solicita los datos del pasajero (nombre, apellido, documento, tipo de documento, teléfono, dirección, mail, fecha de nacimiento).
8. El ER ingresa los datos del pasajero.
9. El sistema solicita el método de pago.
10. El ER selecciona el método de pago.
11. El sistema solicita los datos de la tarjeta (número, CVV, vencimiento, documento y nombre del titular).
12. El ER ingresa los datos de la tarjeta.
13. El sistema solicita confirmación.
14. El ER confirma.
15. El sistema verifica los datos de la tarjeta con éxito.
16. El sistema registra el pago.
17. El sistema emite el comprobante de pago.
18. El sistema registra la reserva.
19. El sistema genera el comprobante con número de reserva asociado.
20. El sistema envía la confirmación de reserva vía mail.
21. Fin del caso de uso.

### Cursos alternativos

**A1 (Paso 3):** El sistema no encuentra cabaña disponible en la fecha seleccionada.
- El sistema solicita ingresar una nueva fecha.
- El ER selecciona una nueva fecha.

**A2 (Paso 15):** El sistema rechaza el pago con tarjeta.
- El sistema solicita los datos de una nueva tarjeta.
- El ER ingresa los datos de la nueva tarjeta.
- El sistema verifica los nuevos datos con éxito.

### Postcondiciones

- **Éxito:** se generó y registró una nueva reserva de alojamiento con su comprobante.
- **Fracaso:** el sistema no encuentra cabañas disponibles.

### El CU se cancela cuando

- El encargado de reservas decide cancelar el caso de uso en cualquier momento previo a confirmar el registro de la reserva.

**Observaciones:** ER = Encargado de Reservas

---

## Trazo grueso

| Campo | Detalle |
|---|---|
| **Nombre del caso de uso** | Registrar reserva |
| **Actores** | Encargado de reservas, Gestor mail, Entidad bancaria |
| **Objetivo** | Registrar una nueva reserva en el sistema previamente verificando la agenda, registrando datos del pasajero, fechas de estadía, cabaña asignada, cantidad de personas y método de pago. |
| **Precondición** | Usuario logueado y sesión activa. |
| **Postcondición** | Éxito: se generó y registró una nueva reserva de alojamiento con su comprobante. Fracaso: el sistema no encuentra cabañas disponibles. |
