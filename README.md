# Training Operations Automation

Plataforma de automatización para altas formativas, validación de datos y workflows operativos.

Proyecto desarrollado para reducir carga administrativa, minimizar errores manuales y centralizar el proceso completo de gestión de alumnos y cursos mediante automatización controlada y supervisión humana.

<p align="center">
  <img src="./docs/hero-dashboard.png" width="100%" alt="Dashboard Training Operations Automation"/>
</p>

> El código fuente y los workflows internos se mantienen privados por motivos de seguridad, explotación comercial y confidencialidad del cliente.  
> Este repositorio actúa como showcase técnico y visual del sistema.

<br>

🌐 **Portfolio:** https://portfolio-adrisanchez.vercel.app  
📧 **Contacto:** adri.ia.dev@gmail.com

---

# El problema

La gestión manual de altas formativas generaba:
- revisión constante de Excels
- detección manual de errores
- múltiples correos para pedir correcciones
- generación repetitiva de CSVs
- pérdida de trazabilidad
- errores operativos frecuentes

Campos inválidos como:
- DNIs incorrectos
- emails mal formados
- datos obligatorios vacíos
- estructuras incompatibles

obligaban a revisar manualmente cada archivo antes de poder subir alumnos a la plataforma externa.

---

# La solución

Un sistema híbrido entre automatización y validación humana diseñado para eliminar tareas repetitivas sin perder control operativo.

La plataforma:
- procesa automáticamente emails entrantes
- detecta y almacena archivos Excel
- valida estructura y datos
- muestra errores exactos en un dashboard centralizado
- genera CSVs compatibles con la plataforma externa
- automatiza emails de bienvenida
- registra trazabilidad completa del flujo

El objetivo no era automatizar a ciegas, sino reducir fricción operativa manteniendo supervisión en los puntos críticos del proceso.

---

# Flujo operativo

<p align="center">
  <img src="./docs/workflow-diagram.png" width="100%" alt="Workflow automatización cursos"/>
</p>

```txt
Email con Excel
        ↓
Extracción automática del adjunto
        ↓
Validación de datos y estructura
        ↓
Creación de ticket operativo
        ↓
Corrección manual si existen errores
        ↓
Generación automática de CSV
        ↓
Subida manual a plataforma externa
        ↓
Confirmación de alta realizada
        ↓
Envío automatizado de emails
        ↓
Logs, errores y reenvíos
```

---

# Funcionalidades principales

- Procesamiento automático de emails
- Extracción y almacenamiento de XLSX originales
- Validación automática de datos
- Detección precisa de errores por fila y campo
- Dashboard operativo con tickets y estados
- Generación automática de CSVs compatibles
- Confirmación manual de altas realizadas
- Automatización de emails de bienvenida
- Logs detallados por destinatario
- Gestión de errores SMTP y reenvíos
- Trazabilidad completa del flujo operativo

---

# Dashboard operativo

<p align="center">
  <img src="./docs/hero-dashboard.png" width="100%" alt="Dashboard operativo"/>
</p>

El panel centraliza:
- tickets pendientes
- errores de validación
- estados operativos
- CSVs generados
- trazabilidad de emails
- incidencias de envío

---

# Validación y control de errores

<p align="center">
  <img src="./docs/validation-errors.png" width="100%" alt="Errores de validación"/>
</p>

El sistema identifica automáticamente:
- campos obligatorios faltantes
- DNIs inválidos
- emails incorrectos
- errores de formato
- inconsistencias estructurales

Esto evita revisar manualmente cada Excel y permite detectar problemas antes de generar el CSV final.

---

# Vista de ticket

<p align="center">
  <img src="./docs/ticket-detail.png" width="100%" alt="Detalle ticket"/>
</p>

Cada ticket conserva:
- XLSX original
- estado del flujo
- errores encontrados
- CSV generado
- historial operativo
- acciones realizadas

---

# Emails y trazabilidad

<p align="center">
  <img src="./docs/email-logs.png" width="100%" alt="Logs email"/>
</p>

El sistema registra:
- emails enviados
- errores SMTP
- destinatarios fallidos
- reenvíos manuales
- historial completo de comunicaciones

---

# Stack tecnológico

| Capa | Tecnología |
|---|---|
| Automatización | n8n |
| Backend | FastAPI · Python |
| Frontend | React · Next.js |
| Base de datos | PostgreSQL · Supabase |
| Emails | SMTP · Automatización transaccional |
| Infraestructura | Docker · Vercel · Cloud Run |

---

# Decisiones técnicas

### Automatización con supervisión humana

El sistema automatiza tareas repetitivas, pero mantiene control manual en puntos críticos para evitar errores masivos y asegurar calidad operativa.

---

### Validación antes de generar CSV

El CSV solo se genera cuando todos los datos son válidos, evitando rechazos posteriores en la plataforma externa.

---

### Trazabilidad completa

Cada acción queda registrada:
- archivos originales
- estados
- emails
- errores
- reenvíos
- confirmaciones

---

### Separación entre validación y alta final

Los datos finales del curso se completan únicamente después de confirmar que la subida a la plataforma externa se ha realizado correctamente.

---

# Estado actual

- Sistema operativo en entorno real
- Automatizaciones activas
- Flujo completo en producción
- Evolución y mantenimiento continuos

---

# Contacto

¿Necesitas automatizar procesos administrativos o flujos operativos similares?

📧 **adri.ia.dev@gmail.com**  
🌐 **Portfolio:** https://portfolio-adrisanchez.vercel.app  
💼 **LinkedIn:** https://www.linkedin.com/in/adrian-sanchez-guerrero