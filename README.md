# Reto-No.6
### Diagramas de flujo
#### 1. Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.
```mermaid
flowchart TD
    A(Inicio) --> B[Repetir para cada numero desde 1 hasta 100]
    B --> C[Calcular cuadrado numero^2]
    C --> D[Mostrar numero y su cuadrado]
    D --> E{¿Hay más números en el rango?}
    E -->|Sí| B
    E -->|No| F[Fin]
```
#### 2. Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.
##### Numeros Impares
```mermaid
flowchart TD
    A(Inicio) --> B[Mostrar Impares]
    B --> C[Repetir para cada numero desde 1 hasta 999]
    C --> D[Mostrar cada 2 numeros]
    D --> E{¿Hay más números en el rango?}
    E -->|Sí| C
    E -->|No| F[Fin]
```
##### Numeros Pares
```mermaid
flowchart TD
    A(Inicio) --> B[Mostrar Pares]
    B --> C[Repetir para cada numero desde 2 hasta 1000]
    C --> D[Mostrar cada 2 numeros]
    D --> E{¿Hay más números en el rango?}
    E -->|Sí| C
    E -->|No| F[Fin]
```
#### 3. Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado.
```mermaid
flowchart TD
    A(Inicio)--> B[Crear lista vacía pares]
    B --> C{¿numero >= 2?}
    C -->|Sí| D[Para i en el rango de numero a 1 (decrementando)]
    C -->|No| H[Imprimir "Error: el número ingresado no es >= 2"]
    D --> E{¿i % 2 == 0?}
    E -->|Sí| F[Agregar i a la lista 'pares']
    E -->|No| G[Continuar]
    F --> G
    G --> D
    D --> I{¿Hay más números en el rango?}
    I -->|Sí| D
    I -->|No| J[Retornar lista 'pares']
    H --> K[Fin]
    J --> K
```
