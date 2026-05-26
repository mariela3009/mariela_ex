# Análisis Editorial Técnico-Académico
## Ensayo: "Automatización del Proceso de Onboarding Empresarial con n8n"
### Universidad Privada de Tacna — Ingeniería de Sistemas — Sistemas Operativos II

---

# 1. Análisis del Ensayo Actual

## 1.1 Estructura actual

El ensayo está redactado en formato de artículo académico con las siguientes secciones:

- **Encabezado:** Título en español e inglés, autores, correos, institución.
- **Resumen / Abstract:** Párrafos de aproximadamente 120 palabras cada uno.
- **Introducción:** Cuatro párrafos bien construidos que establecen el problema, el argumento central (utilidad, usabilidad y arquitectura), el alcance y la tesis.
- **Análisis:** Once subapartados que glosan fuentes y casos de estudio de manera individual (cada fuente tiene su propio bloque de análisis).
- **Desarrollo:** Tres grandes bloques — Utilidad del Sistema, Usabilidad del Sistema y Arquitectura del Sistema — con descripción técnica de los cinco workflows.
- **Discusión:** Cuatro párrafos de síntesis comparativa con evidencia empírica.
- **Conclusión:** Dos párrafos de cierre argumentativo.
- **Referencias:** 26 fuentes con formato APA heterogéneo.

## 1.2 Fortalezas

- **Redacción fluida y consistente:** El estilo académico es uniforme; los párrafos argumentan antes de afirmar.
- **Base empírica sólida:** 26 referencias reales y variadas (arXiv, SHRM, casos empresariales, artículos de revistas indexadas).
- **Arquitectura de cinco workflows bien descrita:** Los WF1–WF5 están detallados con lógica de nodos, bifurcaciones y tecnologías.
- **Tres ejes de análisis coherentes:** Utilidad, usabilidad y arquitectura forman un argumento completo.
- **PPT alineado:** Las diapositivas reflejan correctamente WF1–WF5 con diagramas visuales de los flujos.

## 1.3 Vacíos detectados

| Vacío | Impacto |
|---|---|
| No se justifica técnicamente la elección de **Debian 12** (el ensayo no menciona la distribución base; el PDF técnico usa Ubuntu 22.04 LTS) | La sección de arquitectura queda sin respaldo para la decisión de SO |
| El stack tecnológico real (**Mailcow, Mattermost, Nextcloud, GitLab, Plane.so, Telegram Bot**) se menciona en el desarrollo pero sin justificación técnica individual de cada herramienta | No se puede defender académicamente por qué cada herramienta fue elegida sobre sus alternativas |
| **Sin análisis de costos por escenario:** no hay tabla de costos piloto / producción / enterprise | El análisis económico es solo cualitativo |
| **Sin comparativa formal n8n vs Zapier vs Make** en formato tabular | La ventaja competitiva queda argumentada pero no demostrada visualmente |
| **Sin patrón EDA formal:** el ensayo menciona Event-Driven Architecture pero no la explica como patrón arquitectónico con sus capas | La fundamentación teórica de la arquitectura es superficial |
| **Sin cronograma técnico de implementación** | La sección de Desarrollo no incluye tiempos ni fases |
| **Sin KPIs cuantitativos propios del proyecto:** los KPIs se mencionan de manera dispersa en la discusión, pero no hay tabla consolidada | El aporte medible del sistema no queda sintetizado |
| **Sin análisis de ROI estructurado:** se menciona el 400% pero no se explica el cálculo | El argumento económico no es defendible sin la fórmula |
| **WF1 menciona "Google Sheets"** implícitamente en la descripción del flujo (base de datos referida como "Database" sin especificar) | Inconsistencia con la arquitectura final que usa PostgreSQL exclusivamente |
| **Sección de Análisis es demasiado larga y fragmentada:** cada fuente tiene su propio bloque de 3–4 párrafos, lo que genera repetición | El lector pierde el hilo argumentativo central |

## 1.4 Secciones que ya contienen información parcial relacionada con el nuevo contenido

| Responsable | Información ya presente en el ensayo |
|---|---|
| MARIELA (Infraestructura) | Docker Compose, PostgreSQL, Nginx, UFW, Fail2ban, HTTPS — todos mencionados en la sección de Arquitectura |
| IKER (Costos) | Referencia a USD 20–50/mes en la Discusión; comparación cualitativa con Zapier/Make |
| DAYAN (Arquitectura EDA) | Mención de EDA y n8n como orquestador en el párrafo inicial de Arquitectura |
| CRISTHIAN (KPIs/ROI) | KPIs dispersos en Discusión; ROI 400% mencionado en Resumen y Discusión |
| GABRIEL (Cronograma) | No hay información de cronograma. Es la única área completamente ausente |

---

# 2. Mapeo de Integración de Contenido

## 2.1 MARIELA — Arquitecto de Infraestructura

### Sección exacta de integración
**Sección: Desarrollo → Arquitectura del Sistema**
Subsección nueva sugerida: `3.3 Infraestructura del Servidor y Stack Tecnológico`

### Qué contenido ya existe
- Menciones a Docker Compose, PostgreSQL 15, Nginx, UFW, Fail2ban y script de backup.
- Descripción de requisitos de hardware (4 vCPUs, 8 GB RAM para producción media).
- Variables de entorno con `chmod 600`.

### Qué contenido falta
- **Justificación técnica de Debian 12** frente a Ubuntu Server u otras distribuciones (estabilidad, ciclo de soporte, consumo de memoria en entorno server, seguridad por defecto, footprint mínimo para Docker).
- **Justificación individual de cada componente del stack:** Mailcow (servidor de correo self-hosted con API REST), Mattermost (comunicación interna con webhooks nativos), Nextcloud (almacenamiento documental con API WebDAV/OCS), GitLab (repositorios y CI/CD para perfiles técnicos), Plane.so (gestión de proyectos con API REST), Telegram Bot API (alertas escalonadas de bajo latencia).
- **Arquitectura de contenedores:** diagrama lógico de los servicios Docker y sus redes internas.
- **Hardening:** TLS 1.3 forzado en Nginx, políticas SSH (deshabilitar PasswordAuthentication, cambiar puerto por defecto), variables `.env` con `chmod 600` y `chown root:root`.
- **Justificación del servidor único:** ventajas operativas y económicas de un servidor único modularizado con Docker versus arquitectura distribuida para el volumen de carga del proyecto.

### Cómo ampliarlo
Añadir un bloque de 4–5 párrafos estructurados (sin subtítulos internos, en párrafos continuos para mantener el estilo actual) que primero justifiquen la elección de Debian 12, luego describan el stack de servicios con su función real, y finalmente expliquen el hardening como capa de seguridad integrada. Incluir una tabla de servicios Docker con columnas: Servicio / Imagen / Puerto interno / Función.

### Qué eliminar o reorganizar
El párrafo actual que describe los requisitos de hardware es correcto pero debería reubicarse al inicio de esta subsección para contextualizar la justificación del servidor antes de entrar al stack.

---

## 2.2 IKER — Analista de Costos y Escalabilidad

### Sección exacta de integración
**Sección: Discusión** (ampliar el tercer párrafo existente sobre democratización)
Subsección nueva sugerida: `Análisis Económico y Proyección de Escalabilidad`

### Qué contenido ya existe
- Mención a USD 20–50/mes en discusión.
- Comparación cualitativa de n8n vs Zapier/Make (sin tabla).
- Ventaja de licencia open-source mencionada en introducción.

### Qué contenido falta
- **Tabla de tres escenarios** (Piloto / Expansión / Enterprise) con columnas: workflows activos, vCPUs, RAM, almacenamiento SSD, ejecuciones/día, costo mensual.
- **Comparativa tabular n8n vs Zapier vs Make** con columnas: modelo de licencia, costo workflows ilimitados, control de datos, vendor lock-in, escalabilidad.
- **Análisis de vendor lock-in:** por qué el modelo self-hosted elimina dependencia del proveedor.
- **Punto de migración a Kubernetes/Docker Swarm:** cuándo (umbral de +100 workflows concurrentes o +10,000 ejecuciones/día) y por qué.
- **Ahorro en horas-hombre calculado:** con base en la reducción de 4–8 h/empleado a 20–40 min, y un costo medio por hora de RRHH.

### Cómo ampliarlo
Insertar dos tablas (escenarios de hardware/costo y comparativa de plataformas) dentro de la sección de Discusión, precedidas por un párrafo introductorio en el estilo actual que contextualice el análisis económico como complemento de la evidencia empírica. La redacción de los párrafos que rodean las tablas debe conservar el tono argumentativo existente.

### Qué eliminar o reorganizar
El párrafo de discusión que actualmente mezcla el argumento de democratización con cifras sueltas de costo debe dividirse: un párrafo para el argumento cualitativo y uno para el cuantitativo (donde se insertan las tablas).

---

## 2.3 DAYAN — Especialista en Arquitectura de Software

### Sección exacta de integración
**Sección: Desarrollo → Arquitectura del Sistema** (ampliar el primer párrafo)
Subsección nueva sugerida: `3.2 Event-Driven Architecture: Fundamento Teórico y Aplicación`

### Qué contenido ya existe
- Mención de EDA como patrón en el primer párrafo de Arquitectura del Sistema.
- Descripción de n8n como "orquestador central".
- Referencia a desacoplamiento y reintentos automáticos.

### Qué contenido falta
- **Definición formal de EDA** como patrón arquitectónico: productor de eventos, event bus, consumidores desacoplados, procesamiento asíncrono.
- **Diferencia entre EDA y arquitecturas síncronas/monolíticas:** por qué EDA es superior para un proceso multi-sistema como onboarding.
- **Rol específico de n8n en la arquitectura EDA:** event bus (recibe y enruta eventos), orquestador (controla el flujo), middleware de integración (traduce protocolos entre sistemas heterogéneos).
- **Descripción formal de las capas arquitectónicas** con tabla: Capa / Componente / Tecnología / Función (Presentación, Orquestación, Integración, Persistencia, Seguridad, Monitoreo).
- **Flujo de eventos end-to-end:** desde el trigger del webhook hasta la actualización final en PostgreSQL, explicando cómo cada workflow consume el evento del anterior.
- **Resiliencia y tolerancia a fallos:** reintentos exponenciales, circuit breakers implícitos, notificación de errores.

### Cómo ampliarlo
Insertar entre el primer párrafo de "Arquitectura del Sistema" (EDA) y el párrafo de infraestructura un bloque de 3–4 párrafos que desarrollen el patrón teórico, más una tabla de capas arquitectónicas. El estilo debe mantener los párrafos continuos sin subtítulos internos, con una sola tabla como elemento de visualización.

### Qué eliminar o reorganizar
Nada debe eliminarse. El párrafo existente sobre EDA es el punto de partida correcto; simplemente debe expandirse con el contenido teórico que actualmente está ausente.

---

## 2.4 CRISTHIAN — Analista de Impacto y KPIs

### Sección exacta de integración
**Sección: Desarrollo** (antes de la Discusión)
Subsección nueva sugerida: `3.5 Métricas de Impacto, KPIs y Análisis de ROI`

### Qué contenido ya existe
- KPIs mencionados de manera dispersa: reducción del 70–80% en tiempo, ROI 400%, tasa de error 0% vs 5%, reducción de 6–8 h a <2 h semanales.
- Comparativa onboarding manual vs automatizado implícita en la Introducción (tabla de puntos de falla en el proceso manual).

### Qué contenido falta
- **Tabla comparativa formal onboarding manual vs automatizado** con columnas: Dimensión / Proceso Manual / Proceso Automatizado (tiempo total, errores, carga RRHH, satisfacción día 1, cumplimiento SLA, retención a 90 días).
- **Tabla consolidada de KPIs del sistema** con columnas: KPI / Fórmula / Baseline (Manual) / Target (Automatizado) / Frecuencia.
- **Cálculo estructurado del ROI:** fórmula explícita `ROI = ((Valor recuperado – Inversión) / Inversión) × 100`, con cifras de ejemplo realistas para una empresa de 50 empleados.
- **Reducción de rotación temprana:** vinculación entre onboarding de calidad y retención a 90 días (dato de BambooHR: 31% renuncia en primer año, concentrado en primeros 6 meses).
- **Ahorro en horas-hombre calculado:** 4–8 h manuales por ingreso vs <40 min automatizado, a un costo promedio de USD 15–25/h de RRHH.

### Cómo ampliarlo
Crear una subsección nueva `3.5` antes de la Discusión, con dos tablas y dos párrafos de análisis por cada tabla. La introducción a la subsección debe conectar con el argumento de utilidad ya desarrollado en `3.1`, presentando los KPIs como la evidencia cuantitativa de dicha utilidad.

### Qué eliminar o reorganizar
Los fragmentos dispersos de KPIs en la Discusión deben consolidarse en esta nueva subsección. La Discusión solo debería referenciar los KPIs ya presentados en `3.5`, no repetirlos.

---

## 2.5 GABRIEL — Gestor de Proyecto

### Sección exacta de integración
**Sección: Desarrollo** (al final, antes de la Discusión, o como subsección de Arquitectura)
Subsección nueva sugerida: `3.6 Cronograma de Implementación Técnica Ágil`

### Qué contenido ya existe
**Nada.** Esta es la única área completamente ausente en el ensayo actual. El ensayo describe el sistema pero no indica cómo se implementa en el tiempo.

### Qué contenido falta
- **Cronograma de 4.5 semanas** con descripción de actividades por semana.
- **Tabla de fases** con columnas: Semana / Actividades / Entregable / Responsable técnico.
- **Hitos clave:** servidor operativo (semana 1), webhooks activos (semana 2), integraciones completas (semana 3), hardening y pruebas (semana 4), validación y documentación (media semana final).
- **Metodología ágil aplicada:** justificación del enfoque iterativo (MVP en semana 2, expansión progresiva de funcionalidades).
- **Criterios de aceptación por fase:** cómo se valida que cada semana fue completada exitosamente.

### Cómo ampliarlo
Crear la subsección `3.6` con un párrafo introductorio que justifique la metodología ágil para proyectos de automatización, seguido de la tabla de cronograma. El párrafo debe explicar por qué 4.5 semanas es un plazo realista para el alcance del proyecto, referenciando la complejidad de las integraciones.

### Qué eliminar o reorganizar
Nada. Es contenido nuevo que no interfiere con lo existente.

---

# 3. Nuevo Índice Propuesto

```
Automatización del Proceso de Onboarding Empresarial con n8n
Universidad Privada de Tacna — Ingeniería de Sistemas

Resumen / Abstract
Palabras clave / Keywords

1. Introducción
   [Mantener estructura actual: 4 párrafos]

2. Análisis
   2.1 Onboarding tradicional y sus consecuencias organizacionales
       [Condensar los 11 bloques actuales en 4 párrafos temáticos:]
       2.1.1 Evidencia empírica sobre el impacto del onboarding deficiente
       2.1.2 n8n como plataforma de automatización: validación académica
       2.1.3 Arquitecturas de automatización empresarial con n8n
       2.1.4 Casos de implementación real documentados

3. Desarrollo
   3.1 Utilidad del Sistema: Las Funciones que las Empresas Necesitan
       [Mantener estructura actual — 5 párrafos]

   3.2 Event-Driven Architecture: Fundamento Teórico y Aplicación  ← NUEVA
       3.2.1 Definición y principios del patrón EDA
       3.2.2 n8n como event bus, orquestador y middleware de integración
       3.2.3 Capas arquitectónicas del sistema [TABLA]
       3.2.4 Flujo de eventos end-to-end y resiliencia

   3.3 Infraestructura del Servidor y Stack Tecnológico  ← NUEVA
       3.3.1 Justificación técnica de Debian 12 sobre Ubuntu Server
       3.3.2 Arquitectura de contenedores Docker y servicios del stack [TABLA]
       3.3.3 Hardening de seguridad: UFW, Fail2ban, TLS 1.3, SSH policies
       3.3.4 Justificación del servidor único modularizado vs arquitectura distribuida

   3.4 Usabilidad del Sistema: Operación Autónoma por Perfiles
       [Mantener estructura actual — 5 párrafos]

   3.5 Métricas de Impacto, KPIs y Análisis de ROI  ← NUEVA
       3.5.1 Comparativa onboarding manual vs automatizado [TABLA]
       3.5.2 KPIs consolidados del sistema [TABLA]
       3.5.3 Cálculo del ROI y retorno operativo

   3.6 Flujo Técnico Completo: Cinco Workflows Interdependientes
       [Renombrar y mantener la sección actual de arquitectura de workflows]
       3.6.1 WF1 — Recepción, Validación y Registro en PostgreSQL
       3.6.2 WF2 — Aprovisionamiento Técnico Automatizado
       3.6.3 WF3 — Documentación y Bienvenida
       3.6.4 WF4 — Monitoreo por SLA (30 días)
       3.6.5 WF5 — Pulso de Integración y Retroalimentación

   3.7 Cronograma de Implementación Técnica Ágil  ← NUEVA
       3.7.1 Metodología de despliegue iterativo
       3.7.2 Fases de implementación [TABLA: 4.5 semanas]
       3.7.3 Criterios de aceptación por fase

4. Discusión
   4.1 Evidencia empírica: pymes y grandes corporaciones
   4.2 Análisis económico y escalabilidad [TABLAS DE COSTOS]  ← AMPLIAR
       4.2.1 Escenarios de hardware y costo operativo [TABLA]
       4.2.2 Comparativa n8n vs Zapier vs Make [TABLA]
       4.2.3 Umbral de migración a Kubernetes o Docker Swarm
   4.3 Automatización completa vs parcial: el salto cualitativo
   4.4 Aporte estratégico para la transformación digital

5. Conclusión
   [Mantener estructura actual — 3 párrafos, ampliar ligeramente el segundo]

6. Referencias
   [Mantener y ordenar en APA 7 con consistencia]
```

---

# 4. Recomendaciones de Mejora Académica y Técnica

## 4.1 Partes que necesitan más teoría

| Sección | Teoría faltante |
|---|---|
| Arquitectura del Sistema (EDA) | Definición formal de EDA según Van der Aalst (2016) o Dumas et al. (2018); diferencia entre arquitectura síncrona y event-driven |
| Usabilidad del Sistema | Marco teórico de usabilidad (Nielsen's Heuristics o ISO 9241-11) aplicado al contexto de herramientas de automatización |
| Infraestructura Linux | Fundamentos de containerización (OCI containers, namespaces, cgroups) para justificar Docker técnicamente |
| KPIs y ROI | Definición académica de ROI en proyectos TI (Keen, 1991; Ward & Daniel, 2012) como marco para el cálculo |

## 4.2 Partes que necesitan tablas

| Ubicación | Tabla recomendada |
|---|---|
| Sección 3.2 (EDA) | Tabla de capas arquitectónicas: Capa / Componente / Tecnología / Función |
| Sección 3.3 (Infraestructura) | Tabla de servicios Docker: Servicio / Imagen / Puerto / Función en el onboarding |
| Sección 3.3 (Infraestructura) | Tabla de requisitos por escenario: Piloto / Producción Media / Enterprise |
| Sección 3.5 (KPIs) | Tabla comparativa manual vs automatizado |
| Sección 3.5 (KPIs) | Tabla consolidada de KPIs con fórmulas y targets |
| Sección 3.7 (Cronograma) | Tabla de fases: Semana / Actividades / Entregable |
| Sección 4.2 (Discusión) | Tabla comparativa n8n vs Zapier vs Make |
| Sección 4.2 (Discusión) | Tabla de escenarios de costo mensual |

## 4.3 Partes que necesitan diagramas

| Ubicación | Diagrama recomendado |
|---|---|
| Sección 3.2 (EDA) | Diagrama de flujo EDA: Productor → Event Bus (n8n) → Consumidores (Mailcow, Mattermost, Nextcloud, Plane.so, GitLab) |
| Sección 3.3 (Infraestructura) | Diagrama de servidor único con contenedores Docker y redes internas |
| Sección 3.6 (Workflows) | Diagrama de secuencia WF1→WF2→WF3→WF4→WF5 con webhooks de encadenamiento |

## 4.4 Partes que necesitan gráficos

| Ubicación | Gráfico recomendado |
|---|---|
| Sección 3.5 (KPIs) | Gráfico de barras: Tiempo de onboarding manual vs automatizado |
| Sección 3.5 (KPIs) | Gráfico de reducción de carga RRHH (h/semana antes y después) |
| Sección 4.2 (Discusión) | Gráfico de escalabilidad: costo vs número de workflows activos |
| Sección 4.2 (Discusión) | Gráfico comparativo de costo mensual n8n vs Zapier vs Make a distintos volúmenes |

## 4.5 Referencias académicas adicionales recomendadas

Las siguientes referencias fortalecerían la base teórica de las nuevas secciones:

- **Van der Aalst, W.M.P. (2016). Process Mining: Data Science in Action (2nd ed.). Springer.** → Para fundamentar EDA y BPM.
- **Dumas, M. et al. (2018). Fundamentals of Business Process Management (2nd ed.). Springer.** → Para arquitectura de procesos.
- **Docker Inc. (2024). Docker Compose v2 Documentation.** → Para justificar containerización.
- **Debian Project. (2023). Debian GNU/Linux 12 (Bookworm) Release Notes.** → Para justificar Debian 12.
- **ISO/IEC 27001:2022.** → Para justificar el hardening de seguridad.
- **BambooHR. (2023). The Definitive Guide to Onboarding.** → Para el dato de rotación temprana.

---

# 5. Recomendaciones para las Diapositivas

El PPT actual cubre correctamente la Introducción, Problemática, Solución, los cinco Workflows y la Conclusión. Las siguientes diapositivas deben agregarse o refactorizarse:

## 5.1 Diapositivas a agregar

### Diapositiva nueva: Stack Tecnológico (MARIELA)
- **Contenido:** Diagrama visual del servidor único con contenedores Docker.
- **Formato sugerido:** Ícono del servidor → dentro del servidor, tarjetas por contenedor (n8n, PostgreSQL, Nginx, Mailcow, Mattermost, Nextcloud, GitLab, Plane.so, Telegram Bot).
- **Texto complementario:** Tabla de dos columnas: Herramienta / Función específica en el onboarding.
- **Dónde insertarla:** Después de la diapositiva de Solución, antes de Implementación.

### Diapositiva nueva: Arquitectura EDA (DAYAN)
- **Contenido:** Diagrama del patrón Event-Driven Architecture aplicado al proyecto.
- **Formato sugerido:** Tres bloques horizontales: [Fuentes de Eventos] → [n8n como Event Bus] → [Sistemas Destino]. Dentro de cada bloque, los componentes específicos del stack.
- **Texto complementario:** Destacar los tres roles de n8n: Bus de eventos / Orquestador / Middleware.
- **Dónde insertarla:** Antes de las diapositivas de workflows.

### Diapositiva nueva: Análisis de Costos y Escalabilidad (IKER)
- **Contenido:** Tabla comparativa de escenarios (Piloto / Producción / Enterprise) y comparativa n8n vs Zapier vs Make.
- **Formato sugerido:** Tabla centrada con iconografía de precios. Subtítulo: "Control total de datos. Licencia $0. Sin vendor lock-in."
- **Dónde insertarla:** Dentro de la sección de Discusión.

### Diapositiva nueva: KPIs y ROI (CRISTHIAN)
- **Contenido:** Métricas visuales de impacto.
- **Formato sugerido:** Cuatro tarjetas grandes con íconos: (1) -70% tiempo de onboarding, (2) <1% tasa de error, (3) -80% carga RRHH, (4) ROI >400% primer año.
- **Gráfico adicional:** Barra comparativa tiempo manual (3–7 días) vs automatizado (<4 horas).
- **Dónde insertarla:** Después de la última diapositiva de workflows, antes de Discusión.

### Diapositiva nueva: Cronograma de Implementación (GABRIEL)
- **Contenido:** Roadmap visual de 4.5 semanas.
- **Formato sugerido:** Línea de tiempo horizontal con 5 hitos marcados. Cada hito con nombre, semana y 2–3 actividades clave.
- **Dónde insertarla:** Al final de la sección de Implementación, después de WF5.

## 5.2 Diapositivas a modificar

### Diapositiva de Discusión (actual)
- Reemplazar el gráfico de barras genérico actual (que muestra "7 / 5 / 80 / 35" sin unidades claras) por gráficos con valores explícitos, etiquetas de unidades (días, horas, USD, %) y leyenda completa.
- Agregar la comparativa de costos como segunda visualización en la misma diapositiva o en una adicional.

### Diapositiva de Conclusión (actual)
- Añadir un cuarto bloque a los tres actuales: **"ESCALABILIDAD SIN FRICCIÓN"** → de piloto (USD 15/mes) a producción enterprise (USD 200/mes) sin cambiar el código, solo el hardware.

---

# 6. Recomendaciones Finales de Cohesión

## 6.1 Cómo evitar redundancia

La principal fuente de redundancia actual es la **sección de Análisis**, donde cada fuente se analiza de forma aislada repitiendo el mismo argumento de fondo (n8n es eficiente, reduce carga, tiene ROI positivo) en once variaciones. La solución es:

1. **Condensar el Análisis en 4 párrafos temáticos** que agrupen las fuentes por lo que aportan: (a) evidencia sobre el problema del onboarding manual, (b) validación técnica de n8n, (c) arquitecturas de automatización y (d) casos de implementación reales.
2. **Las citas individuales** se distribuyen dentro de estos párrafos temáticos como referencias de apoyo, no como protagonistas de cada párrafo.
3. **Los KPIs** deben aparecer una sola vez, en la subsección 3.5, y ser referenciados (no repetidos) en la Discusión y la Conclusión.

## 6.2 Cómo mantener coherencia

- El hilo conductor de los **tres ejes** (utilidad / usabilidad / arquitectura) debe declararse en la Introducción (ya está) y reaparecer en la Conclusión cerrando cada eje con una afirmación.
- Las **nuevas secciones técnicas** (3.2 EDA, 3.3 Infraestructura, 3.5 KPIs, 3.7 Cronograma) deben conectar con los ejes existentes mediante frases de transición al inicio de cada una. Ejemplo: "La utilidad descrita en la sección anterior solo es posible sobre una infraestructura técnica que garantice disponibilidad, seguridad y escalabilidad. Esta sección detalla esa infraestructura."
- Las **tecnologías nuevas** (Debian 12, Mailcow, Mattermost, Nextcloud, GitLab, Plane.so) deben aparecer primero justificadas en la sección 3.3, y luego referenciadas por nombre en los workflows sin volver a explicarlas.

## 6.3 Cómo distribuir correctamente teoría y práctica

| Sección | Proporción sugerida |
|---|---|
| Introducción | 100% argumental — ningún detalle técnico |
| Análisis (2.x) | 80% teórico-empírico, 20% referencia al proyecto |
| Desarrollo 3.1 / 3.4 (Utilidad / Usabilidad) | 40% teórico, 60% aplicado al proyecto |
| Desarrollo 3.2 (EDA) | 60% teórico, 40% aplicado |
| Desarrollo 3.3 (Infraestructura) | 30% teórico, 70% técnico-aplicado |
| Desarrollo 3.5 (KPIs) | 20% teórico, 80% datos y métricas |
| Desarrollo 3.6 (Workflows) | 10% teórico, 90% técnico-aplicado |
| Desarrollo 3.7 (Cronograma) | 20% metodológico, 80% operativo |
| Discusión | 70% síntesis con evidencia, 30% reflexión crítica |
| Conclusión | 100% argumental — ningún detalle técnico nuevo |

## 6.4 Cómo hacer que el ensayo parezca una investigación integrada

El riesgo con un ensayo de cinco colaboradores es que cada sección parezca escrita por una persona distinta. Para mitigarlo:

1. **Mantener el estilo de redacción actual** del ensayo base como referencia. El ensayo existente tiene un tono académico consistente: afirmación → evidencia → implicación. Todas las secciones nuevas deben seguir este patrón.
2. **Las tablas deben usar el mismo formato** (bordes simples, encabezado en negrita, alineación izquierda) en todo el documento.
3. **Los workflows** deben nombrarse consistentemente: siempre "WF1 — Recepción y Validación", nunca solo "Workflow 1" o "Flujo 1".
4. **Las tecnologías** deben escribirse consistentemente: "Mailcow" (no "MailCow"), "Mattermost" (no "mattermost"), "Plane.so" (no "Plane"), "PostgreSQL 15" (no "Postgres").
5. **El cronograma y los KPIs** deben referenciar los workflows por nombre, no solo por número, para que las secciones del Gestor de Proyecto y del Analista de KPIs se lean como parte del mismo argumento que las secciones de arquitectura.
6. **La Conclusión** debe sintetizar los aportes de todas las secciones nuevas sin nombrarlas por responsable: el lector no debe saber que el texto fue escrito por cinco personas distintas.

---

## Nota sobre la coherencia del stack tecnológico

La revisión técnica de los documentos detecta una inconsistencia importante entre el **PDF técnico de referencia** (que usa Ubuntu Server 22.04 LTS, Slack, Google Drive, Jira, GitHub) y el **ensayo y PPT actuales** (que ya usan Debian 12, Mattermost, Nextcloud, GitLab, Plane.so). El ensayo y el PPT tienen la arquitectura correcta y actualizada. El PDF técnico es una referencia anterior que **no debe copiarse literalmente**; solo sus secciones de EDA, KPIs, SLA y hardening son reutilizables como base teórica, adaptando las tecnologías al stack real del proyecto.

Las siguientes referencias del PDF técnico deben **ignorarse o adaptarse** en el ensayo:
- Ubuntu Server 22.04 → usar Debian 12.
- Google Workspace / Gmail → usar Mailcow.
- Slack → usar Mattermost.
- Google Drive → usar Nextcloud.
- Jira → usar Plane.so.
- GitHub → usar GitLab (solo para perfiles técnicos).
- Google Sheets → usar PostgreSQL 15 como persistencia central.

Las referencias del PDF técnico que **sí son reutilizables** como base teórica:
- Tablas de KPIs (sección 5.5 del PDF) → adaptadas al stack actual.
- Tabla de SLAs por tipo de tarea (sección del WF4) → directamente usable.
- Descripción de EDA y capas arquitectónicas (sección 4.3.1) → adaptable.
- Configuración de Nginx, UFW, Fail2ban, script de backup → directamente usable (ya es el mismo stack).
- Estructura de directorios `/opt/n8n/` → directamente usable.

---

*Documento generado para uso editorial interno del equipo — Universidad Privada de Tacna — Ingeniería de Sistemas — 2026*
