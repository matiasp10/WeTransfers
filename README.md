# WeTransfers

Este proyecto está enfocado en resolver las necesidades de una empresa que maneja transferencias cripto intraempresariales. El objetivo principal de la página es ofrecer a los clientes una plataforma donde puedan gestionar sus fondos en dólares cripto, ver sus transacciones y realizar nuevas solicitudes de cotización para transferencias, todo dentro de una interfaz sencilla y eficiente. Por otro lado, también proporciona a los administradores un panel donde pueden gestionar las cuentas de los clientes y controlar el flujo de las transferencias de manera segura y efectiva.

![image](https://github.com/user-attachments/assets/374b63d5-a504-4d88-bad3-e8a18b2877d8)

## Funcionalidades clave

Para entender las funcionalidades las separe en las que queria para sus clientes y las que queria para administrar.

### Clientes

- **Saldo en dólares cripto**: Los clientes pueden ver cuántos dólares cripto tienen disponibles en sus cuentas. Esta información se actualiza en tiempo real a medida que se hacen transferencias.
- **Historial de Transferencias**: Se les muestra un registro de las últimas transferencias que han realizado, detallando las cantidades, fechas y direcciones cripto involucradas.
- **Solicitar cotización**: Los usuarios tienen la opción de solicitar una cotización para realizar una nueva transferencia. Esto implica que el cliente elige la cantidad de dólares cripto que quiere transferir y la plataforma genera una cotización basada en las tasas actuales del mercado o criterios establecidos por la empresa.

### Panel de administración

- **Consulta de todas las operaciones**: El administrador tiene acceso a un panel donde puede ver todas las operaciones realizadas por los clientes, desde las transferencias históricas hasta las solicitudes de cotización pendientes.
- **Control de saldos**: El administrador tiene la capacidad de ajustar el saldo inicial de las cuentas de los clientes, lo que le permite modificar los valores de dinero cripto almacenados en el sistema cuando sea necesario.
- **Generación de nuevas transferencias**: Desde el panel administrativo, también es posible crear nuevas transferencias para los clientes. Esto es útil en situaciones donde se requiera un procesamiento manual o ajustes especiales.
- **Responder a cotizaciones**: Cuando los clientes solicitan una cotización para una transferencia, el administrador puede revisar la solicitud y responder con el monto estimado o cualquier otra información necesaria.

![image](https://github.com/user-attachments/assets/5898dc2f-4fc8-4640-8a4d-09499d1de44f)

## Proceso de desarrollo

El proceso de desarrollo de esta página web implicó un enfoque cuidadoso tanto en la planificación de las funcionalidades como en la selección de las tecnologías adecuadas para construir una plataforma escalable y segura. A continuación se detalla el flujo del desarrollo:

1. **Recolección de Requisitos y Análisis**: Primero, trabajé estrechamente con mi cliente para entender las necesidades específicas de la plataforma. La prioridad era asegurarse de que los clientes pudieran tener control y visibilidad de sus fondos en dólares cripto y, al mismo tiempo, proporcionar al administrador herramientas efectivas de gestión.
Después de definir los requisitos funcionales y no funcionales, diseñé la arquitectura del sistema, definiendo cómo se organizarían las bases de datos, las vistas de cliente y las herramientas administrativas.

2. **Diseño del Sistema**: Para el diseño visual, decidí utilizar Tailwind CSS, una herramienta que permite crear diseños de manera rápida y flexible. Me permitió mantener un sistema de diseño coherente, con componentes reutilizables, pero sin perder la libertad de hacer ajustes personalizados cuando fuera necesario.
Utilicé ShadCN para implementar componentes visuales que siguieran las mejores prácticas de diseño moderno. Esto ayudó a que la interfaz fuera intuitiva y atractiva para los usuarios, sin perder funcionalidad.

3. **Desarrollo de la Funcionalidad del Cliente**: En esta etapa, implementé el panel de clientes. El uso de Next.js permitió la creación de una aplicación de una sola página (SPA) eficiente, donde la navegación y actualización de datos ocurre sin necesidad de recargar la página completa.
Usé TypeScript para asegurar que el código fuera sólido, evitando errores comunes asociados con el manejo de datos dinámicos, como las cuentas y transacciones cripto.
La lógica detrás de la solicitud de cotizaciones se construyó con un sistema que interactúa con la base de datos para registrar las solicitudes, calcular las tasas de conversión cripto y mostrar el resultado al usuario.

4. **Desarrollo del Panel de Administración**: El panel de administración es una herramienta crítica para que los operadores del sistema puedan controlar los fondos y las transacciones. Aquí, Next.js también jugó un papel importante en la creación de una interfaz interactiva, donde los administradores pueden gestionar las cuentas de los clientes y ver las operaciones en tiempo real.
ClarkJS se utilizó para manejar la validación y manipulación de datos. Esto ayudó a asegurar que las operaciones del administrador, como cambiar saldos o procesar cotizaciones, fueran precisas y seguras.
DrizzleORM se integró para gestionar las consultas a la base de datos. Opté por SQLite como base de datos debido a su simplicidad y buen rendimiento para esta aplicación. Esto permitió que todas las operaciones del sistema fueran rápidas y eficientes.

5. **Bases de Datos y Seguridad**: El sistema almacena todas las transacciones y los detalles de las cuentas en una base de datos Turso que, junto con SQLite, maneja las operaciones internas de manera segura y escalable.
La elección de Turso y SQLite como bases de datos se basó en la naturaleza ligera del proyecto y la necesidad de tener una solución que pudiera ser rápidamente desplegada sin comprometer el rendimiento ni la seguridad.

6. **Testing y Depuración**: Durante la fase de desarrollo, implementé pruebas continuas utilizando TypeScript para asegurar que todos los flujos funcionaran correctamente y evitar posibles problemas con los datos cripto.
También utilicé herramientas de debugging integradas en Next.js para resolver problemas de rendimiento y asegurar que la aplicación fuera rápida, tanto en la parte del cliente como en el lado del administrador.

![image](https://github.com/user-attachments/assets/c8b96820-5292-41cd-ac7e-208f3270006a)

## Tecnologias utilizadas

- **TypeScript**: Utilizado para proporcionar tipado estático al código, lo que reduce errores y hace que el desarrollo sea más robusto y predecible.
- **Tailwind CSS**: Para el diseño rápido y personalizado, haciendo uso de clases utilitarias que me permitieron tener control total sobre el aspecto visual de la página.
- **ShadCN**: Usado para implementar componentes reutilizables, asegurando que la interfaz de usuario sea limpia y moderna.
- **Turso y SQLite**: Estas bases de datos ligeras fueron elegidas por su simplicidad, rendimiento y fácil manejo, especialmente en una plataforma donde las transacciones y datos deben almacenarse de manera segura.
- **DrizzleORM**: Un ORM que me ayudó a gestionar de manera eficiente las operaciones con las bases de datos, asegurando que las consultas fueran seguras y rápidas.
- **ClarkJS**: Para la validación de datos, asegurando que los datos manipulados sean correctos y estén bien formateados.
- **Next.js**: Como framework principal, permitió construir una aplicación rápida y escalable, aprovechando tanto las rutas estáticas como dinámicas, y brindando una excelente experiencia de usuario.
