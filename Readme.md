# ODOO - TAREA BBDD
*Esteban Miguel montes Adraz* - *2 DAM* - *SXE*

## APARTADO 1 :smile:
**Enunciado**  :point_down:

Como mencionamos en clase, aunque no es recomendable, en ocasiones puede ser
necesario crear tablas ajenas a Odoo dentro de su base de datos (integración con
sistemas externos, almacenamiento de históricos, datos temporales…). Mediante la
herramienta PgAdmin u otro método que estimes oportuno, elabora y ejecuta una
sentencia que cree una tabla llamada “EmpresasFCT“con los siguientes campos:
- **idEmpresa**: autonumérico. Este campo será la clave primaria.
- **nombre**: Texto con tamaño máximo de 40 caracteres.
- **quiereAlumnos**: Booleano.
- **numAlumnos**: número entero.
- **fechaContacto**: tipo fecha
--- 

Para hacer este apartado, primero entramos a PGAdmin y seleccionamos nuestra base de datos, en este caso su nombre es ```OdooDB```. Una vez seleccionada la base, le damos click al apartado llamado ```Esquemas``` y luego al desplegable llamado ```Tablas```. A esta última le daremos click derecho y nos saldrá esto:
![imagen1](img/foto2.png)

Aquí seleccionaremos la opción ```Crear``` y le daremos a ```Tabla...```. Nos saldrá una ventana emergente en la que pondremos el nombre de la tabla, en este caso ```EmpresasFCT```. Una vez hecho esto, le daremos a la pestaña ```Columnas``` e introduciremos la siguiente información:
![imagen2](img/foto1.png)

Para añadir una columna nueva tenemos que darle al ```+``` que está en la parte superior derecha de la ventana. Una vez añadidas todas las columnas, le daremos a ```Guardar``` y ya tendremos nuestra tabla creada.

## APARTADO 2 :neutral_face:
**Enunciado** :point_down:

Inserta 5 registros inventados en la tabla a través de una sentencia SQL.

---

Haremos click en el apartado que pone ```Herramientas de consulta```, que está en la esquina superior izquierda

![imagen4](img/foto5.png).

Al darle click vamos 