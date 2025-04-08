---
marp: true
author: Federico Bond
theme: itba
paginate: true
---

# Clase 2: Ingeniería de Requerimientos
_Ingeniería de Software I_

---

## Objetivos de la clase

- Comprender qué son los requerimientos en ingeniería de software y su rol en el ciclo de desarrollo
- Reconocer los distintos tipos de requerimientos y las formas tradicionales de clasificarlos
- Identificar stakeholders y aplicar técnicas para la elicitación efectiva de requerimientos
- Redactar y evaluar requerimientos claros, verificables y trazables

---

## ¿Qué es un requerimiento?

- Una condición o capacidad que un sistema debe satisfacer para cumplir con una necesidad
- Requerimientos como punto de partida del diseño, desarrollo y pruebas
- Desde Farley: los requerimientos son **hipótesis** hasta que se validan

### Ejemplo:
> "El sistema debe permitir registro con email" vs.
> "Creemos que el registro por email mejora la conversión: lo validaremos con métricas"

---

## Tipos clásicos de requerimientos

- **Requerimientos funcionales**
  Definen comportamientos, funciones, servicios

- **Requerimientos no funcionales**
  Definen restricciones de calidad o condiciones del entorno

- **Requerimientos de dominio / restricciones**
  Provienen del entorno o regulaciones externas

---

## Tipos clásicos de requerimientos

- **Requerimientos funcionales**
  Ej: "El sistema debe permitir que el usuario modifique su perfil"

- **Requerimientos no funcionales**
  Ej: "El sistema debe responder en menos de 2 segundos el 95% del tiempo"

- **Requerimientos de dominio / restricciones**
  Ej: "El sistema debe responder en menos de 2 segundos el 95% del tiempo"

---

## Por qué esta clasificación es útil

- Es el estándar en documentación técnica y plantillas formales (ej. IEEE 830)
- Facilita la organización y trazabilidad
- Es requerida en auditorías, licitaciones, contratos
- Útil para roles específicos: testers, arquitectos, legales

---

## Pero... ¿y si esta división es artificial?

> "No hay requerimientos no funcionales, solo decisiones de diseño técnico que afectan el comportamiento del sistema."
> — Dave Farley

### Problemas con la separación rígida:
- Lo "no funcional" suele ser más crítico y difícil de cumplir
- Puede quedar olvidado o no implementado correctamente
- Afecta directamente la experiencia del usuario y la arquitectura del sistema

---

## Ejemplos comparativos

| Requerimiento funcional | Requerimiento "no funcional" |
|--------------------------|-------------------------------|
| "El sistema debe permitir iniciar sesión" | "Debe seguir estándar OAuth2 y registrar intentos fallidos" |
| "El sistema debe permitir pagar con tarjeta" | "Debe procesar pagos en menos de 500ms en el 95% de los casos" |

> Ambos afectan directamente el diseño, testeo y mantenimiento del sistema

---

## ¿Qué hacemos con esta clasificación?

### En este curso:
- **Sí la usamos**, porque es un lenguaje estándar que deben conocer
- **Pero también la cuestionamos**, porque el pensamiento crítico es parte de la formación

### Lo importante:
- Entender cómo cada requerimiento (sea del tipo que sea) **afecta al sistema completo**
- Diseñar, testear y evolucionar el sistema en función de **todas sus restricciones y expectativas**

---

## Stakeholders y análisis de necesidades

- Identificación de actores clave: usuarios, negocio, legales, IT, etc.
- Técnicas: entrevistas, mapas de poder/interés, observación
- Stakeholders ignorados → requerimientos faltantes o contradictorios

### Actividad sugerida:
> Crear un mapa de stakeholders para un sistema de reservas online

---

## Técnicas de elicitación de requerimientos

- Entrevistas, encuestas, workshops, prototipos, análisis de tareas
- Herramientas visuales: wireframes, storyboards
- Wiegers: detectar supuestos ocultos y necesidades implícitas
- Farley: el aprendizaje y la exploración como parte del diseño

### Actividad:
> Simular una entrevista analista–cliente y analizar los requerimientos descubiertos

---

## Especificación clara y estructurada

- Lenguaje natural estructurado, historias de usuario, casos de uso
- Modelos: UML (casos de uso, actividad), BPMN
- Criterios: claridad, consistencia, trazabilidad, verificabilidad

### Ejemplo:
> Historia de usuario: "Como cliente, quiero recibir una confirmación por email al hacer un pedido"

---

## Validación y verificación

- Validación con stakeholders: revisiones, prototipos, pruebas de aceptación
- Farley: pruebas automatizadas como forma continua de validar requerimientos
- Integración en CI/CD y pipelines

### Actividad:
> Diseñar criterios de aceptación para una funcionalidad clave

---

## Gestión de requerimientos

- Trazabilidad entre requerimientos, código y pruebas
- Control de versiones y manejo de cambios (baselines)
- Priorización: MoSCoW, Kano, WSJF

### Ejemplo:
> Cambio de requerimiento: "La app debe funcionar offline" → ¿Qué impacto tiene?

---

## Requerimientos en entornos ágiles y DevOps

- Backlogs, épicas, historias de usuario, criterios de aceptación
- Refinamiento continuo, validación con datos reales (telemetría, métricas)
- Farley: feedback como parte de la ingeniería moderna

### Actividad:
> Transformar requerimientos clásicos en historias de usuario + definición de hecho

---

## Requerimientos como hipótesis

- Cada requerimiento representa una suposición sobre lo que se necesita
- Validación a través de MVPs, experimentos, A/B testing
- Ingeniería moderna como proceso empírico

### Ejemplo:
> "Creemos que el login con Google aumentará registros" → Validar con feature flags y métricas

---

## Cierre – Buenas prácticas y errores comunes

### Buenas prácticas:
- Documentar claramente
- Validar continuamente
- Incluir requerimientos operativos desde el inicio

### Errores comunes:
- Ambigüedad
- Suposiciones no verificadas
- Requerimientos sin dueño

### Actividad:
> Analizar un caso con problemas de requerimientos y proponer mejoras
