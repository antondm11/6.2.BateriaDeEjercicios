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

