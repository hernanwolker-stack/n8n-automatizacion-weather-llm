# Automatización de Alertas Climáticas con n8n y LLMs 🌦️🤖

Este proyecto consiste en un ecosistema de automatización que integra datos meteorológicos en tiempo real con modelos de lenguaje de gran escala (LLMs) para generar reportes inteligentes y alertas personalizadas.

## 🚀 Funcionalidades
- **Extracción de Datos:** Conexión automática con APIs de clima.
- **Análisis Inteligente:** Uso de LLMs para categorizar riesgos y redactar mensajes naturales.
- **Clasificación Lógica:** Diferenciación de flujos de trabajo según el estado del tiempo (Ramas IF).
- **Notificaciones:** Envío de alertas procesadas a través de Telegram.

## 🛠️ Tecnologías Utilizadas
* **n8n:** Orquestador de flujos de trabajo.
* **LLMs (Groq):** Procesamiento de lenguaje natural.
* **Open-Meteo API:** Fuente de datos climáticos.
* **Telegram Bot API:** Canal de salida para las alertas.

## 📁 Estructura del Proyecto
* `/workflows`: Contiene el archivo `.json` para importar en n8n.
* `/docs`: Documentación detallada y especificaciones técnicas.
* `/images`: Capturas del flujo de trabajo y resultados.

## 📸 Visualización del Flujo

### Rama: Clima Normal
![Clima Normal](Rama-False-Clima-Normal.png) 
*(Sustituye por el nombre exacto de tu archivo de imagen)*

### Rama: Alerta por Lluvia
![Alerta Clima](Rama-true-Alerta-clima.png)
*(Sustituye por el nombre exacto de tu archivo de imagen)*

## ⚙️ Instalación
1. Descarga el archivo `Proyecto Final — Automatización con n8n y LLMs.json`.
2. En tu instancia de n8n, haz clic en **Import from File**.
3. Configura tus credenciales para la API de clima y el nodo del LLM.
4. ¡Ejecuta el workflow!
