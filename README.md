
# Java Getting Started

Repositorio para que puedas empezar ya mismo a programar en Java.

## Herramientas
- JDK: OpenJDK 11
-   Java-building-tool: Maven 3.6.3

### Artefactos definidos en el pom.xml:

- JUnit 5.4.0 - Unit testing framework
- Mockito  3.3.0  - Mock testing framework
- JaCoCo  0.8.5 - Java Code Coverage Tool
- maven-compiler-plugin 3.8.0
- maven-surefire-plugin 3.0.0-M3

## Instalación

1. Hacer un fork al repositorio.
![make-fork-repo](https://help.github.com/assets/images/help/repository/fork_button.jpg)
2.  Activar la integración continua del forked repo en el apartado de Actions 
![active-github-actions](https://raw.githubusercontent.com/LuisCusihuaman/java-getting-started/master/docs/active_fork_actions.png)


## Uso

1. Clonar el repositorio

    `    $ git clone https://github.com/TU-USUARIO/java-getting-started.git`

    `    $ cd java-getting-started`
 2. Resolver las dependencias establecidas en el pom.xml

    `    $  mvn dependency:resolve `

 3. En IntelliJ IDEA cuando abran el repo, en la seccion de Maven:
		Reimport All Maven Projects 
		![idea-maven-import-proyect](https://raw.githubusercontent.com/LuisCusihuaman/java-getting-started/master/docs/maven_import.png)
 4.  Codear!!
 - Modelos en: /src/main/java/poo.coders 
 - Tests en: /src/test/java/poo.coders 
 
## Ejemplo
_Los resultados de coverage son ficticios, solo con el fin de mostrar un ejemplo._
1. Compilar con Maven los modelos y sus tests

    `    $ mvn test-compile`
2. Correr los test, generará el reporte de coverage en **target/site/jacoco/index.html**

    `    $ mvn test`

![make-a-report](https://raw.githubusercontent.com/LuisCusihuaman/java-getting-started/master/docs/jacoco_coverage_report.png)

_Jacoco calculara el coverage de los test de su repositorio._

## Integracion de IntelliJ IDEA con Jacoco
Por defecto IDEA utiliza su propia herramienta de code coverage, se debe cambiar en la configuracion de los test en el IDE.

Las instrucciones para cambiar el **coverage runner** de IDEA por Jacoco son las siguientes:

https://www.jetbrains.com/help/idea/configuring-code-coverage-measurement.html#options

### Integración de Maven con IntelliJ IDEA

Simpre se puede optar por usar la integración que ya trae IntelliJ IDEA

![jacoco-idea-runner](https://raw.githubusercontent.com/LuisCusihuaman/java-getting-started/master/docs/jacoco-idea.png)

Maven -> java-getting-started -> Lifecycle -> **test**, lanzará los tests y Jacoco generará el index.html con el reporte.

## Contribuir
Las Pull Request son bienvenidas. 
Para cambios importantes, abra primero un issue para discutir qué le gustaría cambiar.
