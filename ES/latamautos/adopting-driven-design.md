#                  Adopting Domain Driven Design Philosophy

## Responsibilities

* **Evangelize the team on DDD concepts:** El equipo de desarrollo fué instruído en todos los conceptos presentes en Domain Driven Design:
  * `Bounded context`
  * `Context map`
  * `Aggregate`
  * `Entity`
  * `Value Object`
  * `Repository`
  * `Application Service`
  * `Domain Service`
  * `Factory`
  * `Domain Event`, etc.
* **Design and supervise DDD guidelines:** A continuación algunos de los puntos tomados en cuenta:
  * Estructura de carpetas definidas \(basadas en DDD\) a seguir
  * Nombres estandarizados para cada tipo de elemento DDD, etc 
* **Design and abstract bounded contexts and context maps:** Dado un subdominio o subdominios, abstraer los bounded context asociados y context maps que incluye el diseño de `Aggregate`s, `Entity`s y `Value Object`s, además de las façades \(`Application Service`s\) y boundaries de cada servicio

## Achievements

* **The team can recognize differences between DDD concepts and patterns:** En un equipo de desarrollo nuevo en DDD existen dudas entre las diferentes estructuras presentes:
  * `Application Service` vs `Domain Service` : La diferencia más evidente es que un domain service contiene lógica de dominio que no encaja en un Aggregate, entity o value object aunque existen muchas otras respondabilidades
    * Application Service
      * Authorization
      * Manage Transactions
      * Valida input en cuanto a estructura o firma del servicio
      * Acts as a high level abstraction \(façade\) for external clients \(rest api, ui, etc\), y
      * Todo lo que tenga que ver con la lógica de aplicación como sessions, authorization, etc
    * Domain Service
      * Contiene lógica de dominio que no encaja bien en otra estructura de dominio \(agreggate, entity, etc\) o que necesita hacer uso de un repository
  * `Repository` vs `DAO` : La principa diferencia es que un `DAO` retorna objetos anémicos mientras que un `Repository` retorna objetos de Dominio con estado, comportamiento e invariants de dominio teniendo las siguientes responsabilidades:
    * `Repository`_:_ Su responsabilidad es retornar colecciones de aggregates \(no es encargado de entregar `Value Object`s o `Entity`s\) bajo ciertos criterios definidos
    * `DAO`_:_ Es el patrón típicamente usado por los ORMs, cuyo pricipal objectivo es mapear una tabla \(o documento en el caso de NoSQL\) a un objeto de una clase definida conocidos como `Transfer Object`
  * `Aggregate Root` vs `Entity` vs `Value Object` : Si una entidad puede seguir existiendo cuando su aggregate es eliminado, esta entidad probablemente debería ser otro `Aggregate`; si un `Aggregate` no debería seguir existiendo cuando se elimina otro `Aggregate` relacionado, probablemente estos dos `Aggregate`s deberían ser uno solo
  * `Domain Object` vs `Transfer Object` \(and `DTO`\) : Un `Domain Object` tiene estado comportamiento e invariants, además esta expresado en ubiquitous language mientras que un `Transfer Object` o `Data Transfer Object`es una bolsa de datos sin encapsulamiento que se usa para transferir información entre capas. El nombre `Data Transfer Object` es más usado en la comunicación de servicios distribuídos aunque su concepto es el mismo
* **The team can recognize smells on bounded context and context map abstractions:** Algunos de los principales smells son los siguientes:
  * Chatty communication
  * Bad domain abstractions como por ejemplo: confundir un `Aggregate` por un `Entity` y viceversa



