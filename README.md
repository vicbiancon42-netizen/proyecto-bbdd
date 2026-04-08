# Proyecto BBDD

## Descripción del proyecto
Este proyecto tiene como objetivo transformar una tabla plana con datos de alumnado y claustro en una base de datos relacional normalizada.

A partir de varios archivos CSV, se trabaja la limpieza, organización y estructuración de los datos para construir un modelo relacional en PostgreSQL, acompañado de su diagrama E/R, modelo lógico, scripts SQL y consultas de prueba.

---

## Objetivo
Diseñar una base de datos funcional y escalable que permita:

- separar entidades correctamente
- reducir redundancia
- mantener integridad referencial
- consultar la información de forma clara y eficiente

---

## Flujo general del proyecto

CSV data  
↓  
Python + pandas  
↓  
PostgreSQL  
↑  
pgAdmin 4  

### Explicación del flujo
- **CSV data**: punto de partida con los datos originales en formato plano
- **Python + pandas**: lectura, limpieza, transformación y preparación de tablas
- **PostgreSQL**: base de datos relacional final
- **pgAdmin 4**: entorno para validar la estructura, ejecutar scripts y probar queries

---

## Estructura del repositorio

proyecto-bbdd/  
├── README.md  
├── data/  
├── diagrams/  
├── notebooks/  
└── sql/  

### Contenido de cada carpeta
- `data/` → archivos CSV originales
- `notebooks/` → notebooks de análisis y limpieza
- `diagrams/` → diagrama E/R y modelo lógico visual
- `sql/` → scripts SQL de creación, inserción y consultas
- `README.md` → documentación general del proyecto

---

## Convenciones de organización

- Los archivos CSV originales van en `data/`
- Los notebooks de análisis y limpieza van en `notebooks/`
- Los diagramas finales van en `diagrams/`
- Los scripts SQL finales van en `sql/`
- Los nombres de archivos deben ser claros y consistentes

---

## Estado actual del proyecto
Hasta el momento se ha realizado:

- creación del repositorio base
- organización inicial de carpetas
- subida del notebook de limpieza inicial
- análisis preliminar de la estructura de los datos
- propuesta inicial de entidades y relaciones

---

## Archivos actuales

### Notebooks
- `cleanup_daniel.ipynb` → limpieza y transformación inicial de los datos

### SQL
- `01_create_tables.sql`
- `02_insert_data.sql`
- `03_queries_demo.sql`

---

## Puntos pendientes de validación en grupo
Todavía hace falta confirmar de forma conjunta:

- el modelo final de tablas y relaciones
- la estructura definitiva de `promocion`
- la modelización final de `proyectos`
- las claves primarias y foráneas definitivas
- los nombres finales de algunas entidades

---

## Checklist de trabajo

- [x] Crear repositorio base
- [x] Crear estructura inicial de carpetas
- [x] Subir notebook de limpieza inicial

- [ ] Subir archivos CSV originales a `data/`
- [ ] Validar en grupo el modelo final
- [ ] Cerrar entidades, relaciones, PK y FK
- [ ] Hacer diagrama E/R
- [ ] Hacer modelo lógico visual
- [ ] Generar tablas finales desde la limpieza
- [ ] Escribir `01_create_tables.sql`
- [ ] Escribir `02_insert_data.sql`
- [ ] Escribir `03_queries_demo.sql`
- [ ] Cargar la base en PostgreSQL
- [ ] Probar queries en pgAdmin
- [ ] Organizar la parte visual final
- [ ] Revisar README final
