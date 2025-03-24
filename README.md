# Evaluador Automatizado de Empresas Según Requerimientos (E3)

## Acceso a la Aplicación Web
[Prueba la aplicación en Streamlit](https://iapromptv-a-zwb2njyedpj9rrsspqtj43.streamlit.app/)

> **🧪 Prueba rápida:** Para verificar todas las funcionalidades nuevas, ingresá la URL de Apple (https://www.apple.com/) en el campo de búsqueda.  
> 
> 🚀 **Nuevos cambios implementados:**  
> - Selector de idioma (Original ↔ Español) para toda la salida.  
> - Indicadores financieros clave extraídos automáticamente (capitalización de mercado, precio actual, variación anual, P/E, EPS, dividend yield, máximos/mínimos de 52 semanas y volumen promedio).  
> - Gráfico interactivo de la evolución del precio de la acción en el último año, con medias móviles de 50 y 200 días, descargable en CSV.  

## Descripción del Proyecto

Evaluador Automatizado de Empresas Según Requerimientos (E3) es una herramienta diseñada para automatizar la investigación y evaluación de empresas según criterios específicos, reduciendo el tiempo de búsqueda manual y proporcionando información estructurada y confiable.

### ¿Cómo Funciona?
1. El usuario ingresa hasta cinco URLs de sitios web de empresas.
2. La aplicación extrae información clave de los sitios web y LinkedIn (si está disponible).
3. Se procesan los datos con GPT-4, generando un resumen estructurado con datos relevantes.
4. La información se muestra en un historial de búsquedas, permitiendo filtrar y descargar la información en CSV.

## Introducción

### Nombre del Proyecto
Evaluador Automatizado de Empresas Según Requerimientos (E3)

### Problema a Resolver
El análisis de empresas para adquisiciones, inversiones o benchmarking suele ser un proceso manual, lento y propenso a errores. Obtener información de múltiples fuentes requiere tiempo y esfuerzo, lo que puede retrasar la toma de decisiones.

### Propuesta de Solución
E3 automatiza la recopilación y análisis de datos, extrayendo información clave de sitios web corporativos y perfiles de LinkedIn. Esto se logra mediante web scraping y el procesamiento avanzado con GPT-4.

## Objetivos del Proyecto
- Extraer información estructurada de sitios web y LinkedIn.
- Optimizar el tiempo de investigación manual.
- Permitir el acceso a un historial de búsquedas, con filtros y descargas.
- Integrar métricas de uso de tokens y costos estimados.

## Metodología y Funcionalidades Implementadas

### Procedimientos Implementados
1. Scraping de contenido de sitios web y LinkedIn.
2. Procesamiento con GPT-4 para estructurar y analizar la información.
3. Historial de Búsquedas con filtrado y ordenamiento por fecha.
4. Cálculo del uso de tokens y estimación de costos de cada análisis.
5. Interfaz con Streamlit, optimizada para una mejor usabilidad.

### Justificación de la Viabilidad
- Desarrollado con tecnologías accesibles y de fácil implementación.
- Se aprovecha GPT-4 para análisis avanzados.
- Integración con bases de datos SQLite para almacenamiento eficiente.

## Herramientas y Tecnologías
- **Streamlit** → Interfaz de usuario interactiva.
- **BeautifulSoup** → Scraping de datos desde sitios web.
- **OpenAI API (GPT-4)** → Análisis de información y generación de resúmenes.
- **SQLite** → Base de datos local para el historial de búsquedas.
- **Pandas** → Estructuración y exportación de datos en CSV.
- **Python-dotenv** → Gestión segura de credenciales y variables de entorno.

## Arquitectura de la Aplicación
```
📂 E3-Project
│── .env  # Variables de entorno (API Key)
│── .gitignore  # Archivos a excluir en Git
│── app.py  # Código principal de la aplicación
│── history.db  # Base de datos local con búsquedas previas
│── companies_info.csv  # Exportación de datos en CSV
│── README.md  # Documentación del proyecto
│── requirements.txt  # Dependencias necesarias
│── .devcontainer/  # Configuración para entornos de desarrollo
```

## Instalación y Configuración

### Instalación
1. Clona el repositorio:
   ```bash
   git clone https://github.com/tuusuario/E3-Project.git
   cd E3-Project
   ```
2. Crea un entorno virtual:
   ```bash
   python -m venv env
   source env/bin/activate  # Mac/Linux
   env\Scripts\activate  # Windows
   ```
3. Instala dependencias:
   ```bash
   pip install -r requirements.txt
   ```
4. Configura tu API Key de OpenAI:
   - Crea un archivo `.env` en la raíz del proyecto.
   - Agrega la línea:
     ```plaintext
     OPENAI_API_KEY=tu_clave_aqui
     ```

### Ejecución de la Aplicación
Para iniciar la aplicación, ejecuta:
```bash
streamlit run app.py
```

## Ejemplo de Uso
Para probar la aplicación, puedes ingresar las siguientes empresas:

1. **Coca-Cola**  
   [https://www.coca-colacompany.com/](https://www.coca-colacompany.com/)  
   
2. **Ternium**  
   [https://ar.ternium.com/es](https://ar.ternium.com/es)  

## Funcionalidades Clave

### Búsqueda y Análisis de Empresas
- Permite ingresar hasta 5 URLs para extraer datos de sitios web y LinkedIn.
- Usa GPT-4 para estructurar la información en formato JSON.
- Calcula tokens usados y costos aproximados de cada análisis.

### Historial de Búsquedas
- Accesible desde la barra lateral.
- Filtro por nombre de empresa.
- Ordenamiento por fecha (más recientes primero).
- Descarga de resultados en CSV.

### Navegación Mejorada
- Historial de Búsquedas accesible desde la barra lateral.
- Botón "Back to Search" en el historial para regresar a la búsqueda.

## Próximos Pasos
- Mejorar el scraping de LinkedIn para mayor precisión.
- Agregar gráficos de análisis sobre las empresas consultadas.
- Integrar API externas para verificar datos financieros en tiempo real.

## Contacto
Si tienes dudas o sugerencias, puedes contactarme en:

**Email:** [arandigacatriel@gmail.com](mailto:arandigacatriel@gmail.com)  
**LinkedIn:** [Catriel Nicolás Arándiga](https://www.linkedin.com/in/catriel-nicolas-arandiga)

