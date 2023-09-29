# estudiar_paga

Estimación de una ecuación de Mincer mediante un modelo supervisado de regresión lineal utilizando algoritmos de *feature selection* para la identificación de controles, aplicado al primer trimestre de 2023 de la totalidad de los aglomerados urbanos de Argentina, utilizando la Encuesta Permanente de Hogares (EPH).

## Uso

-   El Jupyter Notebook que se presenta en este repositorio opera con un kernel Python 3.
-   Todos los archivos utilizados como insumo el Jupiter Notebook se encuentran disponibles en este repositorio.
-   Todo paso teórico o técnico ejecutado en el notebook se encuentra fundamentado al interior del archivo.
-   Además de la base de datos de EPH, se utilizan como insumo cuatro archivos donde se guardó la selección de variables de control derivadas de los procedimientos de feature selection aplicados. Esto obedece a que cada procedimiento insume tiempo y recursos de procesamiento. En todo caso, el código que permite correrlos se encuentra anulado como comentarios en los chunks correspondientes.

## Archivos

En esta carpeta se pueden encontrar, las siguientes sub-carpetas:

-   **datasets**: carpeta que incluye el dataset que a través de Drive alimenta al notebook.
-   **feature_selection**: carpeta que incluye el trabajo realizado en la etapa de feature selection.
-   **imagenes**: carpeta que incluye las archivos de imagenes incrustados en el notebook y que se vinculan vía Drive con éste.

Y los siguientes archivos:

-   **estudiar_paga.ipynb**: jupiter notebook de la estimación de Mincer.
-   **glosario de features.pdf**: glosario de las features utilizadas en los 5 modelos presentados.

## Glosario de contenidos del notebook

```         
1. Resumen / Abstract
2. Introducción
    2.1. Antecedentes, problemas, hipótesis y objetivos
        2.1.1. Hipótesis    
        2.1.2. Problemas a resolver    
        2.1.3. Objetivos    
        2.1.4. Contexto    
        2.1.5. Problemas de implementación
        2.1.6. Contexto analítico
    2.2. Preparación de la base de datos
        2.2.1. Carga de librerías    
        2.2.2. Carga del archivo    
        2.2.3. Descripción de la base de datos
3. Análisis Exploratorio de Datos - Parte 1
    3.1. Identificación de variables para análisis exploratorio
    3.2. Análisis Exploratorio de Datos (EDA1)
        3.2.1. Distribución del ingreso de la ocupación principal por sexo
        3.2.2. Descripción de la población según nivel educativo
        3.2.3. Relación entre nivel educativo alcanzado e ingreso de la ocupación principal
        3.2.4. Resumen general de insights obtenidos por EDA1
4. Transformación de variables (Data Wrangling)
    4.1. Identificación de variables para transformaciones
    4.2. Transformación de variables
        4.2.1. Salario por hora    
        4.2.2. Variables educativas
        4.2.3. Variables de contexto geográfico
        4.2.4. Variables de experiencia potencial           
        4.2.5. Variables de género o sexo
        4.2.6. Variables de empleo formal
        4.2.7. Variables por tipo de calificación
5. Análisis Exploratorio de Datos - Parte 2
    5.1. Distribución del logaritmo del ingreso laboral real por hora
        5.1.1. Análisis previo
        5.1.2. Análisis gráfico
        5.1.3. Interpretación general de los resultados
    5.2. Descripción de la población según nivel educativo con nivel terciario
        5.2.1. Análisis gráfico
        5.2.2. Interpretación general de los resultados
    5.3. Relación entre nivel educativo alcanzado y el logaritmo del ingreso laboral por hora
        5.3.1. Análisis previo
        5.3.2. Análisis gráfico
        5.3.3. Interpretación general de los resultados
    5.4. Relación el logaritmo del ingreso laboral por hora y la experiencia potencial
        5.4.1. Análisis previo
        5.4.2. Análisis gráfico
        5.4.3. Interpretación general de los resultado
    5.5. Relación del ingreso laboral por hora con resto del ingreso del hogar per capita
        5.5.1. Análisis previo
        5.5.2. Análisis gráfico
        5.5.3. Interpretación general de los resultados
    5.6. Resumen general de insights obtenidos por EDA2
6. Feature engineering
    6.1. Condicionamiento de instancias
    6.2. Condicionamiento de features
        6.2.1. Eliminación de variables originales
        6.2.2. Eliminación de variables elaboradas en este proyecto
        6.2.3. Eliminación de variables de ingreso nominal
        6.2.4. Eliminación de no convertibles a dummies
    6.3. Creación de variables dummies para las variables tipo objeto
        6.3.1. Pre-filtrado de variables categóricas bajo método Chi^2
        6.3.2. Creación de las variables
        6.3.3. Limpieza de las variables dummies no informativas de las respuestas
        6.3.4. Renombrado de dummies con espaciado en la label
    6.4. Adecuación de valores Nan
        6.4.1. Depuración de la variable objetivo
        6.4.2. Variables que incluyen en su totalidad valores NaN
        6.4.3. Otras variables con valores NaN
    6.5. Identificación de la matriz de características (X)
          6.5.1. Correlaciones entre las features identificadas por la teoría
          6.5.2. Eliminación de variables
    6.6. Identificación de la variable objetivo
7. Aplicación del método de selección
      7.1. Modelo Sequential Forward Selection para RMSE (parte 1)
      7.2. Modelo Sequential Backward Selection para RMSE (parte 1)
      7.3. Análisis de las features seleccionadas bajo SFS y SBS (Parte 1)
          7.3.1. Bloque de features geográficas
          7.3.2. Bloque de features referidas a calificación del trabajo
          7.3.3. Bloque de features referidas a cobertura de salud
          7.3.4. Bloque de features referidas a intensidad de trabajo
          7.3.5. Bloque de features referidas a cobros
          7.3.6. Bloque de features referidas a ingresos
          7.3.7. Bloque de features referidas a tipo de empresa
          7.3.8. Bloque de features referidas a cantidad de empleados de la empresa
          7.3.9. Bloque de features referidas a opciones laborales
          7.3.10. Bloque de features referidas a antigüedad laboral
          7.3.11. Bloque de features referidas a vacaciones
          7.3.12. Bloque de features referidas a miembros del hogar que contribuyen con las tareas domésticas
          7.3.13. Bloque de features referidas a tecnología utilizada en el trabajo con respecto a no uso de maquinaria
          7.3.14. Bloque de features referidas a tipo de relación de dependencia
          7.3.15. Resumen del análisis de las features seleccionadas bajo SFS y SBS
    7.4. Modelo Sequential Backward Selection para RMSE (parte 2)
    7.5. Analísis del Modelo Sequential Backward Selection para RMSE (parte 2)
          7.5.1. Bloques de features referidas a dias laborales pagos por enfermedad
          7.5.2. Bloques de features referidas a jerarquia en el puesto laboral
          7.5.3. Bloques de features referidas a subsidios en dinero
          7.5.4. Bloques de features referidas a renta financiera
          7.5.5. Bloques de features referidas a realización de tareas en la casa por el mismo individuo
          7.5.6. Bloques de features referidas a estabilidad del puesto laboral
          7.5.7. Bloques de features referidas a formalidad de pago
          7.5.8. Bloques de features referidas a jubilación
          7.5.9 Restantes bloques de features seleccionadas por SBS2 que ya estaban presentes anteriormente
          7.5.10 Resumen del análisis de las features seleccionadas bajo SBS (parte 2)
8. Modelos de regresión
    8.1. Modelo teórico básico
          8.1.1. Estimación OLS sin entrenamiento
          8.1.2. Estimación con entrenamiento y métricas
          8.1.3. Conclusiones en base a las métricas
    8.2. Modelo teórico con controles seleccionados sin feature engineering
          8.2.1. Estimación OLS sin entrenamiento
          8.2.2. Estimación con entrenamiento y métricas
          8.2.3. Conclusiones en base a las métricas
    8.3. Modelo con variables seleccionadas con feature selection y análisis posterior
          8.3.1. Estimación OLS sin entrenamiento
          8.3.2. Estimación con entrenamiento y métricas
          8.3.3. Conclusiones en base a las métricas
    8.4. Modelo con variables seleccionadas con feature selection (parte 2) y análisis posterior
          8.4.1. Estimación OLS sin entrenamiento
          8.4.2. Estimación con entrenamiento y métricas
          8.4.3. Conclusiones en base a las métricas
    8.5. Modelo libre
          8.5.1  Creación y uso del estimador de features
          8.5.2. Evaluación de métricas del modelo libre
          8.5.3. Comparación de métricas de modelos
          8.5.4. Conclusiones en base a las métricas
    8.6. Conclusiones en base a las métricas
9. Conclusiones generales
```

## Resumen de resultados hallados

![](https://drive.google.com/uc?id=1-OK4bymc0kV8K4ehqyxAPFqY80oZ6OwZ)

## Estado del Proyecto

El proyecto se encuentra concluido. Se puede modificar el insumo de la base de datos y correr el jupyter note para estimaciones de otros trimestres de EPH.

## Crédito y contacto

Germán Tessmer\
email: [ger.tessmer\@gmail.com](ger.tessmer@gmail.com)\
[LinkedIn](https://www.linkedin.com/in/gtessmer/)  [ORCID](https://orcid.org/0000-0002-3827-7027)
