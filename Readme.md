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

Al darle click vamos a añadirle las siguientes columnas de la siguiente manera:

![imagen5](img/foto4.png)

## APARTADO 3 :clown_face:

**Enunciado** :point_down:

Realiza una consulta donde se muestren todos los datos de la tabla EmpresasFCT
ordenados por fechaContacto, de modo que en la primera fila salga el que tenga la
fecha más reciente.

---

Para hacer esta consulta, como en el apartado anterior,
le damos a ```Herramienta de consulta``` y añadimos la siguiente línea de consulta
```SQL
SELECT * FROM public."EmpresasFCT"
```

Lo ponemos como en la imagen y le damos a ```Execute Script```
![imagen 6](img/foto6.png)

Como resultado nos tendría que salir todo lo que haya en el la tabla de
EmpresasFCT

![imagen 7](img/foto7.png)

## APARTADO 4 :stuck_out_tongue_closed_eyes:
**Enunciado** :point_down:

Realiza una consulta que permita obtener un listado de todos los contactos de
Odoo (no empresas) con la siguiente información:
- Nombre
- Cuya ciudad sea Tracy
- Nombre comercial de la empresa
ordenados alfabéticamente por el nombre comercial de la empresa.
 
---

En herrmientas de consulta pondremos la siguiente consulta
```SQL
SELECT name,commercial_company_name,city FROM public."res_partner"
WHERE city = 'Tracy'
```
![imagen 8](img/foto8.png)

Nos tendrá que salir de resultado la siguiente tabla
![imagen 9](img/foto9.png)
