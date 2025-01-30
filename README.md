# OdooTarea12

En esta tarea trabajaremos con la propia base de datos de Odoo gracias a PGAdmin que nos permite gestionar las bases de datos del servicio conectado a él (Wordpress,Odoo). En este caso nuestro PgAdmin está conectado al servicio de Odoo. Para este ejercicio crearemos una nueva 
base de datos que en mi caso llamaré Tarea12 en la que instalaremos la demoData, es decir unos datos de prueba que nos proporciona el propio Odoo. Es importante recalcar que estes datos cambian dependiendo del país que seleccionemos lo que nos dará problemas en el futuro como
podremos ver en los siguientes pasos. Por ello es importante tener en cuenta esto. 

## CONFIGURACIÓN INICIAL: Desde la interfaz de Odoo, instalamos Facturación y contactos. 

![image](https://github.com/user-attachments/assets/3fec8395-9f1c-4780-b9f2-9cde2e10993c)

## APARTADO 1: Creación de una nueva tabla. 

Para ello entramos en PgAdmin y seleccionamos la opción de CrearTabla. 

![image](https://github.com/user-attachments/assets/cd8787af-3f10-4bb6-9a9d-5908536ed8e4)

Después creamos la tabla con los datos necesarios y las especificaciones precisas. 
● idEmpresa: autonumérico. Este campo será la clave primaria.(Serial, primary key)
● nombre: Texto con tamaño máximo de 40 caracteres.(character, lenght 40)
● quiereAlumnos: Booleano.(Boolean)
● numAlumnos: número entero.(integer)
● fechaContacto: tipo fecha (date)

![image](https://github.com/user-attachments/assets/eb25a271-c017-4e68-9513-6c282cabf0d9)

Escribimos el Script para añadir 5 nuevos ingresos a la tabla (en mi caso he colocado números del 1-5 en el serial para ser más fácil gestionar la clave primaria pero al ser serial no hace falta añadir un número ya que postgres te lo genera automáticamente. Pero para tener unos números simples y fáciles de seguir he decido colocar el número)

![image](https://github.com/user-attachments/assets/4f3550af-3c4e-4c6f-94b2-345ea3c7a1c4)

Comprobamos que se han insertado correctamente: 

![image](https://github.com/user-attachments/assets/c0251a8c-330a-498b-b634-321586a652f1)

Ordenamos con una consulta por orden Ascendente por la fecha de Contacto: 
![image](https://github.com/user-attachments/assets/5d5efd8b-90ca-4d49-883d-4c94cf44f8c6)

Ahora realizamos una consulta para obtener un listado de todos los contactos de
Odoo (no empresas) con la siguiente información:

- Nombre
- Cuya ciudad sea Tracy
- Nombre comercial de la empresa
  
![image](https://github.com/user-attachments/assets/6da28172-d259-4ac1-83ba-47243df70cd2)

Obtener un listado de empresas proveedoras, que han emitido algún reembolso (facturas rectificativas de proveedor)
- Nombre de la empresa
- Número de factura
- Fecha de la factura
- Total factura SIN impuestos
Ordenadas por fecha de factura de modo que la primera sea la más reciente.

![image](https://github.com/user-attachments/assets/2d49f368-bb1a-4f70-ba14-7911994a1660)

Obtener un listado de empresas clientes, a las que se les
ha emitido más de dos facturas de venta (solo venta) confirmadas, mostrando los
siguientes datos:
- Nombre de la empresa
- Número de facturas 
- Total facturado SIN IMPUESTOS
- 
![image](https://github.com/user-attachments/assets/859828c7-f0e9-4d93-9b63-42cf825b4813)

Cambiamos de base de datos por no seleccionar el país, la demo data varía ligeramnete de un país a otro y es necesario repetir el ejercicio por esto




Crea una sentencia que actualice el correo de los contactos cuyo dominio es
@bilbao.example.com a @bilbao.bizkaia.eus

![image](https://github.com/user-attachments/assets/6d9c05c8-b757-406a-bab0-615085fd6dca)

La empresa Ready Mat ha hecho un ERE y ha despedido a todos los empleados
que tenías como contacto. Crea una sentencia que elimine todos los contactos
pertenecientes a la empresa “Ready Mat”, pero mantén la empresa. Añade una
captura de pantalla de la sección de contactos de odoo con Ready Mat antes y
después.

Contactos de "ReadyMat" antes de la consulta 
![image](https://github.com/user-attachments/assets/dd3f7984-1f1e-48c1-81ef-b9cd892aa72e)

Eliminamos los contactos de ReadyMat que tenemos en uestra base de datos con la siguiente consulta

![image](https://github.com/user-attachments/assets/17d42d09-bccd-402f-b608-1e9ff6517bac)

Ahora al entrar en nuestro Odoo nos aparece esto en ReadyMat 

![image](https://github.com/user-attachments/assets/048bb40f-a4ec-4376-b168-82de77719be0)





















