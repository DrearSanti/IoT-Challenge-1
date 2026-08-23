# Monitor Hídrico Sabana Centro — Sistema IoT de Alerta Temprana por Desabastecimiento

Prototipo funcional de un sistema IoT de bajo costo para monitorear la disponibilidad y escasez de agua en puntos críticos de suministro y almacenamiento en la región Sabana Centro (Cundinamarca), con notificación de alerta in situ sin uso de redes de comunicación.

La documentación técnica completa se encuentra en la sección **Wiki** de este repositorio.

---

## Descripción del Proyecto

El sistema integra cuatro variables ambientales (nivel de agua, temperatura, humedad relativa y radiación solar) mediante una lógica de fusión que genera un índice de riesgo compuesto. Ante condiciones concurrentes de descenso de nivel y alta evaporación potencial, el prototipo emite alertas visuales y sonoras de forma autónoma, sin depender de infraestructura de comunicaciones.

---

## Objetivos Técnicos

- Diseñar un sistema embebido de monitoreo hidrometeorológico de bajo costo.
- Integrar sensores de nivel de agua y variables meteorológicas en una sola plataforma.
- Implementar una lógica de fusión multivariable que combine señales heterogéneas en un índice de riesgo único.
- Generar alertas escalonadas por severidad mediante notificación in situ (visual y sonora).
- Operar de forma autónoma sin redes de comunicación convencionales.
- Documentar el proceso de diseño, desarrollo, implementación y validación.

---

## Tecnologías y Componentes Utilizados

- Arduino UNO R3 (microcontrolador ATmega328P)
- BME280 — temperatura, humedad relativa y presión atmosférica (I2C)
- AJ-SR04M — sensor ultrasónico de nivel de agua
- TCS230 — sensor de luz como proxy de radiación solar
- LCD 16x2 con backpack I2C — visualización in situ
- LEDs semáforo y buzzer — notificación de alerta
- Pulsadores — interfaz de navegación local
- Lenguaje C/C++ (Arduino IDE)
- EEPROM interna para persistencia de histórico

---

## Características del Sistema

- Muestreo no bloqueante con temporizadores independientes por sensor
- Lógica de fusión mediante índice de riesgo ponderado y normalizado
- Umbral duro de emergencia independiente del índice compuesto
- Menú jerárquico navegable con dos pulsadores
- Punto de partida configurable por el usuario como línea base de comparación
- Histórico semanal persistente en EEPROM
- Modo de simulación para demostración

---

## Información Académica

- Asignatura: Internet de las Cosas
- Institución: Universidad de La Sabana
- Facultad: Ingeniería
- Profesor: Juan Manuel Aranda López
- Periodo: 2026-2
- Entrega: Challenge #1

---

## Autores

- Santiago Escobar
- [Nombre del segundo integrante]

---

## Estructura del Repositorio

- **Wiki** — Documentación técnica completa
- **/codigo** — Código fuente documentado (.ino)
- **/esquematicos** — Esquemáticos de hardware y diagramas
- **/evidencias** — Fotografías y registros de las pruebas
- **Video demostrativo** — [Enlace pendiente]