# OSINT resources

[Aplicación de Streamlit](https://osint-resources-jmxc5tg6uheukqu86hzwrv.streamlit.app/)

Esta aplicación es una colección de recursos de Inteligencia de Fuentes Abiertas (OSINT), diseñada para ayudar a investigadores, analistas y cualquier persona interesada en recopilar información disponible públicamente. Proporciona una interfaz de búsqueda y filtrado para descubrir diversas herramientas y sitios web categorizados por sus tipos de entrada y funcionalidades.

El proyecto está diseñado para que cada investigador pueda clonar este repositorio y generar su propia "caja de herramientas" OSINT personalizada. Simplemente modifica el archivo `data/osintToolsData.json` para añadir, eliminar o editar los recursos que mejor se adapten a tus necesidades y flujo de trabajo específicos.

## Características

* **Colección Completa:** Una lista creciente de herramientas y recursos OSINT en diferentes categorías.
* **Categorización:** Los recursos están categorizados para facilitar la navegación (p. ej., análisis de redes sociales, inteligencia de dominios, análisis de imágenes).
* **Filtrado por Tipo de Entrada:** Filtra fácilmente los recursos según el tipo de entrada que aceptan (p. ej., nombre, NIF, dominio, dirección IP).
* **Información Detallada:** Cada entrada de recurso incluye una descripción, URL, categoría, tipos de entrada admitidos y tipos de salida.
* **Interfaz Fácil de Usar:** Construida con Streamlit para una aplicación web intuitiva y accesible.
* **Lista para Despliegue en Streamlit:** La aplicación está específicamente diseñada para ser desplegada y alojada fácilmente en la plataforma Streamlit, permitiendo un acceso y compartición rápidos a través de un navegador web.

## Cómo Utilizar

1.  **Explorar la Colección:** La aplicación muestra los recursos OSINT en secciones desplegables, proporcionando un resumen de cada uno.
2.  **Filtrar por Tipo de Entrada:** Utiliza el cuadro de selección múltiple "Filtrar por input" para elegir los tipos de entrada que tienes disponibles. La aplicación filtrará dinámicamente la lista para mostrar solo los recursos que pueden utilizar esa entrada.
3.  **Explorar Detalles:** Haz clic en el título de cada recurso (la sección desplegable) para revelar información más detallada, incluyendo su descripción, URL, categoría y los tipos de entrada y salida específicos que admite.
4.  **Acceder a los Recursos:** Utiliza la URL proporcionada para acceder directamente a la herramienta o sitio web OSINT en tu navegador web.

## Despliegue en Streamlit

Esta aplicación está construida con Streamlit, una librería de Python que facilita la creación de aplicaciones web interactivas para ciencia de datos y aprendizaje automático. Para desplegar esta aplicación en Streamlit Cloud (¡gratis!):

1.  **Regístrate en Streamlit Cloud:** Si no tienes una cuenta, regístrate en [https://streamlit.io/cloud](https://streamlit.io/cloud).
2.  **Prepara tu repositorio:**
    * Asegúrate de que tu código Python (archivo `.py`, p. ej., `osint_resourcesp.py`) esté en tu repositorio de GitHub.
    * Incluye un archivo `requirements.txt` en la raíz de tu repositorio que liste las librerías de Python necesarias (en este caso, al menos `streamlit` y `json`). Puedes generar este archivo ejecutando `pip freeze > requirements.txt` en tu entorno local donde tengas instaladas las dependencias de la aplicación.
    * Asegúrate de que tu archivo de datos JSON (`osintToolsData.json` en el directorio `data/` según el código) también esté presente en tu repositorio.
3.  **Despliega en Streamlit Cloud:**
    * Ve a tu panel de control de Streamlit Cloud.
    * Haz clic en el botón "New app".
    * Selecciona tu repositorio de GitHub, la rama y el archivo Python (`osint_resources.py`) que contiene tu aplicación Streamlit.
    * Especifica cualquier variable de entorno necesaria (si aplica).
    * ¡Haz clic en "Deploy!"!

Streamlit Cloud construirá y desplegará tu aplicación de recursos OSINT, proporcionándote una URL pública que podrás compartir con otros.

## Fuente de Datos

Los datos de los recursos OSINT se almacenan en un archivo JSON (`data/osintToolsData.json`). La estructura de este archivo es la siguiente:

```json
{
    "Nombre del Recurso 1": {
        "descripcion": "...",
        "url": "...",
        "categoria": "...",
        "input_types": ["...", "..."],
        "output_types": ["...", "..."]
    },
    "Nombre del Recurso 2": {
        "descripcion": "...",
        "url": "...",
        "categoria": "...",
        "input_types": ["...", "..."],
        "output_types": ["...", "..."]
    },
    // ... más recursos
}
