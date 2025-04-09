# SQL_books_analytics
# 📚 Proyecto SQL: Análisis de libros durante la pandemia

Durante la pandemia de COVID-19, cambió el comportamiento de consumo de las personas, incrementando el interés por la lectura y generando nuevas oportunidades para startups enfocadas en aplicaciones de libros. Este proyecto utiliza una base de datos de una de estas startups para analizar patrones de comportamiento y ayudar en la generación de una propuesta de valor para un nuevo producto.

## 🔧 Herramientas utilizadas

- Python (Pandas)
- PostgreSQL (consultas SQL)
- SQLAlchemy
- psycopg2
- dotenv para manejo de credenciales
- Jupyter Notebook

## 🗂️ Descripción de la base de datos

La base de datos contiene la siguiente estructura:

### Tabla `books`
| Columna | Descripción |
|--------|-------------|
| book_id | ID del libro |
| author_id | ID del autor o autora |
| title | Título del libro |
| num_pages | Número de páginas |
| publication_date | Fecha de publicación |
| publisher_id | ID de la editorial |

### Tabla `authors`
| Columna | Descripción |
|--------|-------------|
| author_id | ID del autor o autora |
| author | Nombre del autor o autora |

### Tabla `publishers`
| Columna | Descripción |
|--------|-------------|
| publisher_id | ID de la editorial |
| publisher | Nombre de la editorial |

### Tabla `ratings`
| Columna | Descripción |
|--------|-------------|
| rating_id | ID de la calificación |
| book_id | ID del libro |
| username | Usuario que calificó |
| rating | Calificación |

### Tabla `reviews`
| Columna | Descripción |
|--------|-------------|
| review_id | ID de la reseña |
| book_id | ID del libro |
| username | Usuario que reseñó |
| text | Texto de la reseña |

## 🎯 Objetivos del análisis

Se realizaron consultas SQL para responder las siguientes preguntas:

1. ¿Cuántos libros fueron publicados después del 1 de enero de 2000?
2. ¿Cuál es el número de reseñas de usuarios y la calificación promedio para cada libro?
3. ¿Qué editorial ha publicado la mayor cantidad de libros con más de 50 páginas?
4. ¿Qué autor tiene la calificación promedio más alta considerando solo libros con al menos 50 calificaciones?
5. ¿Cuál es el número promedio de reseñas de texto entre los usuarios que han calificado más de 50 libros?

## 📈 Resultados

Las consultas fueron escritas en SQL y ejecutadas directamente sobre la base de datos usando SQLAlchemy y psycopg2, almacenando y mostrando los resultados con Pandas.

Cada resultado fue analizado y comentado en el notebook para generar conclusiones útiles de negocio.

## 🧠 Conclusión

Este análisis ofrece información clave para identificar oportunidades en el mercado editorial digital: las editoriales más activas, los autores con mejor recepción del público, y los usuarios más comprometidos con la plataforma. Esta información puede ser utilizada para el diseño de nuevas funciones, selección de contenido recomendado y estrategias de marketing más efectivas.
