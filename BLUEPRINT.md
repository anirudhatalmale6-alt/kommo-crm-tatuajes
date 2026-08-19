# Blueprint Kommo — Estudio de Tatuajes

**Versión 2 · 19 de agosto de 2026 · Plan Kommo: Avanzado**

Este es el mapeo propuesto de tus procesos dentro de Kommo. Es un documento de trabajo: corrígelo y devuélvemelo con notas.

**Cambios de la v1 a la v2, según lo que me confirmaste:**
- La calificación se reduce a tus 3 preguntas reales: zona del cuerpo, diseño o referencia, y tamaño aproximado en cm.
- Los pagos son manuales (medios locales o tarjeta), así que **no se conecta ninguna pasarela**. El anticipo se confirma a mano y el CRM se encarga solo de los recordatorios y del comprobante.
- Tu número ya está en WhatsApp Business API y Meta está verificado, así que la Fase 2 se acorta bastante.

---

## 1. Estructura general

Dos embudos separados, no uno solo. Meter todo en un embudo es el error más común: rompe los reportes y hace que las automatizaciones se disparen donde no deben.

| Embudo | Para qué sirve |
|---|---|
| **1. Pre-venta y Agenda** | Desde que llega el mensaje hasta que se hace la sesión. Citas, boceto, seña y recordatorios. |
| **2. Post-sesión y Fidelización** | Arranca cuando termina la sesión. Cuidados, encuesta, reseña, retoque y siguiente sesión. |

### Embudo 1 — Pre-venta y Agenda

| # | Etapa | Qué se dispara |
|---|---|---|
| 1 | Nuevo lead | Entra solo desde Instagram, Facebook, WhatsApp o web. El bot saluda. |
| 2 | Calificando | El bot pide las 3 cosas: **zona del cuerpo**, **diseño o referencia** (acepta imagen) y **tamaño aproximado en cm**. Rellena los campos solo. |
| 3 | Cotización enviada | Se manda el precio. Tarea automática de seguimiento a 48 h. |
| 4 | Consulta agendada | *(Opcional, si haces consulta previa)* Evento en Google Calendar + recordatorio 24 h y 2 h. |
| 5 | Boceto en proceso | Tarea para el artista. Aviso al cliente cuando esté listo. |
| 6 | Seña pendiente | El cliente aceptó. Se envían los datos de pago. Recordatorio a 24 h y 48 h. Sin seña a 72 h: etiqueta y tarea para ti. |
| 7 | Sesión agendada | Seña confirmada a mano. Evento en calendario + recordatorio 24 h y 2 h + indicaciones previas (comer antes, no alcohol, ropa cómoda). |
| 8 | Sesión realizada | Se cierra como ganado y pasa automáticamente al Embudo 2. |

**Motivos de pérdida:** sin respuesta · precio · agenda no coincide · no es nuestro estilo · se fue a otro estudio · solo preguntaba.

### Embudo 2 — Post-sesión y Fidelización

| # | Etapa | Qué se dispara |
|---|---|---|
| 1 | Cuidados enviados (día 0) | Cuidados post-tatuaje el mismo día, al terminar la sesión. |
| 2 | Encuesta enviada (día +2) | Encuesta corta de 1 a 5, el cliente responde con un número. |
| 3 | Reseña solicitada (día +7) | Reseña en Google y publicación o etiqueta en Instagram. **Solo si la encuesta dio 4 o 5.** |
| 4 | Recuperación | Encuesta de 3 o menos: NO se pide reseña. Tarea urgente para ti + etiqueta `recuperar`. |
| 5 | Retoque / siguiente sesión | Aviso a los 30 días para retoque, y recordatorio si el trabajo era de varias sesiones. |
| 6 | Cliente recurrente | Base para campañas futuras. Felicitación de cumpleaños opcional. |

> **El detalle que más plata deja:** nunca pedir reseña antes de saber si el cliente quedó contento. La encuesta filtra. Así solo se piden reseñas a quienes van a dejar 5 estrellas, y los descontentos llegan a ti antes que a Google.

---

## 2. Cómo queda el cobro de la seña (pagos manuales)

Como cobras por medios locales o tarjeta a mano, no hay pasarela que conectar. El flujo queda así:

1. El cliente acepta la cotización → el lead pasa a **Seña pendiente**.
2. El bot envía automáticamente tus datos de pago y el monto de la seña.
3. El cliente manda el comprobante por WhatsApp. La imagen queda guardada en el lead, no en el teléfono de nadie.
4. Alguien del equipo marca el campo **Seña pagada = Sí** (un clic).
5. Ese clic dispara solo: crea el evento en Google Calendar, manda la confirmación de la cita y programa los recordatorios de 24 h y 2 h.
6. Si a las 72 h no hay seña, salta la etiqueta y la tarea para ti.

Nadie tiene que acordarse de nada. Lo único manual es el clic de confirmación, que es justo lo que quieres controlar tú.

---

## 3. Campos personalizados

| Campo | Tipo | Valores / nota |
|---|---|---|
| Zona del cuerpo | Lista | Brazo · Antebrazo · Pierna · Espalda · Pecho · Costillas · Mano · Cuello · Otro |
| Diseño o referencia | Texto largo + archivo | Lo que el cliente quiere; el bot guarda la imagen que manda |
| Tamaño aproximado (cm) | Número | Base para el precio |
| Estilo | Lista | *(confirmar los que trabajan)* Fine line · Realismo · Blackwork · Tradicional · Geométrico · Lettering · Cover-up |
| Color o negro | Lista | Color · Negro y gris |
| Artista asignado | Lista | *(nombres de tu equipo)* |
| Precio cotizado / Precio final | Número | Para el reporte de ingresos |
| Seña (monto) | Número | |
| Seña pagada | Sí / No | El clic que dispara la confirmación de cita |
| Medio de pago usado | Lista | *(tus medios locales + tarjeta)* — solo para el reporte |
| Fecha y hora de sesión | Fecha-hora | Sincroniza con Google Calendar |
| Duración estimada (horas) | Número | Para bloquear bien la agenda |
| Nº de sesiones | Número | Trabajos grandes |
| Primera vez tatuándose | Sí / No | Cambia el tono de los mensajes previos |
| Alergias o condiciones médicas | Texto | Se pregunta antes de la sesión |
| Mayor de edad verificado | Sí / No | Bloqueo obligatorio antes de agendar |
| Consentimiento firmado | Sí / No | Checklist del día de la sesión |
| Origen | Lista | Instagram · Facebook · WhatsApp · Google · Referido · Walk-in |
| Puntuación encuesta | Número 1-5 | Lo llena el bot |
| Reseña dejada | Sí / No | Reporte de reseñas conseguidas |

En el contacto: **Instagram**, **cumpleaños** y **preferencia de contacto**.

## 4. Etiquetas

`caliente` · `tibio` · `frío` · `cover-up` · `retoque` · `gran-formato` · `primera-vez` · `recurrente` · `VIP` · `recuperar` · `no-molestar` · `fuera-de-estilo`

`no-molestar` es la más importante para WhatsApp: toda automatización la respeta y no vuelve a escribir a ese contacto nunca. Es la diferencia entre un número sano y un número bloqueado.

---

## 5. Plantillas de WhatsApp

Meta exige plantilla aprobada para escribir primero o fuera de la ventana de 24 h.

| Plantilla | Categoría Meta | Cuándo se envía |
|---|---|---|
| bienvenida_consulta | Utility | Primer contacto fuera de ventana |
| cotizacion_seguimiento | Utility | 48 h sin respuesta tras cotizar |
| boceto_listo | Utility | Cuando el artista termina el diseño |
| sena_pendiente | Utility | Al entrar a la etapa y a las 24 h / 48 h |
| recordatorio_consulta | Utility | 24 h y 2 h antes de la consulta |
| recordatorio_sesion | Utility | 24 h y 2 h antes de la sesión, con indicaciones previas |
| cuidados_post_tatuaje | Utility | Día 0, al cerrar la sesión |
| encuesta_satisfaccion | Utility | Día +2 |
| solicitud_resena | Marketing | Día +7, solo si la encuesta fue 4 o 5 |
| recordatorio_retoque | Utility | Día +30 |
| reactivacion | Marketing | Lead frío, máximo 1 intento |

Las **Utility** pasan aprobación casi siempre y no cuentan como publicidad. Las **Marketing** son las que hacen que la gente reporte el número, por eso solo hay dos y con condiciones estrictas.

---

## 6. Tope diario de WhatsApp y reglas de envío

> **Kommo NO trae tope diario nativo.** Hay que construirlo. Además Meta asigna niveles de envío: 1.000 → 10.000 → 100.000 conversaciones iniciadas por número cada 24 h, y sube solo si tu calidad se mantiene alta. Si te reportan, baja el nivel o te suspenden el número.

1. **Contador real de envíos.** Un servicio pequeño que levanto yo y al que el Salesbot consulta antes de cada envío saliente (el plan Avanzado permite bloques HTTP). Si ya se llegó al tope del día, el mensaje **se encola para el día siguiente en vez de perderse**. Propongo empezar en 150/día y subir según responda Meta.
2. **Ventana horaria.** Nada de mensajes automáticos fuera de 09:00–20:00 ni domingos. Un recordatorio a las 3 de la mañana es reporte seguro.
3. **Tope por contacto.** Máximo 1 mensaje automático por persona al día y 3 en total sin respuesta. Después se corta y queda tarea para atención humana.
4. **Anti-duplicado.** Si dos automatizaciones coinciden, sale una sola.
5. **Respeto de `no-molestar`** y botón de baja en las plantillas de marketing.
6. **Preferir la ventana de 24 h.** Si el cliente escribió en las últimas 24 h, el mensaje sale libre, no consume plantilla ni cuenta como conversación iniciada. La secuencia está diseñada para caer dentro de la ventana siempre que se pueda.

### Buenas prácticas para el equipo
- Nunca importar y escribir en frío a listas de otro sistema. Causa número uno de baneo.
- Responder rápido: la calidad del número sube cuando la gente contesta y no reporta.
- Nada de mandar el mismo texto idéntico a cientos de contactos a la vez.
- Si un cliente pide que no le escriban, etiqueta `no-molestar` en el momento.
- Revisar el estado de calidad del número en WhatsApp Manager una vez por semana.

---

## 7. Google Calendar

- Al confirmar la seña y llenar "Fecha y hora de sesión" se crea el evento con nombre del cliente, artista, zona y duración.
- Si mueves o cancelas la cita en Kommo, el evento se actualiza.
- Un calendario por artista si trabajan varios, para que no se pisen las agendas.
- La autorización de Google la das tú con un clic; te paso las capturas.

## 8. Reportes configurados

- Leads por origen (qué red te trae clientes de verdad, no solo mensajes)
- Conversión por etapa: dónde se caen. Normalmente entre cotización y seña
- Motivos de pérdida
- Ingresos por artista y por estilo
- Tiempo de primera respuesta
- Promedio de encuesta y reseñas conseguidas
- Mensajes enviados por día contra el tope

---

## 9. Checklist de pruebas

Nada se da por entregado hasta que esto pase completo con un número real:

- [ ] Mensaje entrante de Instagram crea lead en etapa 1 con el origen correcto
- [ ] Mensaje entrante de WhatsApp crea lead y no duplica si el contacto ya existe
- [ ] El bot captura zona, referencia (incluida imagen) y tamaño en los campos
- [ ] Cotización enviada genera la tarea de seguimiento a 48 h
- [ ] Marcar "Seña pagada = Sí" crea el evento en Google Calendar con el artista correcto
- [ ] Recordatorio de 24 h llega a la hora correcta
- [ ] Recordatorio de 2 h llega a la hora correcta
- [ ] Reprogramar la cita en Kommo mueve el evento del calendario
- [ ] Sin seña a 72 h se crean la tarea y la etiqueta
- [ ] Cierre de sesión mueve el lead al Embudo 2 automáticamente
- [ ] Cuidados post-tatuaje salen el mismo día
- [ ] Encuesta sale al día +2 y guarda la puntuación en el campo
- [ ] Puntuación 5 → pide reseña al día +7
- [ ] Puntuación 2 → NO pide reseña, crea tarea urgente y etiqueta `recuperar`
- [ ] Etiqueta `no-molestar` detiene todos los envíos a ese contacto
- [ ] Al llegar al tope diario, el envío tope+1 se encola y sale al día siguiente
- [ ] Fuera de la ventana horaria no sale ningún mensaje automático
- [ ] Ninguna automatización manda dos mensajes iguales al mismo contacto
- [ ] Los reportes muestran datos reales tras cargar 3 leads de prueba

---

## 10. Plan de trabajo

| Fase | Qué se hace | Qué necesito de ti |
|---|---|---|
| 0 | **Resolver el error 3107** y auditar lo que dejó la persona anterior. Informe de qué sirve y qué hay que borrar. | Capturas de Meta + token de API de Kommo |
| 1 | Embudos, etapas, campos, etiquetas y motivos de pérdida | Tus correcciones a este documento |
| 2 | Plantillas cargadas para aprobación de Meta | — (tu número ya está en API) |
| 3 | Google Calendar + automatizaciones del Embudo 1 | Un clic de autorización de Google |
| 4 | Automatizaciones del Embudo 2 (cuidados, encuesta, reseña, retoque) | — |
| 5 | Tope diario, reglas de envío y documento de buenas prácticas | — |
| 6 | Reportes, checklist ejecutado y guía de uso para el equipo | 30 min para revisarlo juntos por chat |

---

## 11. Pendiente de confirmar

1. ¿Haces consulta previa presencial o videollamada, o cotizas y agendas directo? (define si la etapa 4 se queda o se borra)
2. ¿Cuántos artistas y cómo se reparten los leads? ¿Por estilo, por turno, o uno solo?
3. ¿Cuánto cobras de seña? ¿Monto fijo o porcentaje?
4. Estilos que trabajan y zona horaria del estudio.
5. ¿Qué hay hoy en tu cuenta que SÍ quieres conservar?

---

*Blueprint v2 · Proyecto Kommo CRM Tatuajes · Anirudha Talmale · 19/08/2026*
