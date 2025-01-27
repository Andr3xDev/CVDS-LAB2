# CVDS-LAB2

## :hammer: Construcción

Proceso de construcción de proyecto en Maven

![image](https://github.com/user-attachments/assets/b8420a50-2b4d-4700-8dd5-8c4ff3403ff7)
![image](https://github.com/user-attachments/assets/a3c6f8d6-f8ec-43a3-a26d-83cbe45e638b)
![image](https://github.com/user-attachments/assets/336f1490-2670-4ea8-9d12-5eb3589d3a66)
![image](https://github.com/user-attachments/assets/6654d7b8-6636-499d-9acd-7b7b17f967bd)
![image](https://github.com/user-attachments/assets/fe3db421-473b-4017-a14f-cc01cbf2714f)


## :hammer_and_wrench: Compilar y Ejecutar
Despues de compilar correctamente con el comando `mvn package`

Ejecutamos con `mvn exec:java -Dexec.mainClass="edu.eci.cvds.patterns.archetype.App"`
y comprobamos que se ejecuta correctamente

![image execute hello world](https://github.com/user-attachments/assets/940e7d34-1973-4f3d-9bc1-cb534d958f51)

Ahora cambiamos la clase `App.java` y añadimos la posibilidad de un saludo personalizado para nombre y nombre-apellido:

Ejecutamos con `mvn exec:java -Dexec.mainClass="edu.eci.cvds.patterns.archetype.App" -Dexec.args="Nicole"`
Y obtenemos correctamente

![image execute hello name](https://github.com/user-attachments/assets/ca378c4b-9aae-4866-b4cd-dfdead15c8d0)

Ahora ejecutammos con `mvn exec:java -Dexec.mainClass="edu.eci.cvds.patterns.archetype.App" -Dexec.args="Nicole Calderon"`
Y comprobamos su funcionamiento

![image execute hello name-last name](https://github.com/user-attachments/assets/44ed8a49-dcd8-4b42-9e03-3039c970e543)

En cada uno de los cambios al código se compila nuevamente con `mvn package`

## :heavy_check_mark: Herramienta Maven

![image Maven](https://github.com/user-attachments/assets/76a37497-d974-4532-b6a9-420062606292)

#### ¿Cúal es su mayor utilidad?
- Permitir al desarrollador comprender el estado del proyecto durante todo su cliclo de vida, de una forma rapida y estandarizada

#### Fases de Maven
- Para un default lifecycle se tienen las siguientes 7 fases:
  1. `Validate` -> Valida que el proyecto este correcto y que toda la información necesaria este diponible
  2. `Compile` -> Compila el código fuente del proyecto
  3. `Test` -> Prueba el código compilado usando un marco de pruebas unitarias
  4. `Package` -> Empaqueta el código compilado en un formato ditribuible
  5. `Verify` -> Verifica los resultados de las pruebas de integración para que cumpla con los criterios de calidad
  6. `Install` -> Instala el paquete en el repositorio local
  7. `Deploy` -> Copia el paquete final en el repositorio remoto
  
#### Ciclos de vida de la construcción
En Maven, el ciclo de vida de construcción de un proyecto esta compuesto por fases, plugins y goals donde cada parte cumple una tarea en el proceso de construcción. En el caso del ciclo de vida Default su ciclo de vida es el siguiente:

![image default lifecycle](https://github.com/user-attachments/assets/e22a6e2e-7812-4f5d-9f21-d97054c3b5ac)

Maven cuenta con 3 ciclos de vida de construcción que son: Default, Clean y Site

#### ¿Para qué sirven `los plugins`?
- Los plugins son colecciones empaquetadas que sirven para reutilizar lógica y ejecutar acciones cuando aún no son descargados. Segun Maven sirven tambien para crear archivos JAR, archivos WAR, compilar codigo, hacer pruebas unitarias,etc. Es decir que son utiles en todo el proyecto
  
#### ¿Qué es? y ¿para qué sirve el repositorio central de maven?
- Maven Central es un repositorio de codigo abierto y el principal registro de software, complementos, bibliotecas y marcos de Java. Permite a los desarrolladores gestionar las dependencias de sus proyectos de manera eficaz
