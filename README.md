# 6.2.BateriaDeEjercicios
Repo para los ejercicios de diagrama de clases

# UML Ejercicio 1

```mermaid  
classDiagram 
direction TB
    class Usuario {
	    -nombre: String
	    -contrasena: String
	    +email: String
	    +cambiarPassword(String nueva) void
	    -validar email() void
    }
```

# UML Ejercicio 2

``` mermaid
classDiagram
direction TB
    class Persona {
	    -nombre: String
	    -DNI: String
    }

    class Estudiante {
	    -numeroExpediente: String
	    -notaMedia: double
    }

    Persona --|> Estudiante
```


# UML Ejercicio 3

```mermaid
classDiagram
direction TB
    class Computadora {
    }

    class PlacaBase {
    }

    class Raton {
    }

    Computadora <|--* PlacaBase
    Computadora <|--o Raton
```

# UML Ejercicio 4

``` mermaid
classDiagram
direction TB
    class CentroComercial {
    }

    class Tienda {
    }

    CentroComercial "1" <|--* "*" Tienda
```

# UML Ejercicio 5

``` mermaid
classDiagram
direction TB
    class MetodoPago {
	    procesar(importe) double
    }

    class Tarjeta {
	    procesar(importe) double
    }

    class PayPal {
        procesar(importe) double
    }

    class Carrito {
	    pagar(MetodoPago miMetodo) double
    }

	<<interface>> MetodoPago

    MetodoPago --|> Tarjeta
    MetodoPago --|> PayPal
    Carrito ..|> MetodoPago

```

# UML Ejercicio 6
```mermaid
classDiagram
direction TB
    class Libro {
	    isbn: String
	    +prestar()
	    +devolver()
    }

    class Revista {
	    numeroEdicion: int
	    +prestar()
	    +devolver()
    }

    class Usuario {
	    nombre: String
	    numCarnet: int
    }

    class Recurso {
	    -id: int
	    -titulo: String
	    +prestar()
	    +devolver()
    }

	<<abstract>> Recurso

    Recurso --|> Libro
    Recurso --|> Revista
    Usuario "1" --> "*" Recurso

```








