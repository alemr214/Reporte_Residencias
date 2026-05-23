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

...

## Arquitectura de software

La arquitectura de software es la forma en la cual un sistema informático se diseña estructural-mente durante su desarrollo con el propósito de darle responsabilidades a cada sección declarada y establecer la forma en la cual estas se comunican entre si.

Existen diferentes arquitecturas de software que han nacido de necesidades específicas durante el desarrollo del mismo o dependiendo de la naturaleza para lo que fue creado el software, estas soluciones han sido probadas por diferentes equipos y se han demostrado su eficacia siendo adoptadas a lo largo de la historia.

En el caso de la arquitectura de software escogida para los módulos del Sistema Integral de Producción se tienen la arquitectura de N-Capas (Multi-layer architecture) para el apartado del backend y para la parte del frontend una arquitectura basada en componentes (Component-Based Architecture) siendo este último más un patrón de organización, pero adoptada a aplicaciones web modernas.

### Estructura backend

En la estructura del backend podemos encontrar la arquitectura de N-capas, estas separan la responsabilidad de cada apartado del backend y el "modelo de negocio" establecido para este sistema de acuerdo que no se mezclen soluciones entre cada capa y el flujo de la información y procedimientos sea en un sentido determinado teniendo que pasar por cada capa involucrada para un tratamiento o procesamiento de la información o procesos para llevar a un resultado esperado.

Dentro de las capas que podemos denotar especialmente en esta solución son 4

1. La capa de controlador (controller).
2. La capa de servicio (servicio)
3. La capa de negocio (business).
4. La capa de datos (data).

Cada sigue su funcionamiento pasando la información hacia la siguiente capa, las utilidades de estas son:

#### Controller

Es aquella capa que se encarga de recibir todas las solicitudes HTTP hechas desde el cliente siendo el primer frente en el cual se realiza la conexión entre el backend y el frontend

#### Service

Una vez obtenida la información de la capa de controlador, dependiendo de esta misma es que redirige la información hacia una parte de la business u a otra de la siguiente capa, esta gestiona que lógica de negocio es la más apropiada para manejar esta información

#### Business

En esta capa está toda la gestión procedimental (el modelo de negocios) de como el sistema maneja la información.

#### Data

Esta capa maneja el acceso a los datos de la base de datos, se encarga de guardar y obtener datos directamente desde la base de datos siendo el conector entre la DB y el backend.

### Estructura frontend

En el apartado del frontend el patron de arquitectura basado en componentes muestra la independencia y utilidad por cada apartado dentro del sistema web, teniendo los siguientes apartados.

#### Components

Refiere a la parte en donde se estructuran componentes atómicos los cuales son reutilizados en diferentes partes de los módulos del SIP, estos esquematizan una utilidad que puede cambiar (su estado) dependiendo de la necesidad donde se implemente

#### Hooks

Son los procesos que permiten modificar la funcionalidad a través de la interacción con el usuario que manipula el componente una vez integrado en su módulo correspondiente y que son generales .

#### Utils

Son funciones de utilidad como cálculos de fechas, formateo de información, ordenamientos de datos, entre otras funciones varías que se utilizan en diferentes componentes para evitar duplicidad de código

#### Styles

Son los archivos de estilos en formato CSS que modifican el estilo de los componentes.

#### Views

Son la contrucción de vistas completas que integran los componentes generando una interacción más compleja las cuales contienen los flujos de información por los cuales los usuarios interactuan.

Adicionalmente, dentro de los apartados de "Components" pueden contener cada componente una carpeta de "Hooks" que cumple con el mismo propósito que la carpeta de hooks general solo que estas contienen las funcionalidades específicas para un componente basado en sus requerimientos.

## Módulos del software
