# Informe entrevista cargo

---

## Resumen de audio (Podcast)  
[Link al audio](https://drive.google.com/drive/folders/1BzfVwnLjr28JTa-17YvbX09Ks3oj0xEY?usp=drive_link)

---

## Resumen de video  
[Link al video](https://drive.google.com/drive/folders/1XXo5IU8m9eFkTR_5iYbqoWg4yUnszclA?usp=drive_link)

---

## Mapa mental  
[Link al mapa mental](https://drive.google.com/drive/folders/1ACbnacfzMyvRDIesK9CygiqFUrNrdHp0?usp=drive_link)

---

## Documento informativo: Ingeniería de backend para sistemas financieros de gran escala

Este documento resume temas, ideas y hechos clave de los extractos de entrevistas proporcionados sobre ingeniería de back-end, particularmente en un contexto financiero con alta escalabilidad y demandas regulatorias.

---

### I. Principios arquitectónicos básicos para la escalabilidad y la flexibilidad

La entrevista destaca un énfasis constante en dos enfoques arquitectónicos principales:

- **Arquitectura de microservicios**  
  Enfoque fundamental para diseñar módulos backend configurables y escalables. Permite servicios independientes, lo que brinda adaptabilidad a regulaciones locales y manejo eficiente de transacciones.  
  > "Para diseñar los módulos de back configurables utilizaríamos una arquitectura en microservicios con una capa de configuración centralizada. Cada módulo estaría diseñado como un servicio independiente..."

- **Escalabilidad Horizontal**  
  Crucial para gestionar un crecimiento significativo en el volumen de transacciones. Se combina con microservicios para permitir la expansión agregando más recursos.  
  > "Para soportar esta cantidad de transacciones, usaríamos una metodología de diseño basada igualmente en microservicios con una arquitectura escalable horizontal..."

---

### II. Diseño para el cumplimiento normativo y la adaptabilidad

- **Capa de Configuración Centralizada**: Maneja regulaciones locales y distribuye normativas a microservicios.  
- **Cambios regulatorios incrementales**: Implementados con entrega continua, despliegue automatizado, pruebas automatizadas y revisión de código.  
- **Monitoreo y alerta**: Proactivo para detectar problemas por cambios regulatorios.

---

### III. Escalabilidad para volúmenes masivos de transacciones

Escalar de **180 millones a 800 millones de transacciones anuales** requiere:

- **Colas de mensajes (Apache Kafka o RabbitMQ)** para gestionar el flujo de datos.  
- **Monitoreo y ajuste continuo** para adaptar la arquitectura al crecimiento.  
- **Mitigación de riesgos**:  
  - Escalabilidad y rendimiento → monitoreo y ajuste continuo.  
  - Errores de procesamiento → pruebas automatizadas y revisión de código.  
  - Fraude y seguridad → autenticación, autorización, cifrado y detección de fraude.

---

### IV. Rendimiento y confiabilidad de los servicios financieros

#### Objetivos críticos de desempeño  
- **Baja latencia**: <200 ms.  
- **Alto rendimiento en procesamiento**.  
- **Alta disponibilidad y escalabilidad**.

#### Estrategias para lograrlo  
- Optimización de consultas de base de datos.  
- Tecnologías de procesamiento de eventos como Apache Kafka.  
- Monitoreo continuo.

---

### V. Monitoreo avanzado y garantía de rendimiento

- **APM Technologies**: DataDog, New Relic.  
- **Alertas basadas en percentiles (P95 y P99)**: Identifican valores atípicos de rendimiento.  
- **Paneles y registros detallados**: Información granular por país/transacción.  
- **Creación periódica de perfiles de código**: Identificación de cuellos de botella.  
- **Gestión de colas lentas**: PostgreSQL.

---

### VI. Escalabilidad modular e incorporación de clientes

- **Arquitectura multiinquilino con aislamiento lógico**: Cada cliente con su propio espacio de datos.  
- **Onboarding asíncrono con colas**: Procesamiento en paralelo para evitar cuellos de botella.  
- **Servicios desacoplados y configuración de activación** para mantener estabilidad.

---

### VII. Desafíos y soluciones para la integración masiva de clientes

- **Validación de datos incompleta** → automatización con reglas configurables.  
- **Sobrecarga en sincronización de sistemas externos** → procesos asíncronos con workers distribuidos.  
- **Reintentos inteligentes y seguimiento de estado** → robustez en la integración.

---

### VIII. Integración segura con bancos y fintechs

- **OAuth 2.0**: Uso de flujos seguros (credenciales de cliente, código de autorización).  
- **TLS 1.3**: Configuración desde el proxy inverso (Nginx).  
- **Medidas de seguridad**: Escaneos periódicos, rotación de secretos y auditorías de accesos.

---

### IX. Criterios técnicos para la integración de diversos sistemas externos

- **Evaluación de compatibilidad**: REST, SOAP, gRPC.  
- **Diseño de adaptadores**: Traducción de protocolos sin afectar el core.  
- **Contratos de servicio y validación de esquemas**: Comunicación clara y datos íntegros.  
- **Pruebas de integración por entorno**.  
- **Requisitos regulatorios**: Cifrado, residencia de datos, trazabilidad.

---

## Conclusión

La entrevista proporciona una visión integral de las mejores prácticas en **ingeniería de backend para sistemas financieros de gran escala**, destacando:

- Uso de **microservicios**.  
- **Escalabilidad horizontal**.  
- **Monitoreo y alertas avanzadas**.  
- Fuerte enfoque en **seguridad** y **cumplimiento normativo**.

---

# Guía de estudio de ingeniería financiera de alto nivel

### I. Principios arquitectónicos básicos  
- Microservicios y escalabilidad horizontal como pilares fundamentales.

### II. Cumplimiento normativo  
- Capa de configuración centralizada.  
- Cambios incrementales con pruebas y CI/CD.

### III. Escalabilidad de transacciones  
- Apache Kafka y RabbitMQ.  
- Monitoreo y ajuste continuo.

### IV. Rendimiento crítico  
- Latencia <200 ms.  
- Optimización de consultas y eventos en tiempo real.

### V. Monitoreo avanzado  
- DataDog, New Relic, alertas P95/P99.

### VI. Escalabilidad modular  
- Arquitectura multiinquilino.  
- Onboarding asincrónico.

### VII. Retos en la integración masiva  
- Validación automatizada, procesos asincrónicos y reintentos inteligentes.

### VIII. Integración segura  
- OAuth 2.0 y TLS 1.3 con auditorías de seguridad.

### IX. Integración de sistemas externos  
- REST, SOAP, gRPC con adaptadores y contratos de servicio.

---

# Cuestionario (preguntas frecuentes): Ingeniería de backend financiero a gran escala

**Instrucciones**: Responda cada pregunta en 2–3 oraciones.

1. ¿Cuáles son los dos principios arquitectónicos fundamentales que se destacan para diseñar sistemas financieros escalables y flexibles a gran escala? ¿Cómo se complementan?  
2. ¿Cómo se utiliza una capa de configuración centralizada para gestionar diversas regulaciones locales en una arquitectura de microservicios?  
3. Describa la estrategia para implementar cambios regulatorios para evitar la inestabilidad del sistema.  
4. Nombre dos tecnologías cruciales para gestionar el flujo de datos y garantizar la escalabilidad con un alto volumen de transacciones.  
5. ¿Cuál es el objetivo explícito de baja latencia para las API críticas en un backend financiero de gran escala? ¿Cuáles son dos estrategias generales para lograrlo?  
6. ¿Cómo las alertas basadas en percentiles (P95 y P99) proporcionan una comprensión más sólida del rendimiento?  
7. Explique el concepto de una arquitectura multiinquilino con aislamiento lógico en el contexto de la incorporación de 2500 nuevas PYMES.  
8. ¿Cuáles son dos desafíos comunes identificados durante la integración masiva de clientes y cómo se resuelven normalmente?  
9. ¿Cuáles son los dos estándares de seguridad más importantes para una integración segura con bancos y FinTechs, y dónde se configura normalmente uno de ellos?  
10. ¿Cuál es el propósito de diseñar adaptadores y por qué son importantes los contratos de servicio al integrar sistemas externos?

---

# Cronología (Línea de tiempo)

- **Arquitectura de microservicios**: Estilo arquitectónico que estructura una aplicación como servicios independientes.  
- **Escalabilidad horizontal**: Incremento de capacidad agregando más nodos.  
- **Capa de configuración centralizada**: Servicio para distribuir configuraciones y normativas.  
- **Entrega continua (CD)**: Producción de software en ciclos cortos con despliegues confiables.  
- **Apache Kafka**: Plataforma de transmisión de eventos distribuidos.  
- **RabbitMQ**: Intermediario de mensajes basado en AMQP.  
- **Baja latencia**: Retardo menor a 200 ms.  
- **APM (Application Performance Monitoring)**: Herramientas para supervisar rendimiento.  
- **Alertas basadas en percentiles**: P95/P99 para identificar valores atípicos.  
- **Arquitectura multiinquilino**: Soporte a múltiples clientes con aislamiento lógico.  
- **OAuth 2.0 y TLS 1.3**: Estándares clave de seguridad.  
- **Adaptadores**: Traducen protocolos entre sistemas (REST, SOAP, gRPC).  
- **Contratos de servicio**: Especificaciones para comunicación clara y datos íntegros.

---

## Entrevista Completa

Puedes acceder a la entrevista completa en el siguiente enlace:

[Entrevista Completa](https://drive.google.com/drive/folders/1ezzhoo6Q_Qcm2Vk4mbGHzfF_iu6yO0wb?usp=drive_link)

## Trabajo Realizado

El trabajo fue realizado en la siguiente página:

[Notebook del Trabajo](https://notebooklm.google.com/notebook/1f662ec2-d298-4459-8055-49e9b38c30aa)
---
