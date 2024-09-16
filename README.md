# AdminUsuarios-SQL
---- Sistema-Registro de Usuarios ---- 

## Descripción del Sistema: 
El **Sistema-Registro** es una aplicación de escritorio hecha en **C#** que sirve para administrar usuarios de una base de datos **SQL Server** de manera más sencilla. Ayuda a crear nuevos usuarios y a gestionar los que ya existen, todo desde una interfaz fácil de usar.

## El Problema: 
Administrar usuarios en **SQL Server** puede ser complicado y lleva tiempo si se hace directamente en el **Management Studio**.

_____________________________________________________________________________________________________________________________________________________

### Desglose General:

#### Capa de Presentación (Interfaz de Usuario)
- Esta es la capa que contiene los **formularios** o vistas que el usuario final interactúa.
- Se encarga de recibir las interacciones del usuario y mostrar los resultados de manera amigable.

#### Capa de Lógica de Negocios (Business Logic Layer)
- Aquí es donde reside la **lógica central** del sistema. Esta capa se encarga de procesar los datos, validar la información y aplicar las **reglas de negocio** del sistema.

#### Capa de Acceso a Datos (Data Access Layer)
- Aquí es donde se gestionan las interacciones con la **base de datos SQL Server**.
- En esta capa, el sistema realiza operaciones como **inserciones, consultas, actualizaciones y eliminaciones** de registros de usuarios.

#### Capa de Modelos (Entidades)
- Los **modelos** representan las estructuras de los datos que se están gestionando. En este caso, el modelo `Usuario` incluye las siguientes propiedades:
  - `nombreUsuario`: Nombre de usuario del sistema.
  - `contrasenia`: Contraseña del usuario.
  - `NombreUsuario`: Nombre completo del usuario.
  - `TipoUsuario`: Tipo o rol del usuario (por ejemplo, administrador o usuario estándar).
  - `FechaCreacion`: Fecha en que el usuario fue creado.
  - `RolesServidor`: Roles asignados al usuario dentro del servidor.
  - `UltimoInicioSesion`: Fecha y hora del último inicio de sesión del usuario. Este campo es opcional (nullable), permitiendo valores nulos.
---

### Ventajas de esta Estructura:

- **Modularidad**: Cada capa tiene su propia responsabilidad, lo que facilita el mantenimiento y futuras mejoras del sistema.
- **Reusabilidad**: Al tener una lógica de negocio bien definida, puedes reutilizar código en diferentes partes de la aplicación sin necesidad de duplicarlo.
- **Seguridad**: La capa de acceso a datos permite una interacción segura con la base de datos, controlando el acceso y protegiendo la integridad de los datos.

---

### Demostración del Sistema

[Muestra de uso del SISTEMA](https://vimeo.com/1010004301)

---
