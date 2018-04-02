Windows Internal. Part 1 Part 2 

# JAva Enterprise

- **Plataforma introducda en Junio 1999**.
- **J2SE **- Java 2 Standard Edition
	- Java for the desktop / workstation.
	- http://java.sun.com/j2se
- **J2ME **- Java 2 Micro Edition
	- Java for the consumer device
	- http://java,sun.com/j2me
- **J2EE **- Jaa 2 Enterprise Edition
	- Java for the servers
	- http://java.sun.com/j2ee

IBM z OS -> For Mainframes // File Sistem = DB2 for Z // Connected with emulators 5250
IGM I -> For Mini // File Sistem = DB2 for I

Espeficiacion no producto.

Enfoque basado en componentes apra el disenio. desrrollo, montaje y  despkiegue de aplicaciones empresariales.

Spring -- Rob Johnson Leer.

--- 

Define el estandar para el desarollo de aplicaciones empresariales multi-capas.
Simplifica las aplicaciones empresariales por:
- Basandolas en componentes modulares estandar
- Proveyendo un conjunto completo de serivcios para estos componentes
- Manejando de muchos detalles de comportamiento de la aplicacion automaticamente, sin necesidad de programacion compleja.

### Caracteristicas
- Especificaciones de Api y tecnologias
- Platadorma de Development y Deplyment
- Implementaciones Estandart y production quality
- Compatibility Test Suit
- J2EE Brand
- J2EE Blueprints
- Codigos de ejemplos

### Soluciones Abiertas y Estandar
- Un modelo de "Componentes y contenedores" en el que lso servicios del sistema son provistos por los contenedores en un lugar bien definido y como estandar de la industria.
- J2EE es que el estandar que tambien proporciona la portabilidad de codigo ya que se basa en la tecnologia Java, y la API de Java basada en estandares de programacion.

### Valor para los Desarrolladores
- Puede utilizar cualquier implementacion de J2EE para el desarrollo y despliegue
	- Utilice la aplicacion estandar de calidad de produccio que es gratuito para el desarrollo yd espligue.
	- Utilice producciones comerciales de alta gama J2EE para escalabilidad y tolerancia de fallos.

- Gran cantidad de recursos de la comunidad j2EE
	- Muchs libros de J2EE articulos, tutoriales codifos de calidad que puede utilizar, directrives sorne mejores practicas, aptrones de diseno, etc

-Utilziar componentes de negocio de terceras partes.

### Ventajas

- Provee una arquitectura completa para dearrollo.
	- Sistemas distribuidos, con persistencia de objetos, manejo de sesiones, transacciones, etc...

- Separa el codigo tecnico y el especifico de la aplicacion
	- Deplayment descriptors
	- Container-Managed Persistance

### Desventajas

- Tecnologia muy compleja
	
- Diversos Errores ocurren solo en el runtime
	- Se requieren diversos pasos para tener la aplicacion corriendo
		- Compilacion
		- Empaquetado
		- Deployment
		- Ejecutar la aplicacion

### Enterprise Java Beans

Tres tipos de EJBs 
- Entity BEans
	- Persisten datos del negocio de manera OO
	- 2 Tipos: CMO y BMP
	- Acceso sictronico utilizando RMI-IIOP

- Session Beans
	- Modelan procesos de negocio
	- 2 tipos:  Statefull (Permiten guardar estados)  vs Stateless	
	- Acceso sincronico utilziando RMI-IIOP

- Message Driven Beans (Administracion de colas de mensajes)
	- Similares a los Session Beans pero proveen acceso asicronico por medio de JMS

### Uso de los EJBs
- BEans se registran en un repositorio llamando JNDI
	- Se busca por nombre

- Se acceden a lso beans por medio de sus interfaces
	- Remote interface
		- Expone los servicios a nivel de aplicacion del bean
			- getName().getCurstomerList()
	- Home interface
		- Interface para adminsitrar las instancias de los Beans
			- create().findAll().findByPrimaryKey()

- Cada tipo de Bean posee Home y Remote Iterface

### Seassion beans

- Son utilziados apra realizar tareas de negocios
- Por lo general sus mtodos corresponden a casos de usos  y utilizan los serivicos de uno o mas Entity Beans
	- Ejemplo: realizarCompra()
- Session Beans encampsulan Entity Beans.
- Session Beans representa laFachada.

### Servlets
- Clases Java especiales localizadas en els ervidor
- Utilizados apra la implementacion de interfaces web dinamicas
	- Generan contenido dinamico en vez de estatico.

- Los clientes invocan un servlet utilizando un request HTTP.
	- El contenedor web reenvia el pedido al servlet
	- El servlet realiza el proceso y genera el contenido
	- El contenedor web devuelve la respuesta al cliente

- Los servlets pueden acceder a lso componentes del contenedor EJB (Session Ebans, Entity Beans, Message Beans)
- Una calse que impelementa la interface HttpServlet
	- GET --> doGet(...)
	- POST --> doPost(...)
	- publix String doGet(...)
	
	
Common Gateway Interface 

### JSP

- Paginas html especiales localizadas en el servidor web
- Pueden ser html comun y se puede incluir algo de Java
	- Apropiadas para crear interfaces de usuario
	- No se recomiendo incluir logica de negocio.
- JSPs se transforman en Servlets en tiempo de ejecucion
- POsee Tangs especiales
	- <% %> Se peude insertar codigo de java entre estos tags
	- <%@ %> Se insertan directivas con tags
	- <jsp:forward> Se pueden enviar in redireccionamiento
- Importante
	- JSP tags, nombre, parametros, etc con case-sensitive

### Tecnologias
- Web Tier: Servlets and JSP
- Enterprise tier: EJB
- Data Acces Layer: JDBC, JCA
- JMS
- JTA
- JavaMail
- XML and Web servicesL JAXP, JAX-RPC, JAXR
- JNDI (Cuando inician aca se registran) // Java Naming Directory Interface

### Software Project Management

- Problemas
	- Los proyectos grander por lo general contienen gran cantidad de sub-proyectos / modulos/ librerias (Dependencias)
	- Se vuelve incomprensble y desprolijo si no se sigue um principio comun
	- Es muy complejo y tedioso construit rodos los proyectos.

- Solucion preferida
	-Utilizar una herramienta de administracon de proyectos (maven)
	- Maven proporciona ayuda en varios aspectos
		- Procesos de Build
		- Estructura de proyectos		
		- Administracion de Dependencias
		- Acceso a informacion y documentacion

~/.ms/repository --> Local Cache

```java

public class Ciente S {
}


```

### Apache Maven 2

- Build Process
	- Project Object Model (POM) - Archivo XML
	- COntiene informacion del proyecto y detalles de configuracion
		- Utilzado para construit  desplegar el proyecto
		- Administrar dependencias del proyecto
		- Es posible ejecutar comandos (goals)
		- Posee un arquitectura extensible de plugins
		- Adminsitra servicios de metadatos

``` bash

mvn releare prepare / prferm

```

> Scopes
>	Compile
>	test
>	runtime --- Dependencias necesarias al momento de ejecucion y no de compilacion
>	provided --- Necesito para compilar, ejecutar, pero no dentro del empaquetado final por que alguien mas me lo va a proveer



### Ciclo de vida Construccion y Fases
- El ciclo de vida de construccion es el proceso de construccion e implementacion de un artefacto
- La fase es una etapa en este ciclo de vida
- Las fases mas importantes son
	- Validacion
	- Compilacion
	- Prueba (Test)
	- Empaquetado (Package)
	- Instalacion
	- Implementacion (Deploy

### Estructura de directorios estandar
- Ventajas
	- Rapida adaptacion a para los derarolladores familiarizados con Maven2
	- No se pierde tiempo reiventando una estructura de directorios

src/main/java
src/main/resources
src/main/filters
src/main/config
src/main/webapp
src/test/java
src/test/resources
src/test/filters
src/site


### Administracion de Dependencias
- Dependencias: Librerias de software de terceras partes o propias (Jar -War)
- La administracion de dependecnias es tediosa en lso grandes proyectos
	- Dependencia de dependencias (Arbol o grafo de dependencias)
	- Errores en tiempo de ejecucion por falta de librerias

### Vida sin Maven
- Enfoque manual:
	- Descargar las libreris y replicarlas en lso proyectos
		- Ineficiente cuando el tamanio de librerias aumenta
		- Dificil d ellevar versiones de librerias
		- El checkout de proyecto es lento por necesitar descargas las librerias

- Enfoque Adminsitrado:
	- utilizar un repositorio de dependencias
		- Lugar comun donde almacenar y buscar librerias
			- Solo una copia existe
			- Se almacenan fuera del proyecto
		- Las dependencias se definen en el POM

``` xml
<dependencies>
	<dependency>
		<groupid>commons-logging</groupid>
		<artifactld>commons-loggin</groupid>
		<version>1.3</version>
	</deependency>
<dependencies>
```

### Repositorios
- Repositorios Remotos
	- Proveen lso artefactos para dscargas
		- http://repo1.maven.org
		- Repositorio central de MAven

- Repositorio local
	- copia local de artefactos descargados
	- USER_HOME/.m2/repository

### Dependencias Transitivas

- Maven lee los POM de las dependencias y las agrega automaticamente como librerias requeridas
- No hay limite en el numero de niveles de dependencias.

### Crear un proyecto Web

mvn archetype:generate -DgroupId=ar.edu.utn.free.cs -DartifactId=webapp1

### Java Persistece API
- Api de persistencia desarrollada para la plataforma Java EE
- JPA fue originada a partir del rabajo del JSR 220.
- Ha sido incluida en el estandar EJB3
	- La API en si misma, definia en javax.persistence.package
	- La Java persistence Quesy Languaje (JPQL)
	- Metadatos Objeto/relacional

SET ----> HashSet
LIST----> ArrayList
	> Vector
MAP ----> HashMap
TREE

Leer sobre Hash

JUANCHUMENI!

MENICHUWAN

#### Siete pasos
- Cargar el friver. Debe estar en memoria al momento de ejecutar la app
- Indicar donde esta base de datos que intento conectarme, se debe cosntruitr la URL de conexion
	- jdbc:mysql://localhost/dacs?
- Establecer la coneccion, tengo la URL, Credenciales
- Crear Statement
- Ejecutar un query stm.executeQuery(query) 
- Procesar los resultados
- Liberar los recursos 

Estructura de try catch finally
