# ENTREGABLE_PRUEBA_DESEMPE-O_2026


Este proyecto es parte de la iniciativa de modernización de datos de EventFlow Systems.
El objetivo es transformar una estructura de datos plana basada en Excel en una base de datos relacional adecuadamente diseñada que permita un almacenamiento eficiente, consistencia y consultas analíticas.

Anteriormente, toda la información se almacenaba en hojas de cálculo donde la información se mezclaban en los mismos registros.
Esto causó varios problemas:

Duplicación de datos
Precios inconsistentes de las entradas
Informes y análisis difíciles
Falta de integridad de los datos

Para resolver estos problemas, se diseñó un esquema de base de datos relacional en MySQL siguiendo los principios de normalización.

Diseño de la base de datos
Enfoque de diseño

El conjunto de datos plano contiene las siguientes columnas:


TransactionID
TransactionDate
AttendeeName
AttendeeEmail
AttendeeCity
EventName
EventCategory
EventDate
VenueName
VenueCity
TicketType
TicketPrice
Quantity
OrganizerName
OrganizerEmail


Dado que esta estructura mezcla información de múltiples entidades del mundo real, el primer paso fue identificar las entidades centrales en el sistema.

Las principales entidades identificadas fueron:

Asistentes
Organizadores
Eventos
Lugares
Tipos de ticket
Transacciones
Detalles de la transacción

El esquema fue diseñado siguiendo la Tercera Forma Normal (3NF) para eliminar la redundancia y asegurar la integridad de los datos.

Modelo de relación de entidades

La estructura de la base de datos separa los datos en múltiples tablas relacionadas.
Relaciones principales:

Un evento puede tener múltiples tipos de ticket
Un participante puede realizar múltiples transacciones
Una transacción puede contener múltiples compras de boletos

Estructura conceptual:

Asistentes
Transacciones
TransactionDetails
TicketTypes
Eventos
Organizadores
Lugares

Esta estructura evita la duplicación y garantiza que cada entidad se almacene solo una vez.
