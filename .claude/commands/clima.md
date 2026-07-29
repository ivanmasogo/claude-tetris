---
description: Muestra el clima actual de una ciudad
argument-hint: [ciudad]
---

El usuario quiere saber el clima de: $ARGUMENTS

Pasos:
1. Si no se indica ninguna ciudad, pide al usuario que especifique una.
2. Usa WebFetch para consultar `https://wttr.in/<ciudad-url-encoded>?format=j1` (JSON) y obtener los datos actuales del clima. Si la ciudad tiene espacios o tildes, codifícala correctamente para la URL.
3. A partir del JSON, extrae: temperatura actual (°C), sensación térmica, descripción del clima, humedad y velocidad del viento.
4. Responde en español, de forma breve, con un resumen tipo:

   **Clima en <Ciudad>**: <descripción>, <temp>°C (sensación <feels_like>°C), humedad <humedad>%, viento <viento> km/h.

5. Si la petición falla o la ciudad no se encuentra, informa el error claramente sin inventar datos.
