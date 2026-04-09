# Proyecto BBDD

Proyecto de diseño e implementación de una **base de datos relacional** a partir de archivos CSV con información de estudiantes y claustro, desarrollado en **PostgreSQL**.

## Objetivo

El objetivo del proyecto fue transformar una estructura plana de datos en un modelo relacional organizado, normalizado y preparado para consultas SQL.

Para ello, se trabajó en tres fases principales:

- limpieza y transformación de los datos con **pandas**
- diseño del **modelo entidad-relación** y del **modelo lógico**
- implementación de la base de datos en **PostgreSQL** mediante **pgAdmin**

---

## Datos de entrada

Los archivos utilizados como punto de partida fueron:

- `clase_1.csv`
- `clase_2.csv`
- `clase_3.csv`
- `clase_4.csv`
- `claustro.csv`

Los cuatro archivos de clase contenían información de estudiantes y compartían una estructura similar, por lo que se integraron en un único conjunto de datos.  
El archivo `claustro.csv` se trató por separado al corresponder a una entidad diferente.

---

## Proceso realizado

### 1. Limpieza y transformación
- concatenación de los archivos de estudiantes
- carga separada de `claustro.csv`
- corrección de pequeñas inconsistencias
- transformación de proyectos de formato ancho a formato largo mediante `melt`
- creación de tablas de referencia y tablas principales

### 2. Normalización
Se separaron los valores repetidos en tablas independientes para reducir redundancia y mejorar la consistencia del modelo.

Tablas de apoyo creadas:
- `campus`
- `modalidad`
- `promocion`
- `rol`
- `vertical`
- `tipo_proyecto`

### 3. Modelado
Se elaboró un **diagrama E/R** y un **modelo lógico** para representar las entidades principales, sus atributos y relaciones.

### 4. Implementación en PostgreSQL
Se creó la base de datos en PostgreSQL y se implementaron las tablas necesarias para almacenar la información transformada y ejecutar consultas SQL.

---

## Estructura de la base de datos

### Tablas principales
- `estudiante`
- `faculty`
- `calificacion`

### Tablas de apoyo
- `campus`
- `modalidad`
- `promocion`
- `rol`
- `vertical`
- `tipo_proyecto`

---

## Diagramas

Los diagramas del proyecto se encuentran en la carpeta `diagramas/`:

- `er_diagrama_final.pdf`
- `er_diagrama_simple.pdf`
- `modelo_logico_final.pdf`

---

## Notebook principal

El proceso de limpieza y transformación de los datos se encuentra en:

- `notebooks/limpieza_y_transformacion_datos.ipynb`

---

## Scripts SQL

Los scripts SQL se encuentran en la carpeta `sql/`:

- `01_create_tables.sql`
- `02_insert_data.sql`
- `03_queries_demo.sql`

> Nota: estos archivos recogen la estructura y las consultas del proyecto y pueden seguir ajustándose para reflejar exactamente la versión final validada en PostgreSQL.

---

## Presentación

Presentación editable en Canva:

[https://canva.link/d36afws5q9grnm8](https://canva.link/d36afws5q9grnm8)

---

## Estructura del repositorio

```text
proyecto-bbdd/
├── data/
├── diagramas/
├── notebooks/
├── sql/
├── .gitignore
└── README.md
