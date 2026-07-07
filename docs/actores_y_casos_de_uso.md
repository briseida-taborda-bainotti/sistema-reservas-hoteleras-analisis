# Actores y Casos de Uso

> Diagrama de casos de uso: [`../diagramas/casos_de_uso_v2.png`](../diagramas/casos_de_uso_v2.png)

## Actores del sistema

| Actor | Descripción |
|---|---|
| **Encargado de recepción** | Gestiona las reservas presenciales, realiza check-in y check-out, consulta la agenda, registra cancelaciones, actualiza precios y registra al cliente. |
| **Administrador de sistemas** | Gestión técnica y mantenimiento del sistema: usuarios, seguridad, precios, cabañas, agenda, proveedores y mantenimiento. |
| **Encargado de compras** | Registra y gestiona las compras de insumos necesarios para el complejo. |
| **Encargado de mantenimiento** | Consulta y registra los mantenimientos realizados y pendientes en las instalaciones. |
| **Usuario** | Actor genérico que accede al sistema de forma segura (iniciar/cerrar sesión, modificar contraseña). |
| **Encargado web** | Administra y registra reservas, y gestiona cancelaciones provenientes de distintos medios (web, teléfono, Booking o presencial). |
| **Gestor mail** | Servicio que envía automáticamente correos de confirmación de reservas y notificaciones. |
| **Entidad bancaria** | Actor externo que autoriza los pagos con tarjeta de crédito/débito. |

## Catálogo de casos de uso

### Casos de uso de soporte

| Caso de uso | Descripción | Rol |
|---|---|---|
| Iniciar sesión | Permite ingresar al sistema de forma segura mediante autenticación de credenciales. | Usuario |
| Cerrar sesión | Finaliza la sesión activa de forma segura, protegiendo la información confidencial. | Usuario |
| Modificar contraseña | Permite cambiar la contraseña de forma segura y sencilla. | Usuario |
| Registrar mantenimiento | Carga, actualización y control de tareas de mantenimiento. | Administrador de sistemas |
| Registrar proveedores | Mantiene un registro actualizado de proveedores. | Administrador de sistemas |
| Registrar precios | Gestiona y actualiza tarifas según temporada, promociones o convenios. | Administrador de sistemas |
| Registrar cabaña | Registra y administra la información de cada cabaña. | Administrador de sistemas |
| Registrar agenda | Organiza y mantiene actualizada la agenda de reservas. | Administrador de sistemas |
| Registrar métodos de pago | Registra y administra los métodos de pago aceptados. | Administrador de sistemas |

### Casos de uso de negocio

| Caso de uso | Descripción | Rol |
|---|---|---|
| Registrar cliente | Alta de un nuevo cliente con sus datos personales; permite actualizarlos. | Encargado de recepción / Encargado web |
| Registrar reserva | Registra una nueva reserva verificando agenda, datos del pasajero, cabaña, cantidad de personas y método de pago. | Encargado web |
| Registrar cancelación de reserva | Anula una reserva existente y actualiza la disponibilidad de cabañas. | Encargado web |
| Consultar reserva | Verifica los detalles de una reserva registrada. | Encargado web / Encargado de recepción |
| Consultar pago | Verifica que el pago de una reserva esté realizado. | Encargado web |
| Consultar cliente | Busca y visualiza información de un cliente ya registrado. | Encargado de recepción |
| Registrar ingreso (check-in) | Registra la llegada del cliente, validando la reserva e identidad. | Encargado de recepción |
| Registrar finalización de estancia (check-out) | Registra la salida del cliente, libera la cabaña y actualiza el estado de la reserva. | Encargado de recepción |
| Consultar mantenimiento | Visualiza las tareas de mantenimiento en curso o pendientes. | Encargado de mantenimiento |
| Registrar nuevo mantenimiento | Registra una nueva tarea de mantenimiento. | Encargado de mantenimiento |
| Registrar mantenimiento finalizado | Marca una tarea de mantenimiento como terminada. | Encargado de mantenimiento |
| Registrar compra de insumos | Registra la compra de insumos a proveedores. | Encargado de compras |
| Consultar compras | Visualiza compras pendientes o el historial. | Encargado de compras |
