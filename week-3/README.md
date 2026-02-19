# Historia de usuario - Semana 3
# Gestión de contenido y usuarios en MongoDB
 
## Objetivo de la Historia de usuario
- Como usuario:
- Modelar e implementar en MongoDB colecciones para usuarios, contenido audiovisual y valoraciones, realizando CRUD, creando índices y ejecutando agregaciones para gestionar datos semiestructurados de forma eficiente y obtener reportes y métricas de uso.
- Aplicar conceptos de NoSQL, MongoDB CRUD (insertOne/insertMany, find, updateOne/updateMany, deleteOne/deleteMany), índices (createIndex, getIndexes) y agregaciones (aggregate con $match, $group, $sort, $project, $unwind).
- Utilizar operadores de consulta $gt, $lt, $eq, $in, $and, $or, $regex y comparadores/lógicos avanzados.
 
## Descripción de las tareas
### TASK 1
1. Análisis del dominio (StreamHub) y diseño de documentos:
Identifica colecciones necesarias (p. ej., usuarios, películas, series, valoraciones, listas).
Define la estructura JSON de cada documento (campos, arreglos, documentos anidados).
### TASK 2
2. Inserción de datos:
Población inicial con insertOne() y/o insertMany() en las colecciones definidas.
Incluye variedad de casos (p. ej., películas con reseñas, usuarios con historial).
### TASK 3
3. Consultas (Lectura) con operadores:
Realiza find() con filtros empleando $gt, $lt, $eq, $in, $and, $or, $regex.
Ejemplos sugeridos:
Películas con duración > 120 min
Usuarios que vieron > 5 contenidos
### TASK 4
4. Actualizaciones y eliminaciones:
Modifica información con updateOne()/updateMany() (p. ej., actualizar calificación de un contenido).
Elimina documentos con deleteOne()/deleteMany() cuando aplique.
### TASK 5
5. Índices para performance:
Crea índices con createIndex() sobre campos consultados con frecuencia (p. ej., título, género).
Verifica índices existentes con getIndexes() y documenta tus decisiones.
 
# Criterios de aceptación
Se definieron y documentaron colecciones y documentos adecuados para el dominio.
Se poblaron datos con insertOne/insertMany cubriendo casos variados.
Existen consultas find() usando operadores $gt, $lt, $eq, $in, $and, $or, $regex con resultados coherentes.
Se ejecutaron updateOne/updateMany y deleteOne/deleteMany correctamente.
Se crearon y verificaron índices con createIndex/getIndexes, justificando su elección (mejora de consulta).
Se entregaron ≥ 2 pipelines de agregación con $match, $group, $sort, $project, $unwind para métricas solicitadas.
Entrega en .zip con script + (opcional) evidencias de Compass, siguiendo estas especificaciones:
Un archivo .js o .txt con todos los comandos de MongoDB usados (inserciones, consultas, updates/deletes, índices y agregaciones).
Mínimo dos consultas de aggregate() incluidas.
Adjunta capturas o exportaciones desde MongoDB Compass (opcional).
Comprime en .zip y sube a Moodle antes de la fecha de entrega.