
# Análisis de Métricas de YouTube con Python y la API de YouTube

## Descripción del Proyecto
Este proyecto permite analizar las métricas de un canal de YouTube utilizando la **API de YouTube Data v3**. En particular, extrae y analiza:
- **Videos publicados en un mes específico**.
- **Vistas de cada video publicado en ese mes**.
- **Total de vistas generadas por videos nuevos en el mes analizado**.

El objetivo es obtener insights sobre el rendimiento de los videos recientemente publicados sin incluir el impacto de videos anteriores.

## Requisitos Previos
Antes de ejecutar el proyecto, asegúrate de tener instalado:
- **Python 3.7 o superior**
- **Librerías necesarias:** `requests`, `pandas`

Puedes instalarlas con:
```sh
pip install requests pandas
```

## Obtención de la API Key de YouTube
Para acceder a los datos del canal, es necesario obtener una clave de API de YouTube. Sigue estos pasos:

1. Ve a [Google Cloud Console](https://console.cloud.google.com/).
2. Crea un nuevo proyecto o selecciona uno existente.
3. En la barra de búsqueda, busca y selecciona **YouTube Data API v3**.
4. Haz clic en "Habilitar".
5. Ve a la sección **Credenciales** y selecciona "Crear credenciales" → "Clave de API".
6. Copia la API Key generada y guárdala de manera segura.

## Uso del Proyecto
### 1. Configurar la API Key y el Canal
En el archivo principal, reemplaza `API_KEY` con tu clave de API y `CHANNEL_ID` con el ID del canal que deseas analizar.

```python
API_KEY = "TU_API_KEY_AQUI"
CHANNEL_ID = "ID_DEL_CANAL"
```

Para encontrar el `CHANNEL_ID`, puedes utilizar esta URL, reemplazando "NOMBRE_DEL_CANAL":
```sh
https://www.googleapis.com/youtube/v3/search?part=snippet&type=channel&q=NOMBRE_DEL_CANAL&key=TU_API_KEY_AQUI
```

Ejecuta la URL en el navegador y busca `"id":{"channelId":"..."}`.

### 2. Ejecutar el Análisis
Ejecuta el script principal para obtener los videos publicados en el mes y calcular sus vistas.

### 3. Resultados Esperados
El script mostrará una tabla con los videos publicados en el mes seleccionado y sus respectivas vistas, junto con el total de vistas generadas en ese periodo.

## Posibles Mejoras
- Agregar análisis de engagement (likes, comentarios, etc.).
- Visualizar los datos con `matplotlib` o `seaborn`.
- Automatizar la extracción de datos mes a mes.

---


