# Ecosistema de Flujos de Trabajo Automatizados con n8n

Este repositorio contiene un conjunto de automatizaciones diseñadas para mitigar el "caos digital" y optimizar la gestión del tiempo mediante la integración de inteligencia artificial y orquestación de APIs. El ecosistema está construido sobre **n8n** (alojado localmente) e integra los modelos de lenguaje de **Google Gemini** para la comprensión semántica y el triaje de información.

## Funcionalidades Principales (Workflows)

1. **Bot de Resumen Matutino (Discord):** Extrae noticias e información diaria, la unifica en formato Markdown y autogestiona el canal eliminando mensajes obsoletos.
2. **Sistema Inteligente de Triaje (Gmail + Telegram + Sheets):** Monitoriza la bandeja de entrada, utiliza Gemini IA para resumir, puntuar y clasificar correos, guarda un registro en Google Sheets, responde automáticamente y agenda eventos en Calendar.
3. **Alertas de Precio (Web Scraping + Discord):** Rastrea precios de hardware (memoria RAM) en la web y notifica automáticamente si caen por debajo del precio objetivo.

---

## Requisitos Previos

Dado que el sistema prioriza la privacidad de los datos (self-hosting), necesitarás ejecutar el orquestador en tu propio entorno local o servidor privado.

### Infraestructura
* **Docker** con el paquete n8n instalado en tu máquina o servidor local.

### Cuentas y Credenciales de APIs
Para que los nodos de n8n puedan comunicarse con los servicios externos, deberás generar las siguientes credenciales:
* **Google Cloud Console:** Credenciales OAuth2 (para Gmail API, Google Sheets API y Google Calendar API).
* **Google AI Studio:** API Key de Gemini.
* **Discord Developer Portal:** Token de Bot de Discord y permisos de lectura/escritura en canales.
* **Telegram:** Token de Bot generado a través de *BotFather*.
