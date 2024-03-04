# LAB 5.1: Aplicación 

## Capítulo 1: Creación proyecto Spring Boot

## Tutorial: Creación de un Proyecto Spring Boot con un Servicio "Hello World"

### 1. Introducción a Spring Boot
Spring Boot es un marco de trabajo de código abierto que simplifica el desarrollo de aplicaciones Spring independientes y de calidad de producción. Está construido sobre el Spring Framework y proporciona una variedad de herramientas, bibliotecas y convenciones para simplificar la configuración y el despliegue de aplicaciones.

### 2. Creación del Proyecto
Para comenzar, sigue estos pasos:

1. **Genera un nuevo proyecto Spring Boot**:
   - Utiliza la herramienta **Spring Initializr** en línea o tu IDE preferido (como IntelliJ IDEA o Eclipse).
   - Selecciona las siguientes opciones:
     - **Group**: net.codejava
     - **Artifact**: SpringBootHelloWorld
     - **Dependencies**: Elige "Web" para habilitar el manejo de solicitudes HTTP.
![](https://github.com/AlejoCNYT/cvds-LAB-5.1/blob/main/img/Captura%20de%20pantalla%202024-02-29%20172654.png)
2. **Estructura del Proyecto**:
   - Descomprime el archivo descargado en una carpeta.
   - Abre el archivo `pom.xml` y elimina la dependencia `spring-boot-starter-test`.
![](https://github.com/AlejoCNYT/cvds-LAB-5.1/blob/main/img/Captura%20de%20pantalla%202024-02-29%20181206.png)
### 3. Creación del Controlador
1. **Crea un controlador**:
   - Abre la clase `SpringBootHelloWorldApplication.java`.
   - Agrega la anotación `@RestController` a la clase.
   - Crea un método llamado `home()` con la anotación `@RequestMapping("/")` que devuelve un mensaje "Hello world Spring Boot".

2. **Ejecuta la Aplicación**:
   - Ejecuta la aplicación usando el comando `mvn spring-boot:run`.
   - ![](https://github.com/AlejoCNYT/cvds-LAB-5.1/blob/main/img/Captura%20de%20pantalla%202024-02-29%20190218.png)
   - Accede a ella desde el navegador en [http://localhost:8080/](http://localhost:8080/).
     ![](https://github.com/AlejoCNYT/cvds-LAB-5.1/blob/main/img/Captura%20de%20pantalla%202024-02-29%20190327.png)
3. **Personalización del Mensaje**:
   - Modifica el método `home()` para usar etiquetas HTML y agrega otro método con `@RequestMapping("/new")` que devuelva otro mensaje.

### 4. Empaquetado y Ejecución
1. **Empaqueta la Aplicación**:
   - Ejecuta `mvn package` para crear un archivo JAR ejecutable.
     ![](https://github.com/AlejoCNYT/cvds-LAB-5.1/blob/main/img/Captura%20de%20pantalla%202024-02-29%20193557.png)
2. **Ejecuta la Aplicación**:
   - Ejecuta la aplicación con el comando `java -jar target/SpringBootHelloWorld-0.0.1-SNAPSHOT.jar`.
     ![](https://github.com/AlejoCNYT/cvds-LAB-5.1/blob/main/img/Captura%20de%20pantalla%202024-02-29%20194634.png)

¡Listo! Ahora tienes un proyecto Spring Boot con un servicio "Hello World".
