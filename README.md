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

## Resumen de resultados hallados

![](https://drive.google.com/uc?id=1-OK4bymc0kV8K4ehqyxAPFqY80oZ6OwZ)

## Estado del Proyecto

El proyecto se encuentra concluido. Se puede modificar el insumo de la base de datos y correr el jupyter note para estimaciones de otros trimestres de EPH.

## Crédito y contacto

Germán Tessmer\
email: [ger.tessmer\@gmail.com](ger.tessmer@gmail.com)\
[LinkedIn](https://www.linkedin.com/in/gtessmer/)  [ORCID](https://orcid.org/0000-0002-3827-7027)
