# Historia de usuario - Semana 2
# Diseño y consulta de un Sistema Académico en SQL
 
## Objetivo de la Historia de usuario
- Como usuario de una institución académica:
Diseñar e implementar una base de datos académica que soporte estudiantes, docentes, cursos e inscripciones, aplicando SQL (DDL, DML, DQL, DCL y TCL) con consultas de análisis (agregaciones, subconsultas y vistas), para administrar la información académica y analizar el rendimiento de forma confiable.
- Crear la BD gestion_academica_universidad.
- Definir tablas con restricciones (NOT NULL, UNIQUE, FOREIGN KEY, CHECK).
- Insertar datos de ejemplo, ejecutar JOINs, GROUP BY, AVG, HAVING, ALTER TABLE, ON DELETE.
- Construir una vista y gestionar permisos y transacciones (GRANT/REVOKE, BEGIN/SAVEPOINT/ROLLBACK/COMMIT).
 
## Descripción de las tareas
### TASK 1
1. Diseño inicial y creación de la base de datos:
Crea la base de datos: gestion_academica_universidad.
Diseña las tablas con los siguientes campos mínimos y llaves:
estudiantes: id_estudiante (PK, autoincremental), nombre_completo, correo_electronico, genero, identificacion (UNIQUE), carrera, fecha_nacimiento, fecha_ingreso
docentes: id_docente (PK, autoincremental), nombre_completo, correo_institucional, departamento_academico, anios_experiencia
cursos: id_curso (PK, autoincremental), nombre, codigo (UNIQUE), creditos, semestre, id_docente (FK)
inscripciones: id_inscripcion (PK, autoincremental), id_estudiante (FK), id_curso (FK), fecha_inscripcion, calificacion_final
Aplica NOT NULL, UNIQUE, FOREIGN KEY y CHECK donde corresponda.
### TASK 2
2. Inserción de datos:
Inserta al menos 5 estudiantes, 3 docentes y 4 cursos.
Genera 8 inscripciones distribuidas entre cursos y estudiantes.
### TASK 3
3. Consultas básicas y manipulación:
Listar todos los estudiantes con sus inscripciones y cursos (JOIN).
Listar cursos dictados por docentes con > 5 años de experiencia.
Obtener promedio de calificaciones por curso (GROUP BY + AVG).
Mostrar estudiantes inscritos en más de un curso (HAVING COUNT(*) > 1).
ALTER TABLE: agregar columna estado_academico a estudiantes.
Eliminar un docente y observar el efecto en cursos (revisar ON DELETE en la FK).
Consultar cursos con más de 2 estudiantes inscritos (GROUP BY + COUNT + HAVING).
### TASK 4
4. Subconsultas y funciones:
Estudiantes cuya calificación promedio sea > promedio general (AVG() + subconsulta).
Nombres de carreras con estudiantes inscritos en cursos del semestre ≥ 2 (IN o EXISTS).
Usar ROUND, SUM, MAX, MIN, COUNT para obtener indicadores.
(Esta tarea se apoya en el soporte temático de la semana sobre DQL, filtros, agregaciones, GROUP BY/HAVING y funciones)
### TASK 5
5. Creación de una vista:
Crea la vista vista_historial_academico que muestre: nombre del estudiante, nombre del curso, nombre del docente, semestre y calificación final.
### TASK 6
6. Control de acceso y transacciones:
Otorga permisos de solo lectura a un rol revisor_academico sobre la vista (GRANT SELECT).
Revoca permisos de modificación de datos en inscripciones para ese rol (REVOKE).
Simula actualización de calificaciones usando BEGIN, SAVEPOINT, ROLLBACK y COMMIT.
 
# Criterios de aceptación
BD creada y tablas definidas con PK/FK y restricciones (NOT NULL, UNIQUE, CHECK) según el diseño indicado.
Datos mínimos insertados (5 estudiantes, 3 docentes, 4 cursos, 8 inscripciones).
Consultas de la ### Task 3 funcionan y evidencian JOIN, GROUP BY, AVG, HAVING, ALTER TABLE y el comportamiento de ON DELETE.
Subconsultas y funciones (### Task 4) entregan resultados correctos (promedio > general; filtros con IN/EXISTS; ROUND/SUM/MAX/MIN/COUNT).
Vista vista_historial_academico creada con las columnas requeridas.
Permisos y transacciones configurados y demostrados (GRANT/REVOKE; BEGIN/SAVEPOINT/ROLLBACK/COMMIT).