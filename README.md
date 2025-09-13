# Workflows n8n

Este repositorio contiene tres workflows para n8n, cada uno diseñado para automatizar tareas específicas utilizando diferentes servicios y nodos. A continuación se describe cada uno:

## 1. 1-Sheet.json
**Descripción:**
Este workflow crea un formulario de contacto que recopila información de usuarios (nombre, apellido, email, descripción del problema y adjunto). Cuando un usuario envía el formulario, los datos se agregan automáticamente a una hoja de Google Sheets.
- **Nodos principales:**
  - Formulario de contacto (formTrigger)
  - Google Sheets (append row)
- **Uso típico:** Recopilación de solicitudes o problemas de clientes y almacenamiento organizado en una hoja de cálculo.

## 2. 2-ChatBot Telegram.json
**Descripción:**
Este workflow implementa un chatbot en Telegram que recibe mensajes de los usuarios y responde utilizando un modelo de lenguaje de OpenAI (GPT-4o-mini) a través de un agente AI. El flujo es:
- El bot recibe un mensaje en Telegram.
- El mensaje se envía a un agente AI que utiliza el modelo de OpenAI para generar una respuesta.
- El bot responde al usuario en Telegram con la respuesta generada.
- **Nodos principales:**
  - Telegram Trigger
  - AI Agent (Langchain)
  - OpenAI Chat Model
  - Envío de mensaje por Telegram
- **Uso típico:** Automatización de respuestas inteligentes en un canal de Telegram.

## 3. 3-Drive share file.json
**Descripción:**
Este workflow monitoriza una carpeta específica de Google Drive y, cuando se detecta la creación de un nuevo archivo, comparte ese archivo automáticamente con un grupo de emails definidos. Utiliza un bucle para compartir el archivo con varios destinatarios.
- **Nodos principales:**
  - Google Drive Trigger (detecta archivos nuevos)
  - Loop Over Items (para iterar sobre emails)
  - Share file (comparte el archivo)
- **Uso típico:** Automatización del compartido de archivos nuevos en Drive con un grupo de personas.

---

Cada workflow puede ser importado directamente en n8n para su uso y adaptación según las necesidades del usuario.
