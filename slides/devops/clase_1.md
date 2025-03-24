---
marp: true
author: Federico Bond
theme: itba
paginate: true
---
<style>
    .container {
        display: flex;
        gap: 2em;
        align-items: flex-start;
    }
    .col {
        flex: 1;
    }
</style>

# Clase 1: Fundamentos y Orígenes de DevOps
_Practicas Modernas de Desarrollo y Operaciones_

---

## Objetivos de la Clase
- Comprender el contexto histórico del surgimiento de DevOps
- Introducir los principios fundamentales de DevOps
- Relacionar DevOps con movimientos como Lean y Agile

---

## ¿Qué es DevOps?
- Cultura + Prácticas + Herramientas
- Colaboración entre Desarrollo (Dev) y Operaciones (Ops)
- Objetivo: entregar valor al cliente más rápido y con mayor calidad

> “DevOps is the outcome of applying Lean principles to the IT value stream.”
> – Gene Kim (The DevOps Handbook)

<!--
Es importante enfatizar que el enfoque DevOps no es solo tecnológico, sino que también involucra cambios culturales y organizacionales.

Tradicionalmente, el equipo de desarrollo busca innovar y añadir nuevas funcionalidades con rapidez, mientras que el equipo de operaciones busca estabilidad y seguridad. En muchas organizaciones estos objetivos están contrapuestos. DevOps busca alinear estos objetivos y crear un flujo de trabajo más eficiente y colaborativo.
-->


---

![bg fit 70%](../images/Devops-toolchain.svg)

---

## Problemas Tradicionales en IT
- Silos organizacionales
- Procesos manuales y frágiles
- Despliegues poco frecuentes
- Tiempo largo para resolver errores

<!--
Los equipos de desarrollo y operaciones tradicionalmente trabajan de forma aislada y no se comunican eficientemente. Desarrollo no quiere divulgar mucho sobre los cambios porque teme que operaciones los rechace, y operaciones no quiere que desarrollo haga cambios sin su aprobación. Cada equipo tiene sus propios objetivos y prioridades, y optimizan localmente en lugar de optimizar el sistema completo.

Procesos manuales y frágiles: los procesos de desarrollo, testing y despliegue son manuales y propensos a errores. Los cambios se realizan de forma manual y no hay una forma estandarizada de hacerlo.

Por esta razón, los despliegues son poco frecuentes y se realizan con mucho cuidado. Cada despliegue es un evento estresante y se intenta minimizar la cantidad de cambios para reducir el riesgo. Esto lleva a despliegues menos granulares, lo que se traduce en una mayor propensión a errores, por la amplificación del riesgo que significa introducir múltiples cambios de una sola vez.

Finalmente, cuando ocurren errores en producción, el tiempo para resolverlos es largo. Los equipos de desarrollo y operaciones se culpan mutuamente y se pierde tiempo valioso en identificar la causa raíz del problema. La información sobre el error no se comparte de forma eficiente y se pierde en la comunicación entre los equipos.

Esta es la forma en la que todavía trabajan muchas organizaciones, y es lo que DevOps busca cambiar.
-->

---

## Orígenes del Movimiento DevOps
- Agile sin operaciones
- Patrick Debois y Andrew Shafer (2008)
- Necesidad de entrega continua (Continuous Delivery)
- Influencias: Lean Manufacturing, Agile, Theory of Constraints

<!--
Con la adopción de metodologías ágiles, los equipos de desarrollo comenzaron a entregar valor de forma más rápida y frecuente. Sin embargo, la operación de sistemas no estaba alineada con estos objetivos. Los despliegues seguían siendo manuales y poco frecuentes, y la comunicación entre desarrollo y operaciones era deficiente.

En 2009, Patrick Debois y Andrew Shafer organizaron la primera conferencia DevOpsDays en Gante, Bélgica. En esta conferencia se discutieron los problemas de comunicación entre desarrollo y operaciones y la necesidad de alinear los objetivos de ambos equipos. La conversación continúa en Twitter, donde Dubois propone el hashtag #DevOps.
-->
---

## Línea de Tiempo del Movimiento DevOps

- 1950s–1980s: Toyota Production System – Lean Manufacturing
- 2001: Manifiesto Ágil
- 2006: "Continuous Integration" – Martin Fowler
- 2007: Jez Humble y David Farley inician Continuous Delivery
- 2008: Patrick Debois organiza DevOpsDays
- 2010: Publicación de "Continuous Delivery"
- 2013: "The Phoenix Project" de Gene Kim
- 2014+: Informes anuales de *State of DevOps* por DORA

---

## Influencias Clave

* **Lean IT**
    Flujo de valor (*value stream*), eliminación de desperdicios, mejora continua

* **Agile**
    Feedback constante, equipos multifuncionales, iteraciones

* **Teoría de Restricciones**
    Enfocarse en el cuello de botella

---

## Lean IT

- Adaptación de Lean Manufacturing al ámbito de IT
- Inspirado en el Toyota Production System
- Entrega de valor eliminando desperdicios
- Flujo continuo, WIP limitado, Kaizen

---

## Principios de Lean Manufacturing / Lean IT

1. **Identificar y definir el valor**: Qué es valioso para el cliente
2. **Mapear el flujo de valor**: Identificar el proceso completo
3. **Eliminar desperdicios**: Actividades que no agregan valor
4. **Crear flujo continuo**: Entrega sin interrupciones
5. **Establecer un sistema pull**: Trabajar en base a la demanda
6. **Buscar la perfección**: Mejora continua (*Kaizen*)

---

## Agile
- Manifiesto Ágil (2001)
- Agile introdujo ciclos de desarrollo cortos, iterativos y basados en feedback rápido.
 - DevOps amplía esta mentalidad hacia operaciones, extendiendo el ciclo de vida del software hasta producción.

---

## Agile

Ambas culturas comparten principios fundamentales:

  - Entrega continua de valor al cliente
  - Adaptación al cambio
  - Equipos pequeños, autónomos y multidisciplinarios
  - DevOps es una evolución natural de Agile que abarca todo el sistema sociotécnico

---

## Teoría de las Restricciones

- Propuesta por Eliyahu Goldratt en el libro La Meta (1984).
- Es un enfoque de mejora continua que parte de una idea simple:
“Un sistema es tan fuerte como su eslabón más débil.”
- Enfocarse en el cuello de botella
- Aplicación en procesos como despliegue y pruebas

---

## Teoría de Restricciones

1. Identificar la restricción (el cuello de botella).
2. Explotar la restricción (maximizar su rendimiento).
3. Subordinar todo lo demás a la restricción.
4. Elevar la restricción (mejorarla o eliminarla).
5. Volver al paso 1 (es un proceso iterativo).

---

*DevOps* toma esta idea para optimizar el flujo de valor desde el desarrollo hasta producción.

##### Algunas restricciones comunes en IT:


-  El proceso de testing manual
-  Aprobaciones de cambio lentas
-  Entornos de staging mal configurados
-  Integración y entrega no automatizadas

En lugar de optimizar todo al mismo tiempo, se focaliza el esfuerzo donde el sistema realmente se traba.

---

## Los tres caminos (Three Ways) de DevOps
1. **Flujo:**
    Entrega continua desde desarrollo hacia producción
2. **Feedback:**
    Retroalimentación rápida desde producción hacia desarrollo
3. **Aprendizaje Continuo:**
    Cultura de experimentación y mejora constante

---

## Primer camino – Flujo

Optimizar el flujo de entrega de valor al cliente.
Enfocarse en reducir el tiempo de ciclo y los cuellos de botella.

<hr>

##### Prácticas asociadas:

 - Integración continua (CI)
 - Entrega continua (CD)
 - Infraestructura como código
 - Pipelines automatizados

---

## Segundo camino – Feedback

Crear ciclos de retroalimentación rápidos y frecuentes.
Detectar y resolver problemas rápidamente.

<hr>

##### Prácticas asociadas:

 - Monitoreo y alertas en tiempo real
 - Revisiones post-mortem sin culpa
 - Comunicación abierta entre Dev y Ops
 - Feature flagging para pruebas controladas

---

## Tercer camino – Aprendizaje Continuo

Fomentar la experimentación, el aprendizaje y la mejora continua.
Aceptar el fracaso como parte del proceso de innovación.

<hr>

##### Prácticas asociadas:

 - Automatización de pruebas
 - Cultura de seguridad psicológica
 - Revisión de incidentes como oportunidad de mejora
 - Experimentación controlada (A/B testing, canary releases)

---

<!-- _class: lead -->
<!-- _paginate: "" -->

# DORA
## La introducción de la ciencia en DevOps

---

## DORA: DevOps Research and Assessment

* Equipo de investigación respaldado por Google.

* Utiliza encuestas masivas y análisis estadístico para encontrar qué prácticas técnicas y culturales mejoran el rendimiento organizacional.

* Desde 2014 publica el informe State of DevOps Report, uno de los más influyentes en la industria.


---

## 4 métricas clave

<div class="container">
<div class="col">

- **Change Lead Time**: Tiempo desde commit hasta producción

- **Deployment Frequency**: Frecuencia con la que se despliega a producción

</div>
<div class="col">

- **Change Fail Rate**: % de despliegues que causan fallos en producción

- **Failed Deployment Recovery Time**: Tiempo promedio para restaurar el servicio luego de un cambio que ocasionó un fallo

</div>
</div>

<!--
Las métricas de la izquierda miden la eficiencia del flujo de trabajo, mientras que las de la derecha miden la calidad y estabilidad del sistema. Las métricas de la izquierda están más asociadas a los objetivos de desarrollo, mientras que las métricas de la derecha están más asociadas a los de operaciones. Sin embargo, van a ver que todas requieren de una colaboración estrecha entre ambos equipos para ser mejoradas.
-->

---

<!-- _class: blank -->
<!-- _paginate: "" -->

![bg fit](../images/dora-metrics.png)

---

<!-- _class: blank -->
<!-- _paginate: "" -->

![bg fit 90%](../images/dora-core-v2.0.0-summary.png)

<!-- Quiero remarcar lo importante que es este resultado, recién en los últimos 5-10 años contamos con evidencia empírica de qué prácticas funcionan y cuáles no para desarrollar software. Si algo quiero que se lleven de esta clase, y que se lo cuenten a sus compañeros es que hay una serie de prácticas de ingeniería de software que tienen una base científica. No tienen que creer en DevOps porque lo dice un gurú, sino porque hay evidencia que demuestra que estas prácticas funcionan.
-->

---

## Beneficios de DevOps
- Despliegues seguros y frecuentes
- Respuesta rápida ante incidentes
- Satisfacción del cliente
- Cultura colaborativa y resiliente

---

## Lecturas Recomendadas
- *The DevOps Handbook* – Capítulos 1 y 2
- *The Phoenix Project* – Prólogo y primeros 5 capítulos
- *Accelerate* – Capítulo 1

---

## Cierre
- DevOps es cultura, no sólo tecnología
- DevOps busca alinear objetivos de desarrollo y operaciones, priorizando la entrega de valor al cliente
- Las prácticas de DevOps cuentan con una sólida base científica y han demostrado mejorar el rendimiento organizacional y el bienestar de los equipos
- ¡Bienvenidos al curso!
