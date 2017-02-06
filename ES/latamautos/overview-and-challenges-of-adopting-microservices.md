# Overview and challenges of Adopting Microservices

La implementación de una arquitectura de microservicios promete un sin número de ventajas entre las que se pueden listar: facilita el uso de diferentes tecnologías orientadas al dominio \(o subdominio\); mejora el desacoplamiento, lo que facilita el cambio de una implementación por otra; facilita el deployment de funcionalidades independientes, introduce el empoderamiento, independencia y especialización de equipos \(squads\) a un determinado subdominio; mejora la sincronización entre la estructura organizacional y el diseño del bounded context \(Conway Law\); entre otras ventajas. Como consecuencia el time-to-market disminuye por la facilidad de desarrollar microservicios en versiones de experimientación \(Minimum Viable Product\).

Por otro lado, la arquitectura de microservicios puede llegar a ser un dolor de cabeza a nivel técnico por los desafíos que plantea. A continuación se presentan algunas de las dudas y problemas que como líder técnico he enfrentado sobre este tema: 

* ¿Cómo manejar la consistencia en microservicios distribuidos?
* ¿Cuál es la mejor forma de comunicación entre microservicios?
* ¿Cómo reponerse a un fallo en el canal de comunicación entre microservicios?
* ¿Cómo garantizar el orden de eventos en la comunicación distribuida?
* ¿Cómo garantizar que la dependencia entre microservicios no se rompa en continuous delivery?
* ¿Implementar un framework base que facilite la implementación de microservicios?, etc

Además de los retos técnicos, existen desafíos de habilidades blandas como:

* Evangelización en el uso de Domain Driven Design
* Convencer al equipo del uso de la pirámide de pruebas
* Demostrar y sensibilizar al equipo de las ventajas de los microservicios frente al gasto en tiempo de la mitigación de las desventajas
* Inexperiencia en el campo



