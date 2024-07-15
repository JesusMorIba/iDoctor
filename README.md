# Proyecto iDoctor

El proyecto iDoctor es una aplicación de gestión diseñada para conectar usuarios con profesionales de la salud. La aplicación proporcionará perfiles para doctores, fisioterapeutas y dentistas, y permitirá a los usuarios buscar profesionales, ver sus horarios, realizar reservas de citas, ver informes y valoraciones.

Con este proyecto buscamos crear una aplicación que simplifique la administración de las consultas de salud y mejore la comunicación de los pacientes y los profesionales. Se usará una base de datos en tiempo real, en concreto, Firebase Realtime Database.

## Requisitos de Información

Los requisitos de información son aquellos que nos indican la información que debemos almacenar y la estructura de dicha información. Nuestra aplicación deberá almacenar datos de:

- **Usuario**: nombre de usuario y contraseña.
- **Profesional**: nombre, apellidos, foto, número de colegiado, especialidad (General, Fisioterapia u Odontología), descripción, media de estrellas y número de valoraciones.
- **Paciente**: nombre, apellidos, foto, email, teléfono y si tiene seguro médico o no.
- **Consulta**: dirección, ciudad, email, teléfono, teléfono auxiliar y observaciones.
- **Horario**: día de la semana (Lunes, Martes, Miércoles, Jueves, Viernes, Sábado y Domingo), hora de inicio y hora de fin.
- **Cita**: fecha de la cita, hora de la cita y si está activa o no.
- **Evaluación**: descripción, exploración, tratamiento, fecha y hora de la evaluación.

Además, debemos almacenar un identificador de todas las entidades anteriores.

## Requisitos Funcionales

Los requisitos funcionales indican las diferentes funcionalidades que debe realizar nuestra aplicación:

### Usuarios
- Un usuario debe ser capaz de registrarse en la aplicación con el Rol de Profesional o Paciente.
- Un usuario debe ser capaz de entrar en la aplicación mediante su nombre de usuario y contraseña.
- Un usuario logueado debe ser capaz de cerrar sesión.

### Profesional
- Un profesional debe ser capaz de gestionar sus consultas (listar, crear, editar y eliminar).
- Un profesional debe ser capaz de gestionar el horario de sus consultas (listar, crear, editar y eliminar).
- Un profesional debe ser capaz de gestionar sus citas (listar, crear, editar y eliminar).
- Un profesional debe ser capaz de realizar una evaluación de una cita médica.
- Un profesional debe ser capaz de listar todas las valoraciones que ha recibido y verlas en detalle.
- Un profesional debe ser capaz de generar automáticamente las citas asociadas a una de sus consultas de una semana o un mes.

### Paciente
- Un paciente debe ser capaz de listar todos los profesionales de la aplicación y verlos en detalle.
- Un paciente debe ser capaz de reservar una cita médica con algún profesional.
- Un paciente debe ser capaz de listar todas sus citas médicas.
- Un paciente debe ser capaz de ver en detalle sus citas médicas y cancelarla si la fecha de la reserva no ha pasado.
- Un paciente debe ser capaz de ver las evaluaciones de sus citas médicas.

## Requisitos No Funcionales

Los requisitos no funcionales describen las funciones específicas que el sistema debe realizar, se centran en cómo debe funcionar el sistema en términos de calidad, rendimiento, seguridad y otras características importantes. Los requisitos no funcionales que debe cumplir nuestra aplicación son los siguientes:

- Un usuario no registrado solo podrá registrarse como Profesional o como Paciente, o loguearse mediante un nombre de usuario y contraseña.
- Un Profesional solo podrá crear citas asociados a sus consultas.
- Se debe implementar un sistema de control de roles para gestionar los permisos de acceso a las diferentes pantallas.
- Las contraseñas deben almacenarse cifradas.