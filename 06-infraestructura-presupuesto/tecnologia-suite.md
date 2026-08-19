# Tecnología del departamento

Ventaja diferencial: plataformas propias ya construidas y en uso.
El colegio que llega con tecnología dedicada al área deportiva se diferencia de inmediato.

## Plataforma 1: SCM - Gestión del área

### Qué hace
Sistema centralizado para administrar toda la operación del departamento de deportes:
- Registro de alumnos por curso, nivel y disciplina.
- Gestión de selecciones: nóminas, convocatorias, historial de participación.
- Asistencia a clases curriculares y extraprogramáticas.
- Comunicaciones directas con apoderados (avisos, citaciones, resultados).
- Evaluaciones del perfil atlético con seguimiento longitudinal curso a curso.
- Reportes automáticos para rectoría: participación, cobertura, tendencias.

### Qué problema resuelve
Sin SCM, la información vive en planillas sueltas, cuadernos y memorias individuales. Cuando un profesor se va, se va con los datos. SCM centraliza todo en un lugar accesible para el equipo, con historial que no se pierde.

## Plataforma 2: CoachDrill - Planificación de entrenamientos

### Qué hace
Herramienta para que cada docente y entrenador planifique sus sesiones de manera estandarizada:
- Biblioteca de ejercicios por deporte, objetivo y grupo etario.
- Plantillas de sesión con estructura definida (calentamiento, parte principal, vuelta a la calma).
- Visualización del plan semanal y mensual del equipo completo.
- El coordinador puede revisar la planificación de todo el equipo desde un solo lugar.

### Qué problema resuelve
Cada profesor planifica como quiere o no planifica. No hay visibilidad de qué se enseña, no hay progresión documentada y no se puede evaluar la calidad de las sesiones. CoachDrill hace visible lo invisible.

## Plataforma 3: AutoCut - Análisis de video

### Qué hace
Sistema de registro y análisis de video enfocado en selecciones:
- Grabación de partidos y entrenamientos clave.
- Corte automático o asistido de jugadas relevantes.
- Etiquetado por situación de juego (ataque, defensa, transición, pelota parada).
- Clips compartibles con deportistas para retroalimentación individual.
- Archivo histórico de partidos por temporada.

### Qué problema resuelve
El análisis de video es estándar en el deporte de rendimiento, pero casi ningún colegio lo hace. AutoCut permite dar retroalimentación objetiva, preparar rivales y documentar el progreso de cada selección a lo largo de la temporada.

## Comparación con alternativas comerciales

| Criterio | Plataformas propias | Soluciones comerciales (Hudl, Teamsnap, etc.) |
|----------|--------------------|-------------------------------------------------|
| Costo anual | Marginal (hosting + mantenimiento) | USD 500-5.000 por plataforma |
| Personalización | Total, adaptada al modelo del colegio | Limitada a lo que ofrece el proveedor |
| Integración entre módulos | Nativa (SCM + CoachDrill + AutoCut comparten datos) | Requiere integraciones manuales o no existe |
| Datos | Propiedad del colegio, alojados donde se decida | En servidores del proveedor, con sus términos |
| Soporte | Depende del desarrollador (riesgo si es una sola persona) | Soporte del proveedor, pero genérico |

**Por qué lo propio es mejor en este caso**: el modelo del departamento tiene lógica específica (niveles Formación-Desarrollo-Élite, perfil atlético longitudinal, vínculo clase-selección) que ninguna plataforma comercial resuelve sin personalización costosa.

**Riesgo de lo propio**: dependencia del desarrollador. Mitigación: documentar el código, usar tecnologías estándar, tener plan de contingencia si el desarrollador no está disponible.

## Arquitectura de datos

- SCM es el sistema maestro: contiene el registro de alumnos, cursos y selecciones.
- CoachDrill consulta las nóminas de SCM para asociar planificaciones a grupos reales.
- AutoCut etiqueta videos con datos de SCM (nombre del deportista, selección, temporada).
- Los tres sistemas alimentan un panel de indicadores para el coordinador y para rectoría.
- Exportación de datos en formatos estándar (CSV, PDF) para respaldo y reportes ad hoc.

## Hosting y seguridad

- Hosting en servidor dedicado o cloud (definir con el colegio según política de TI).
- Certificado SSL para todas las plataformas (acceso solo por HTTPS).
- Respaldos automáticos diarios con retención de al menos 30 días.
- Acceso por usuario y contraseña; roles diferenciados (coordinador, docente, apoderado en modo consulta).
- Cumplimiento de Ley 21.719: ver carpeta 09-administracion-normativa para detalle de protección de datos.

## Integración con sistemas del colegio

- Evaluar si el sistema de notas o matrícula del colegio tiene API o exportación que permita sincronizar listas de alumnos con SCM (evitar doble digitación).
- Si el colegio usa plataforma de comunicación (Schoolnet, Educamos, etc.), definir si las comunicaciones deportivas salen por ahí o por SCM.
- En cualquier caso, SCM es la fuente de verdad para datos deportivos; el sistema del colegio lo es para datos académicos.

## Estructura de costos

| Ítem | Costo estimado anual |
|------|---------------------|
| Hosting (cloud básico) | $200.000 - $500.000 |
| Dominio y certificado SSL | $30.000 - $50.000 |
| Mantenimiento y actualizaciones (horas de desarrollo) | $500.000 - $1.500.000 |
| Equipamiento de video (cámara, trípode, almacenamiento) | $500.000 - $1.000.000 (inversión inicial) |
| **Total operativo anual (sin inversión inicial)** | **$730.000 - $2.050.000** |

Comparar con el costo de una sola plataforma comercial equivalente para dimensionar el ahorro.

## Plan de implementación

### Fase 1 - Piloto (meses 1-3)
- Cargar una selección y un nivel de EF en SCM. Un entrenador usa CoachDrill un mes completo. Dos partidos con AutoCut. Feedback y ajuste.

### Fase 2 - Expansión (meses 4-6)
- Todas las selecciones y niveles curriculares en SCM. Todo el equipo en CoachDrill. AutoCut en partidos de local.

### Fase 3 - Consolidación (meses 7-12)
- Primer reporte anual desde las plataformas. Perfil atlético con datos longitudinales. Ajustes basados en uso real.

## Plan de capacitación

- Sesión inicial de 2 horas por plataforma para todo el equipo (presencial, con práctica).
- Manual breve por plataforma (máximo 5 páginas con capturas de pantalla).
- Revisión de uso real a los 3 meses: quién lo usa, quién no, y qué ajustar.
