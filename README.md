# Clean Code
El clean code nos sirve para tener código de mejor calidad, fácil de leer, estructurado y autodocumento.
Para poder lograr este objetivo podemos divir en siguientes áreas:
- **Nombrado** (Clases, métodos, atributos, etc.)
- **Funciones**
- **Comentarios**
- **Formato del código**



## Nombrado:
La autodocumentación parte del como nombramos nuestras clases, los métodos, paquetes, etc. Pero haré hincapié en lo siguiente:
también nombrar con contexto extra.

    -   Nombre en variabes:                             
            Ej: erroneo                                |          Ej erroneo
                int d;                                 |          Map<Integer, Integer> employeeList 
                int m;                                 |                 
                int y:                                 |                     
            ------------------------------------------------------------------------------------------------------------------- 
            Ej: correcto                               |          Ej correcto               
                int dayOfBirth;                        |          Map<Integer, Integer> employeeMap                       
                int monthOfBirth;                      |                                                             
                int yearOfBirth:                       |                                                 
            --------------------------------------------------------------------------------------------------------------------
            Ej: erroneo                                | 
            private String lstUsedName                 |   
            --------------------------------------------------------------------------------------------------------------------   
            Ej correcto                                | 
            private String leastUsedName               | 

En el nombrado de clases se deben poner nombre o conjunto de nombres.
Los métodos deben de ser nombrados con verbo

## Funciones
Las características para una funciones con principios de clean code son:
    - **Pequeñas**
    - **Hacen una sola cosa**
    - **Nivel de abstracción único**
    - **Reciben pocos argumentos**
    - **No tienen efectos secundarios**
    - **Devuelcen excepciones en lugar de códigos de error**

## Comentarios
Son muy utiles cuando aprendemos y queremos explicar una parte del código, pero en la vida profesionel mintras menos comentarios mejor.

## Formato del código
    Se puede tomar como una guia los lineamientos que proponen empresad de la industria como google.

    El formato de  es importante, si una función hace llamado de otras funciones se recomienda lo siguiente:
        -   private void b(){             |    private function a {        
                a();                      |          a();
                b();                      |          b(); 
            }                             |    }             
                                          |    public void a(){}
                                          |    public void b(){}            
             ------------------------------------------------------------------------------------------------------------------- 


# Principios SOLID
Es un acrónimo propuesto por Robert C. Martin:
- **S** ingle Responsability Principle
- **O** pen-Close Principle
- **L** iskov substitution Principle
- **I** nterface Segregation Principle
- **D** ependency Inversion Principle


##(SRP): Un módulo sólo debe de tener una razón de cambio, no se refiere a que una función haga sólo haga algo en especifico
         sino a que dentro de una clase, que tenga otro objeto como atributo no se haga lógica dentro del contexto de la clase principal
         porque ya dicha clase tendría dos razones de cambio, la clase por si misma y la de la clase como atributo. En todo caso lo que debe de 
         suceder es que se genere una tercera clase que contenga esta logica y las clases anteteriores solo queden con una sola razón de cambio.

-   Clases con demasiadas líneas de código.
-   Cuando se nos indica un cambio tenemos que modificar en muchos ficheros.
-   No cumplir la separación de capas en la arquitectura de software.
-   No analizar bien las responsabilidades a la hora de desarrollar software.
-   Al explicar que hace la clase se enumera más de una responsabilidad.
-   Tener más de un método público. 
-   Dificultad a la hora de testear la clase.


##(OCP): Es el principio que establece que el software debe de estar abierto para su extensión y cerrado para su modificación.
         Esto quiere decir que todo que haga mas robusto el software es válido porque incrementa la funcionalidad sólo que este incremento no debe de cambiar el sentido del mismo.
         Tiene que ver con el acoplamiento, 


**(LSP) Establece si una clase base tiene ciertos comportamientos y propiedades, sus clases derivadas deben de ser capaces de heredar y utilizar 
        esos comportamientos y propiedades de sin cambiar el correcto funcionamiento del programa.
         