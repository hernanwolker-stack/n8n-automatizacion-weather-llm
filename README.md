# Automatización de Alertas Climáticas con n8n y LLMs 🌦️🤖

## 📌 Descripción

Este proyecto implementa un workflow automático en n8n que permite
consultar el clima de cualquier ciudad mediante un bot de Telegram.

El sistema utiliza APIs externas para obtener datos climáticos y modelos
de lenguaje (LLMs) para analizar y generar respuestas dinámicas.

------------------------------------------------------------------------

## ⚙️ Tecnologías utilizadas

-   n8n (automatización de workflows)
-   Telegram Bot API
-   API Open-Meteo (datos climáticos)
-   API Nominatim (geocoding)
-   Groq (LLMs - Llama3)

------------------------------------------------------------------------

## 🚀 Funcionamiento

1.  El usuario envía una ciudad al bot de Telegram
2.  El sistema obtiene las coordenadas (lat/lon)
3.  Se consultan los datos climáticos
4.  Se limpian y estructuran los datos
5.  LLM 1 clasifica el clima (NORMAL / LLUVIA / TORMENTA)
6.  Un nodo IF decide la rama a seguir
7.  LLM 2 genera una alerta si corresponde
8.  Se envía la respuesta por Telegram
9.  Se registran logs de la ejecución

------------------------------------------------------------------------

## 🧠 Modelos LLM

### LLM 1 --- Clasificación

-   Rol: Clasificar el clima
-   Salida: NORMAL / LLUVIA / TORMENTA
-   Tipo: Respuesta estructurada

### LLM 2 --- Generación

-   Rol: Generar alertas y explicaciones
-   Salida: Texto amigable con recomendaciones

------------------------------------------------------------------------

## 🔀 Lógica condicional

El flujo utiliza un nodo IF que evalúa:

-   Probabilidad de lluvia \> 60%
-   Lluvia acumulada \> 10 mm
-   Humedad \> 80%

Si alguna condición se cumple → ALERTA\
Caso contrario → NORMAL

------------------------------------------------------------------------

## 📩 Notificación

Se utiliza Telegram para enviar mensajes al usuario con:

-   Datos del clima
-   Recomendaciones
-   Alertas (si corresponde)

------------------------------------------------------------------------

## 🛠 Logs

Se implementaron logs mediante nodos Code que registran:

-   Tipo de clima
-   Ciudad
-   Timestamp
-   Mensaje generado

Esto permite trazabilidad y debugging del sistema.

------------------------------------------------------------------------

## ▶️ Cómo ejecutar

1.  Importar el archivo workflow.json en n8n
2.  Configurar credenciales de:
    -   Telegram
    -   Groq
3.  Publicar el workflow
4.  Enviar una ciudad al bot de Telegram

------------------------------------------------------------------------

## 🧪 Pruebas

Se probaron múltiples ciudades con distintos escenarios:

-   Clima normal
-   Lluvias leves
-   Tormentas intensas

El sistema respondió correctamente en todos los casos.

------------------------------------------------------------------------

## 🔒 Seguridad

-   No se incluyen credenciales en los archivos entregados
-   Uso de credenciales de n8n
-   Manejo básico de errores implementado
