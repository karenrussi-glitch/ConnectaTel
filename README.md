# ConnectaTel Sprint 7 Tripleten
Análisis de datasets que se complementan para analizar el comportamiento del usuario, su consumo en relación con el plan de telecomunicaciones contratado.

# Análisis de Clientes y Patrones de Consumo en ConnectaTel

## Descripción del Proyecto

Este proyecto tiene como objetivo analizar el comportamiento de los clientes de **ConnectaTel**, una empresa de telecomunicaciones en Latinoamérica, a partir de información histórica registrada hasta el año **2024**.

Mediante técnicas de exploración, limpieza de datos, análisis descriptivo, detección de valores atípicos y segmentación de clientes, se busca identificar patrones de consumo, oportunidades de negocio y posibles estrategias para optimizar la oferta comercial de la compañía.

## Objetivos

- Explorar la calidad y estructura de los datos disponibles.

- Identificar y corregir problemas de calidad de datos.

- Analizar el comportamiento de uso de llamadas y mensajes.

- Detectar clientes con patrones de consumo atípicos.

- Segmentar usuarios por edad y nivel de uso.

- Generar recomendaciones para mejorar los planes ofrecidos por ConnectaTel.

## Datasets Utilizados

### plans.csv

Contiene información sobre los planes comerciales ofrecidos por ConnectaTel:

- Nombre del plan

- Precio mensual

- Minutos incluidos

- Datos móviles incluidos

- Costo por consumo adicional

### users_latam.csv 

Contiene información demográfica y comercial de los clientes:

- `user_id`

- Edad

- Ciudad

- Fecha de registro

- Plan contratado

- Estado de cancelación (churn)

###  usage.csv

Contiene el histórico de uso de los servicios:

- `id`

- `user_id`

- Tipo de actividad (`call` o `text`)

- Duración de llamadas

- Longitud de mensajes

- Fecha de uso

##  Metodología del Análisis

### 1. Carga y Exploración de Datos

- Importación de librerías.

- Carga de datasets.

- Revisión inicial mediante:

- `.head()`

- `.shape()`

- `.info()`

### 2. Evaluación de Calidad de Datos

- Identificación de valores nulos.

- Cálculo de proporciones de datos faltantes.

- Detección de sentinels e inconsistencias.

- Revisión de variables categóricas y numéricas.

### 3. Limpieza de Datos

Correcciones realizadas:

- Sustitución del valor sentinel **-999** en la variable edad.

- Conversión de **"?"** a valores nulos en ciudad.

- Identificación y corrección de fechas fuera del rango válido.

- Validación de nulos dependientes del tipo de registro.

### 4. Construcción de Métricas por Usuario

Se generaron indicadores agregados:

- Cantidad de mensajes enviados.

- Cantidad de llamadas realizadas.

- Minutos totales consumidos en llamadas.

Estas métricas fueron integradas con la tabla de usuarios para construir perfiles de comportamiento.

### 5. Análisis Exploratorio y Visualización

Visualizaciones realizadas:

- Histogramas de distribución.

- Comparación de consumo según el tipo de plan.

- Boxplots para detección de outliers.

- Evaluación de patrones de consumo.

### 6. Segmentación de Clientes

#### Segmentación por Edad

- Joven

- Adulto

- Adulto Mayor

#### Segmentación por Nivel de Uso

- Bajo uso

- Uso medio

- Alto uso

### 7. Generación de Insights

- Identificación de segmentos relevantes.

- Evaluación de usuarios de alto valor.

- Recomendaciones estratégicas para ConnectaTel.

##  Principales Hallazgos

- Se detectaron valores sentinels e inconsistencias que requirieron limpieza previa.

- Se identificaron diferencias claras entre usuarios de bajo, medio y alto consumo.

- Los usuarios de alto uso representan oportunidades de monetización y fidelización.

- Existen clientes cuyo patrón de consumo podría ajustarse mejor a planes diferenciados.

- Se encontraron outliers asociados a usuarios con consumos significativamente superiores al promedio.

##  Tecnologías Utilizadas

- Python

- Pandas

- NumPy

- Matplotlib

- Seaborn

- Jupyter Notebook / Google Colab

##  Cómo Ejecutar el Proyecto

### Opción 1: Google Colab

1. Descarga el archivo `.ipynb`.

2. Abre [[[Google Colab](https://colab.research.google.com/).](https://colab.research.google.com/drive/14FkfNG8dbbyktBcVT2d3KlKzR1j04I0b?usp=sharing)]

3. Selecciona **Archivo → Subir notebook**.

4. Carga el notebook.

5. Sube los datasets necesarios.

6. Ejecuta las celdas en orden.

### Opción 2: Jupyter Notebook

Instala las dependencias:

```bash

pip install pandas numpy matplotlib seaborn

```

Inicia Jupyter:

```bash

jupyter notebook

```

Abre el notebook y ejecuta todas las celdas de forma secuencial.

## Guía de Reproducción

Para reproducir completamente el análisis:

### 1. Descargar los archivos

- `plans.csv`

- `users_latam.csv`

- `usage.csv`

### 2. Verificar estructura del proyecto

```text

Proyecto_ConnectaTel/
│
├── datasets/

│ ├── plans.csv

│ ├── users_latam.csv

│ └── usage.csv

│

├── notebook.ipynb

└── README.md

```

### 3. Ejecutar el notebook en el siguiente orden

1. Carga de datos.

2. Exploración inicial.

3. Evaluación de calidad.

4. Limpieza de datos.

5. Construcción de métricas.

6. Visualización y análisis exploratorio.

7. Detección de outliers.

8. Segmentación de clientes.

9. Conclusiones e insights ejecutivos.

## 💡 Recomendaciones de Negocio Derivadas

- Diseñar planes específicos para usuarios de alto consumo.

- Optimizar la oferta para clientes de bajo uso.

- Implementar campañas de migración entre planes según comportamiento.

- Crear estrategias diferenciadas para segmentos etarios.

- Monitorear continuamente clientes con consumos extremos para detectar oportunidades comerciales.

##  Autor

**Karen Lorena Russi Giraldo**

Proyecto desarrollado como parte de un ejercicio de análisis de datos enfocado en limpieza, exploración, segmentación de clientes y generación de insights de negocio utilizando Python.
