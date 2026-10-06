# Análisis de sensores industriales Examen Primer parcial

### Andrés Tadeo Carmona Capula
### IDIA222
### 05/10/2026

# Monitoreo y Análisis de Sensores Industriales

Este proyecto realiza el procesamiento y análisis de mediciones de temperatura y vibración en plantas industriales. La solución se encuentra implementada de forma reproducible a través de un Jupyter Notebook en Python (`src/analisis.ipynb`).

## 🎯 Objetivo del Proyecto

El objetivo de este proyecto es analizar un conjunto de datos masivo de sensores industriales para extraer métricas clave y alertar sobre posibles fallas operativas. Específicamente, el sistema busca:

1. **Analizar** 100,000 registros de lecturas de sensores distribuidas en cuatro plantas industriales.

2. **Calcular** la temperatura promedio por planta y detectar la temperatura máxima absoluta registrada (indicando el sensor y la fecha/hora exacta).

3. **Identificar** lecturas críticas que superen el umbral de alerta establecido en **85 °C**.

4. **Determinar** la planta con el mayor número de alertas de temperatura registradas.

5. **Exportar** todas las lecturas de alerta a un archivo CSV (`resultados/alertas.csv`), conservando las columnas originales.

## 📊 Descripción de los Datos

> ⚠️ **IMPORTANTE - NOTA SOBRE LOS DATOS:**
> **Todos los datos contenidos en este dataset son completamente simulados** con fines académicos e industriales didácticos.

El archivo de datos de entrada se encuentra ubicado en `data/sensores_industriales.csv` y cuenta con un total de 100,000 registros.

### Estructura de las Columnas

| Columna | Tipo de Dato | Descripción | 
| ----- | ----- | ----- | 
| `id_registro` | Entero (`int`) | Identificador único de cada medición individual | 
| `fecha_hora` | Texto / Datetime | Fecha y hora en la que se realizó la lectura | 
| `id_sensor` | Texto (`str`) | Código identificador del sensor (ej. `S001`) | 
| `planta` | Texto (`str`) | Nombre de la planta donde está instalado el sensor (ej. `Planta_1`) | 
| `temperatura_c` | Flotante (`float`) | Lectura de temperatura en grados Celsius (°C) | 
| `vibracion_mm_s` | Flotante (`float`) | Lectura de vibración en milímetros por segundo (mm/s) | 

## 📦 Dependencias del Proyecto

Este proyecto utiliza librerías de terceros (`pandas`, `jupyter`, `notebook`, `ipykernel`) para la manipulación eficiente de datos y la visualización del cuaderno.

* *Nota:* Si prefirieras utilizar únicamente la **biblioteca estándar de Python** (como los módulos `csv`, `datetime` o `collections`), el proyecto **no requeriría dependencias externas**. Sin embargo, al hacer uso de Pandas y Jupyter, las dependencias exactas y sus versiones correspondientes se encuentran especificadas en el archivo `requirements.txt`.

## 🛠️ Instalación y Configuración

Sigue estos pasos para clonar el proyecto y configurar el entorno de ejecución:

### 1. Clonar el repositorio

```
git clone https://github.com/Tadand-64/An-lisis-de-sensores-industriales-Examen-Primer-parcial.git
cd An-lisis-de-sensores-industriales-Examen-Primer-parcial

```

### 2. Crear y activar el entorno virtual (`.venv`)

* **En macOS / Linux:**

  ```
  python3 -m venv .venv
  source .venv/bin/activate
  
  ```

* **En Windows (PowerShell / CMD):**

  ```
  python -m venv .venv
  .venv\Scripts\activate
  
  ```

### 3. Instalar las dependencias (`requirements.txt`)

Con el entorno virtual activado, instala los paquetes requeridos:

```
pip install -r requirements.txt

```

## 🚀 Comandos para Ejecutar el Proyecto

Para ejecutar el notebook del análisis (`src/analisis.ipynb`), puedes elegir una de las siguientes opciones:

### Opción A: Desde Visual Studio Code (Recomendado)

1. Abre la carpeta raíz del proyecto en VS Code.

2. Abre el archivo `src/analisis.ipynb`.

3. Selecciona el kernel de Python apuntando a tu entorno virtual (`.venv`).

4. Haz clic en **Run All** (Ejecutar todo) en la parte superior del notebook.

### Opción B: Desde la línea de comandos con Jupyter Lab / Notebook

1. Activa tu entorno virtual `.venv`.

2. Ejecuta uno de los siguientes comandos en la terminal:

   ```
   jupyter lab
   
   ```

   *o bien:*

   ```
   jupyter notebook
   
   ```

3. En el navegador que se abre, navega a la carpeta `src/` y selecciona `analisis.ipynb`.

4. En el menú superior, selecciona **Kernel > Restart & Run All**.

Al finalizar la ejecución, el análisis mostrará las métricas solicitadas y generará el archivo `resultados/alertas.csv` de forma automática.
