# Pipeline ETL para datos de ensayos clínicos Pfizer

Este repositorio contiene un pipeline ETL (Extract, Transform, Load) para procesar y analizar datos de ensayos clínicos, implementado en Python.

![Pipeline ETL](https://miro.medium.com/v2/resize:fit:1400/1*7zQzuTl1FZkAMD4aHYAw4A.png)

## Descripción

Este pipeline está diseñado para procesar datos de ensayos clínicos, incluyendo:

- Carga de datos de múltiples fuentes
- Limpieza y normalización de datos
- Detección y tratamiento de valores atípicos (outliers)
- Imputación de valores faltantes mediante KNN
- Normalización de identificadores
- Procesamiento de texto en notas clínicas
- Generación de variables derivadas clínicamente relevantes
- Clasificación de respondedores según criterios clínicos
- Codificación de variables categóricas
- Validación de calidad de los datos
- Visualización de resultados

## Requisitos

```
pip install pandas numpy scikit-learn fuzzywuzzy python-Levenshtein nltk matplotlib plotly
```

## Estructura del código

El pipeline está organizado en las siguientes secciones:

1. **Carga de datos**
   - Función `cargar_datos_clinicos()` que simula la carga desde múltiples fuentes

2. **Limpieza y normalización**
   - Normalización de categorías
   - Detección y manejo de outliers
   - Imputación de valores faltantes con KNN
   - Normalización de identificadores
   - Limpieza de texto en notas clínicas

3. **Transformación y Feature Engineering**
   - Generación de variables derivadas
   - Clasificación de respondedores
   - Agregación de eventos adversos
   - Codificación de variables categóricas
   - Normalización de variables continuas
   - Creación de variables de agrupación

4. **Validación de calidad**
   - Métricas de completitud
   - Detección de outliers
   - Valores imputados
   - Generación de reportes de calidad

5. **Visualización**
   - Distribuciones demográficas
   - Medidas clínicas por grupo de tratamiento
   - Relaciones entre variables
   - Proporción de respondedores
   - Mapas de calor de correlación

## Ejecución del pipeline

Para ejecutar el pipeline completo:

```python
# Ejecuta el pipeline completo
datos_procesados, reporte = ejecutar_pipeline_completo("/ruta/a/datos_ensayos_clinicos.csv")

# Genera visualizaciones
visualizar_datos(datos_procesados)
```

## Salida

El pipeline genera:

1. Un DataFrame de pandas con todos los datos procesados
2. Un reporte de calidad con métricas del proceso ETL
3. Visualizaciones para análisis exploratorio

## Contribuciones

Las contribuciones son bienvenidas. Por favor, siga estos pasos:

1. Haga fork del repositorio
2. Cree una nueva rama (`git checkout -b feature/nueva-caracteristica`)
3. Haga commit de sus cambios (`git commit -am 'Añade nueva característica'`)
4. Haga push a la rama (`git push origin feature/nueva-caracteristica`)
5. Abra un Pull Request

## Licencia

Este proyecto está licenciado bajo la Licencia MIT - vea el archivo LICENSE para más detalles.
