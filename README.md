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