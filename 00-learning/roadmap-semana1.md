# Semana 1: Fundamentos de n8n

## Día 1: Setup y Conceptos

### Instalación n8n (Opción A: Cloud Gratis)
1. Crear cuenta en [n8n.io](https://n8n.io) (tier gratis: 100 executions/mes)
2. Explorar UI: Canvas, Node Panel, Executions

### Instalación n8n (Opción B: Self-hosted en Render)
1. Crear cuenta en [Render.com](https://render.com) (gratis 1er año)
2. Deploy n8n usando Blueprint oficial
3. Configurar variables de entorno básicas

## Día 2: Primer Workflow - HTTP Trigger

**Objetivo:** Crear endpoint que reciba datos y responda.

```
HTTP Trigger → Code Node (transform) → HTTP Response
```

**Práctica:**
- Crear webhook endpoint `/test`
- Enviar POST con JSON desde Postman/curl
- Retornar mismo JSON modificado

## Día 3: Integraciones Básicas - Google Sheets

**Setup:**
1. Crear proyecto en Google Cloud Console
2. Habilitar Google Sheets API
3. Descargar credentials JSON
4. Conectar a n8n (OAuth2)

**Workflow:**
```
HTTP Trigger → Google Sheets (Append) → Slack Message
```

**Práctica:** Formulario de contacto que guarda en Sheets y notifica.

## Día 4: Email Automation - Gmail

**Workflow:**
```
Gmail Trigger (nuevo email) → Filter (asunto específico) 
→ Google Sheets (log) → Telegram Notification
```

**Casos de uso:**
- Alertas de leads entrantes
- Auto-responder FAQs
- Escalación a humano

## Día 5: Scheduling y Cron Jobs

**Workflows tipo:**
- Reporte diario: Sheets → Resumen → Email a CEO
- Limpieza de datos: Borrar registros antiguos >30 días
- Backup automático: Notion → Google Drive

## Recursos de Apoyo

- [Documentación n8n](https://docs.n8n.io)
- [YouTube: n8n Tutorials](https://youtube.com/n8n-io)
- [Community Forum](https://community.n8n.io)
- **Plantillas de workflows:** workflow.n8n.io

## Checkpoint Semana 1

Debes poder:
- [ ] Explicar qué es un Trigger vs un Node
- [ ] Conectar al menos 3 servicios (Sheets, Gmail, Telegram)
- [ ] Crear un workflow que combine Trigger + Acción + Notificación
- [ ] Debuggear errores básicos (ver Execution log)

**¿Listo para Semana 2?**
