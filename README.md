Hola!

Para que la página web de HoneyTrack funcione correctamente, se debe actualizar la base de datos que está en la ruta /HoneyTrack/DataBase/HoneyTrackv2.sql Este archivo contiene las tablas y está listo para ser cargado en una base de datos ya existente. NOTA: La base de datos se debe llamar "HoneyTrackv2" para que la conexión sea exitosa. Una vez creada la base de datos, se puede insertar las tablas del archivo con el siguiente comando: mysql -u root -p HoneyTrackv2 < HoneyTrackv2.sql
También es importante crear el usuario "cisco" con la contraseña "class". Para crearlo es necesario usar el siguiente comando dentro de mysql: "CREATE USER 'cisco'@'localhost' IDENTIFIED BY 'class';". Una vez creado, se le deben asignar todos los permisos con el siguiente comando: "GRANT ALL PRIVILEGES ON * . * TO 'cisco'@'localhost';". Si no se agrega este usuario al servidor local MySQL, no se podrán realizar las conexiones de la página web con la base de datos.

Gracias.
