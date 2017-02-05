# Overview and challenges of Adopting Microservices

La implementación de una arquitectura de microservicios promete un sin número de ventajas entre las que se puede listar: facilita el uso de diferentes tecnologías orientadas al subdominio; mejora el desacoplamiento, lo que facilita el cambio de una implementación por otra; facilita el deployment de funcionalidades independientes, introduce el empoderamiento, independencia y especialización de equipos \(squads\) a un determinado subdominio; mejora la sincronización entre la estructura organizacional y el diseño del bounded context \(Conway Law\); entre otras ventajas. Como consecuencia el time-to-market disminuye por la facilidad de desarrollar microservicios en versiones de experimientación \(Minimum Viable Product\).

Por otro lado, la arquitectura de microservicios puede llegar a ser un dolor de cabeza a nivel técnico por los desafíos que plantea. A continuación se presenta algunos de los problemas que como líder técnico he enfrentado y superado:

* Lograr consistencia en microservicios distribuidos
* Establecer una comunicación desacoplada entre microservicios
* 
Consistency

Fault Tolerance

No hay conocimiento de DOmain Drive design

Tenia que tener soporte real time

Comunicacion entre microservicios

Si no habia una comunicacion desacoplada era simplemente otro monolitico

Aggregates Distribuidos

Orden en el Event sourcing

Como deployar tantos microservicios

Codigo legacy

Costos de tener muchos servidores

No existian pruebas

Rechazo al cambio

Monitoreo de los microservicios

Como manejar versiones

Como manejar squads en los microservicios, ley conway

Inexperiencia

No sql approach y el rechazo al cambio de una sola base de datos para todo el sistema, hagamoslo directo a la base, no hay disciplina en cuanto a hacerlo todo mediante rest

Eventual consistency, asyn o sync

Message Driven



