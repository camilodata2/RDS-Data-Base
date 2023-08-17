# 🤤 BASE DE DATOS BDS
Amazon Relational Database Service (RDS) es un servicio de base de datos en la nube ofrecido por Amazon Web Services (AWS). RDS facilita la creación, operación y escalabilidad de bases de datos relacionales en la nube sin que tengas que preocuparte por la administración de la infraestructura subyacente.Cuenta con los motores de bases de datos relacionales conocidos por mucho como.

1. [MySQL](#id1)
2. [Aurora](#id2)
3. [MariaDB](#id3)
4. [Oracle](#ide4)
5. [PostgreSQL](#ide5)
6. [MicrosoftSQLserver](#id5)
 
## Caracteristicas y beneficios 
 Como se mensiono anteriore mente AWS es compatibilidad con Múltiples Motores de Bases de Datos: Amazon RDS admite varios motores de bases de datos populares, como MySQL, PostgreSQL, MariaDB, Oracle Database, Microsoft SQL Server y Amazon Aurora.

  Gestión Automatizada: RDS administra tareas de administración como aprovisionamiento de hardware, parcheo de software,
  copias de seguridad automatizadas, recuperación ante fallos y monitoreo.

  Escalabilidad: Puedes escalar verticalmente (cambiando el tamaño de la instancia) y horizontalmente (mediante réplicas de lectura y clústeres de Aurora)
  según tus necesidades de rendimiento y capacidad.

  Disponibilidad y Tolerancia a Fallos: RDS ofrece opciones para réplicas de lectura, backups automatizados y alta disponibilidad a través de múltiples 
  zonas de disponibilidad.

  Seguridad: Amazon RDS proporciona encriptación de datos en reposo mediante AWS Key Management Service (KMS), y también admite SSL/TLS 
  para encriptación de datos en tránsito.

  Facilidad de Uso: Puedes gestionar tus bases de datos a través de la consola de administración de AWS, la línea de comandos de AWS (CLI) y SDKs.
  También puedes utilizar herramientas de gestión de bases de datos de terceros.

  Automatización de Tareas Comunes: RDS ofrece características como snapshots automáticos, copias de seguridad y restauraciones, 
  lo que facilita la recuperación en caso de errores.

  Flexibilidad de Implementación: Puedes elegir entre diferentes tipos de instancias de base de datos según tus requisitos de rendimiento y 
  carga de trabajo.

Amazon Aurora:

Además de los motores de bases de datos tradicionales, Amazon RDS ofrece Amazon Aurora, un motor de bases de datos compatible con MySQL y PostgreSQL 
que se desarrolló específicamente para la nube. Aurora ofrece un rendimiento y una disponibilidad excepcionales y puede ser una opción sólida 
para cargas de trabajo críticas.

En resumen, Amazon RDS es una solución poderosa y flexible para alojar bases de datos relacionales en la nube, lo que puede simplificar 
la administración y reducir la carga operativa en comparación con la gestión de bases de datos en entornos locales.

### 😲 Crear una instancia de base de datos

Para crear una instancia de base de datos en Amazon RDS, sigue estos pasos:

  Iniciar Sesión en AWS:
  Accede a tu cuenta de Amazon Web Services (AWS) usando tus credenciales en la consola de administración de AWS.

  Navegar a Amazon RDS:
  Una vez dentro de la consola de administración de AWS, busca y selecciona "RDS" en la lista de servicios disponibles.

  Crear una Nueva Instancia de Base de Datos:
  En el panel de control de Amazon RDS, haz clic en el botón "Create database" (Crear base de datos) para iniciar el proceso de creación.

  Elegir el Motor de Base de Datos:
  Selecciona el motor de base de datos que deseas usar, como MySQL, PostgreSQL, Oracle, SQL Server o Amazon Aurora.

<img src="https://docs.aws.amazon.com/es_es/AmazonRDS/latest/UserGuide/images/tutorial-create-mysql.png" alt="Texto alternativo" width="300"/>


  Elegir una Opción de Uso:
  Selecciona si deseas crear una base de datos "Standard Create" (Creación estándar) o si deseas restaurar desde una copia de seguridad existente o una instantánea de base de datos.

  Configuración de la Instancia:
  Completa los siguientes pasos para configurar la instancia de base de datos:
  Templates: Elige un "DB instance size" (Tamaño de la instancia de la base de datos) basado en tus necesidades de rendimiento y capacidad.
  Settings: Proporciona un nombre de instancia, un nombre de usuario y una contraseña para la base de datos.
  DB instance identifier: Asigna un nombre único a tu instancia.
  Master username: Establece el nombre de usuario del administrador de la base de datos.
  Master password: Configura la contraseña para el administrador de la base de datos.

<img src="https://docs.aws.amazon.com/es_es/AmazonRDS/latest/UserGuide/images/Tutorial_WebServer_Settings.png" alt="Texto alternativo" width="200">


<img src="https://docs.aws.amazon.com/es_es/AmazonRDS/latest/UserGuide/images/Tutorial_WebServer_DB_instance_micro.png" alt="Texto alternativo" width="200">

  También puedes configurar opciones avanzadas como el almacenamiento, la configuración de red, la seguridad y más.

  Configuración de la Red:
  Configura la red y las opciones de seguridad para la instancia de base de datos. Puedes elegir una VPC existente o crear una nueva.
<img src="https://docs.aws.amazon.com/es_es/AmazonRDS/latest/UserGuide/images/Tutorial_WebServer_Connectivity.png " alt="Texto alternativo" width="300">

<img src="https://docs.aws.amazon.com/es_es/AmazonRDS/latest/UserGuide/images/Tutorial_WebServer_Endpoint_Port.png " alt="Texto alternativo" width="300">

  Opciones de Base de Datos Adicionales:
  En esta sección, puedes configurar opciones como copias de seguridad automatizadas, configuración de mantenimiento, monitoreo y más.

  Resumen:
  Revisa la configuración que has proporcionado y asegúrate de que todo esté correcto. Puedes modificar cualquier configuración si es necesario.

  Crear la Instancia:
  Una vez que hayas revisado y confirmado la configuración, haz clic en "Create database" (Crear base de datos). 
  La instancia de base de datos comenzará a crearse. Puedes monitorear el estado de creación desde la consola de administración de RDS.



Después de que la instancia de base de datos se haya creado correctamente, podrás conectarte a ella utilizando las credenciales que configuraste y comenzar a administrar tus bases de datos en la nube. Recuerda que los detalles específicos pueden variar según el motor de base de datos que elijas y las opciones de configuración que prefieras.

#### 🤓 Conexion grafica a la base de datos 

Si deseas conectarte a una base de datos alojada en Amazon RDS de manera gráfica, puedes utilizar herramientas de administración de bases de datos 
que te permitan establecer una conexión visual con la base de datos. Aquí hay un ejemplo de cómo hacerlo utilizando la herramienta MySQL Workbench 
para conectarte a una instancia de base de datos MySQL en Amazon RDS:

  Descargar e Instalar MySQL Workbench:
  Si aún no tienes MySQL Workbench instalado en tu computadora, descárgalo e instálalo desde el sitio web oficial de MySQL: https://www.mysql.com/products/workbench/

  Abrir MySQL Workbench:
  Una vez instalado, abre MySQL Workbench en tu computadora.

  Crear una Nueva Conexión:
  En la pantalla de inicio de MySQL Workbench, haz clic en el botón "New Connection" (Nueva conexión) en la parte inferior izquierda.
  Ingresa un nombre para la conexión.
  Configura los siguientes detalles:
  Hostname: La dirección de la instancia de RDS (puede ser el endpoint proporcionado en la consola de RDS).
  Port: El puerto de la base de datos (por defecto es 3306 para MySQL).
  Username: El nombre de usuario de la base de datos.
  Password: La contraseña del usuario de la base de datos.
  Haz clic en "Test Connection" (Probar conexión) para asegurarte de que la configuración sea correcta y puedas conectarte.

  Conectarse a la Base de Datos:
  Si la prueba de conexión es exitosa, haz clic en "OK" para guardar la configuración de la conexión. Luego -
  selecciona la conexión que creaste y haz clic en "Connect" (Conectar).

  Explorar y Administrar la Base de Datos:
  Una vez conectado, podrás explorar la estructura de la base de datos, ejecutar consultas SQL y realizar diversas operaciones de 
  administración de datos de manera gráfica en MySQL Workbench.

Recuerda que, si estás utilizando un motor de base de datos diferente, como PostgreSQL o SQL Server, también hay herramientas de administración gráfica específicas 
para esos motores que puedes utilizar de manera similar.Existen opciones como JetBrains DataSpell o DBeaver para la administración de bases de datos. 
No obstante, te recomiendo utilizar DBeaver debido a su gratuidad. Mientras que JetBrains DataSpell requiere un pago.
Ofrece una capa gratuita durante dos meses. Sin embargo, si eres estudiante universitario, puedes acceder de manera ilimitada utilizando 
tu correo institucional .

Ten en cuenta que la configuración específica puede variar según el motor de base de datos que estés utilizando y las políticas de seguridad que hayas configurado en Amazon RDS. Asegúrate de consultar la documentación relevante para obtener instrucciones precisas sobre cómo establecer la conexión gráfica a tu base de datos específica.

##### 🤫 Conexión por consola a nuestra base de datos mediante SSH
Para esta sección, se requiere conocimiento en programación en bash. Sin embargo, no te preocupes, ya que tengo un repositorio muy completo en mi GitHub donde explico a fondo el tema de la programación en bash. Cubro cómo programar en bash, cómo utilizar bucles en bash y cómo funcionan. Además, he incluido un par de ejemplos muy interesantes.

También, les proporcionaré el enlace a mi blog, donde hablo en detalle sobre AWS EC2 y otras características interesantes de este servicio de AWS. Si desean obtener más información, les invito a visitar el blog a través de este enlace

Si deseas conectarte a una instancia de base de datos alojada en Amazon RDS mediante SSH, sigue estos pasos:

  Habilita el Acceso a través de SSH en Amazon RDS:
Antes de conectarte mediante SSH, asegúrate de que has habilitado la opción de acceso público y configurado el grupo de seguridad de tu instancia de RDS para permitir conexiones SSH. Para ello, debes configurar la opción "Publicly accessible" (Acceso público) como "Yes" (Sí) al crear o modificar tu instancia.

  Obtén las Credenciales de Acceso:
  Asegúrate de tener las credenciales de acceso SSH a la instancia de Amazon RDS. Esto generalmente incluye la dirección IP pública o DNS del servidor y la clave SSH que utilizas para conectarte.

  Abre una Terminal en tu Computadora:
  Abre una terminal en tu sistema operativo. Puedes usar el terminal en Linux o macOS, o una herramienta como PuTTY si estás en Windows.

  Conéctate al Servidor de Amazon RDS:
  Utiliza el comando SSH para conectarte al servidor de Amazon RDS. El comando tendrá la siguiente estructura:

    

1. [ssh -i /ruta/a/tu/llave-ssh.pem usuario_ssh@direccion_ip_o_dns](#ide1)

    /ruta/a/tu/llave-ssh.pem es la ruta a la clave SSH que utilizaste para acceder.
    usuario_ssh es el nombre de usuario SSH que configuraste.
    direccion_ip_o_dns es la dirección IP pública o el DNS de tu instancia de RDS.

###### Ejemplo



2.    [ssh -i /ruta/a/mi-llave.pem ec2-user@54.123.45.678](#ide2)

  Conéctate a la Base de Datos:
  Una vez conectado al servidor mediante SSH, puedes usar el cliente de línea de comandos de la base de datos (como mysql para MySQL o psql para PostgreSQL) para conectarte a la base de datos.

  Desconéctate al Finalizar:
  cuando hayas terminado de trabajar, asegúrate de desconectarte correctamente del servidor mediante el comando exit.

Recuerda que, además de habilitar el acceso público y configurar el grupo de seguridad, también debes asegurarte de que el usuario SSH que utilizas tenga los permisos adecuados para acceder a la instancia de RDS. Si tienes dudas o problemas, siempre es recomendable consultar la documentación oficial de Amazon RDS o buscar asistencia específica.
