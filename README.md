:card_index_dividers: # Gestión de usuarios

## Resumen

Aplicación para la gestión de usuarios de una aplicación web.

Aplicación se deberá realizada a través de API REST (HTTP).
La aplicación persistirá los datos, de forma que si se para todos los cambios deberán permanecer guardados(especie de base de datos)

## Definición de entidades

-   **Usuario**: Usuario registrado en la plataforma, todos los campos son obligatorios.
    -   Nombre: Mínimo de 2 caracteres y un máximo 20 (Todos los caracteres serán válidos)
    -   Apellidos: Mínimo de 4 y máximo de 50 (Todos los caracteres serán válidos)
    -   Email: Deberá cumplir el [RFC 5322](https://www.ietf.org/rfc/rfc5322.txt)
    -   Contraseña: Mínimo de 10 caracteres y máximo de 25 (Al menos una minúscula, mayúscula y un número)

## Requisitos funcionales

-   El usuario podrá registrarse en la aplicación, introduciendo los datos necesarios.
    -   El email debe ser único por cada usuario.
-   El usuario podrá autenticarse ante la aplicación utilizando su email y contraseña.
    -   Si la autenticación es válida, la aplicación le devolverá al usuario un identificador que le servirá para demostrar su identidad ante la aplicación cuando quiera cambiar/eliminar sus datos.
-   El usuario podrá obtener todos sus datos exceptuando su contraseña, utilizando su identificador.
-   El usuario podrá actualizar su nombre y apellidos, será necesario el identificador.
-   El usuario podrá actualizar su email, será necesario el identificador y la contraseña actual.
-   El usuario podrá actualizar su contraseña, será necesario el identificador y la contraseña actual.
-   El usuario podrá eliminar todos sus datos de la plataforma, será necesario el identificador y la contraseña actual.

## Requisitos no funcionales

-   La aplicación se puede ejecutar con la versión LTS de Node.JS(16).
-   Se puede utilizar cualquier base de datos, aunque es recomendable utilizar Mongo.DB
