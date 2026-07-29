# Visor de Incendios Forestales en España

Aplicación WebGIS para la visualización, filtrado espacial y consulta en tiempo real de anomalías térmicas detectadas por satélite en territorio español. La herramienta consume datos directos de la NASA y clasifica espacial y temporalmente los focos detectados en los últimos 3 días.

🌍 **Demo en directo:** [https://andresgarcia2002.github.io/visor_espana_incendios/](https://andresgarcia2002.github.io/visor_espana_incendios/)

## Funcionalidades y Lógica Espacial

- **Consumo de APIs de Teledetección:** Conexión directa con la API de NASA FIRMS para la extracción de anomalías térmicas captadas por el sensor VIIRS (satélite Suomi NPP).
- **Filtrado Geográfico en Cliente:** Algoritmo de *ray-casting* (JavaScript) para delimitar las geometrías al ámbito nacional (Península Ibérica, Baleares, Canarias, Ceuta y Melilla), descartando automáticamente detecciones fuera de fronteras.
- **Simbología y Clasificación Temporal:** Renderizado cromático diferencial según la antigüedad del registro (0–6 h, 6–24 h y 24–72 h) para la evaluación de la dinámica espacio-temporal del fuego.
- **Actualización Dinámica:** Mecanismo de recarga manual mediante botón interactivo y ciclo de consulta automatizado cada 15 minutos, con indicador visual de la hora exacta del último registro cargado.
- **Interoperabilidad de Capas Base:** Integración de capas cartográficas de OpenStreetMap y servicios de mapas de teselas (WMTS) del Instituto Geográfico Nacional (IGN).
- **Inspección de Atributos:** Ventanas emergentes (*popups*) con datos de potencia radiativa del fuego (FRP en MW), nivel de confianza y hora UTC de paso del satélite.

## Arquitectura y Tecnologías

- **Lenguajes:** HTML5, CSS3, JavaScript (Vanilla ES6+).
- **Mapeo Web:** Leaflet.js v1.9.4.
- **Procesamiento de Datos:** PapaParse (parseo asíncrono de feeds CSV).
- **Fuentes de Datos:** NASA FIRMS API / Instituto Geográfico Nacional (IGN).

## Autor

**Andrés García Séllez**  
Geógrafo | Técnico GIS
