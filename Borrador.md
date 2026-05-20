# Desarrollo del proyecto

## Requerimientos

Dentro del desarrollo interno de software de TenarisTamsa las especificaciones que el sistema debe de cubrir (los requerimientos de software) son establecidos por personal propio de la compañía, los cuales establecen las necesidades que se deben de contemplar para cubrirse en su totalidad. A través del equipo de desarrollo es que se van negociando estas propuestas para llevar un consenso especifico de lo que puede o no puede llegar a hacer el sistema.

El Sistema Integral de Producción conlleva diferentes módulos internos los cuales cubren necesidades de diferentes áreas operativas de la corporación, por lo que diferentes personas pueden llevar acabo consensos diferentes sobre lo que puede llevar o no ciertos módulos los cuales van a hacer disposición una vez implementado el sistema dentro de las áreas productivas de la empresa.

Sin embargo, es importante denotar que todos los módulos propios del Sistema Integral de Producción llevan los siguientes requerimientos debido a los estándares especificados por la corporación Tenaris.

### Requerimientos funcionales

- Inicio de sesión: Los usuarios que harán uso de algún módulo del Sistema Integral de Producción podrás iniciar sesión siempre y cuando estos hayan sido dados de alta dentro del módulo en cuestión por algún usuario administrador o gerencial.

- Gestionar usuario: Los usuarios con rol administrador o gerente tienen la capacidad de gestionar (crear, modificar, eliminar) los demás usuarios del módulo del Sistema Integral de Producción.

- Reportar producción: Los usuarios podrán generar reportes de producción dentro del sistema.

- Gestión de registros de producción: Los usuario con rol de trabajador podrán modificar o  eliminar su propio registro de producción. Los usuarios con rol supervisor o administrador podrán modificar o eliminar los registros de producción de cualquier usuario.

- Registro de almacén: Los usuarios con rol supervisor podrán generar, modificar o eliminar registros de materias primas que existan en almacén.

- Visualización del stock en almacén: Los usuarios con rol operador, supervisor y administrador podrán visualizar el stock existente en almacén.

- Visualización de la producción: Los usuarios con rol supervisor podrán visualizar la producción del día y turno seleccionados.

- Programación de ordenes: Los usuarios programadores podrán subir la programación de las ordenes que se deberán de producir en los centros de producción de la empresa.

- Modificación de productos: Los usuarios administradores podrán realizar modificaciones en las especificaciones descritas en el Sistema Integral de Producción sobre los productos que genera la compañía.

### Requerimientos no funcionales

- El sistema deberá autenticar a los usuarios mediante un nombre de usuario y contraseña antes de permitir el acceso a cualquier módulo.
- El sistema deberá implementar control de acceso basado en roles (administrador, supervisor, operador y programador).
- El sistema deberá soportar múltiples usuarios conectados simultáneamente sin degradación crítica del servicio.
- El sistema deberá garantizar la integridad de los datos almacenados evitando duplicidad o pérdida de información.
- El sistema deberá ser accesible desde equipos de escritorio utilizados dentro de la empresa.

## Casos de uso

## Arquitectura de software

### Estructura backend

### Estructura frontend

## Esquema de bases de datos

## Modulos del software
