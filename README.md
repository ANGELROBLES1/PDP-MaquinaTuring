# Maquina de Turing BINARIA

Este repositorio contiene una implementacion de una Maquina de Turing en Python capaz de procesar cadenas binarias y realizar operaciones matematicas basicas y avanzadas

## Descripcion

La Maquina de Turing implementada en este proyecto trabaja con una cinta binaria y utiliza una tabla de transiciones para moverse a traves de ella Ademas tenemos el codigo que incluye funciones para realizar operaciones matematicas como suma resta multiplicacion division raiz cuadrada potencia logaritmo y seno midiendo el tiempo de ejecucion de cada una

## Funcionamiento

Se inicializa con una cinta de entrada y un estado inicial Luego ejecuta las transiciones definidas en su tabla hasta alcanzar un estado final La cinta se representa como una lista de caracteres y el cabezal se mueve a la derecha o izquierda dependiendo de la transicion correspondiente

### Tabla de Transiciones

| Estado | Simbolo leido | Nuevo estado | Simbolo escrito | Movimiento |
|--------|--------------|--------------|----------------|------------|
| q0     | 0            | q0           | 0              | Derecha    |
| q0     | 1            | q0           | 1              | Derecha    |
| q0     | (espacio)    | qf           | (espacio)      | Izquierda  |
| qf     | -            | -            | -              | -          |

## Ejecucion

Para ejecutar la Maquina de Turing crea una instancia de la clase `MaquinaTuring` y llama al metodo `ejecutar` Tambien puedes utilizar la funcion `realizar_operacion` para ejecutar operaciones matematicas

### Ejemplo de Uso

```python
from maquina_turing import MaquinaTuring

# Crear una instancia de la Maquina de Turing con una cinta binaria
mt = MaquinaTuring("10101 ")
resultado = mt.ejecutar()
print("Resultado de la ejecucion de la Maquina de Turing:", resultado)

# Ejemplo de operaciones matematicas
operacion tiempo = mt.realizar_operacion('suma' 5 3)
print(f"Suma {operacion} Tiempo {tiempo:.6f} segundos")
```

## Pruebas y Resultados Esperados

| Entrada    | Salida esperada | Explicacion |
|------------|----------------|-------------|
| "1010 "   | "1010 "        | La maquina recorre la cinta y se detiene en el estado final |
| "11100 "  | "11100 "       | La maquina procesa la cinta hasta encontrar el espacio |

### Pruebas de Operaciones Matematicas

| Operacion          | Entrada       | Salida esperada |
|--------------------|--------------|----------------|
| Suma              | (1005 2033)  | 3038           |
| Resta             | (5 3)        | 2              |
| Multiplicacion    | (5 3)        | 15             |
| Division          | (5 4)        | 125            |
| Raiz cuadrada     | (16)          | 40            |
| Potencia          | (2 4)        | 160           |
| Logaritmo         | (100 10)     | 20            |
| Seno              | (90 grados)   | 10            |

## Errores que se pueden esperar

El codigo maneja errores en casos de
- Division por cero
- Raiz cuadrada de un numero negativo
- Exponentes negativos en la funcion de potencia
- Logaritmos con base no valida

## Requisitos
- Librerias estandar de Python math time

____________________________________________________________________________________________________________________________________________________________________
# Maquina de Turing Unitaria

Este repositorio contiene una implementacion de una Maquina de Turing en Python capaz de procesar cadenas en notacion unitaria y realizar operaciones matematicas basicas y avanzadas

## Descripcion

La Maquina de Turing implementada en este proyecto trabaja con una cinta que representa numeros en notacion unitaria y utiliza una tabla de transiciones para moverse a traves de ella Ademas el codigo incluye funciones para realizar operaciones matematicas como suma resta multiplicacion division raiz cuadrada potencia logaritmo y seno midiendo el tiempo de ejecucion de cada una

## Funcionamiento

La Maquina de Turing se inicializa con una cinta de entrada y un estado inicial Luego ejecuta las transiciones definidas en su tabla hasta alcanzar un estado final La cinta se representa como una lista de caracteres y el cabezal se mueve a la derecha o izquierda dependiendo de la transicion correspondiente

### Tabla de Transiciones

| Estado | Simbolo leido | Nuevo estado | Simbolo escrito | Movimiento |
|--------|--------------|--------------|----------------|------------|
| q0     | 1            | q1           | X              | Derecha    |
| q1     | 1            | q1           | 1              | Derecha    |
| q1     | +            | q2           | +              | Derecha    |
| q2     | 1            | q3           | Y              | Izquierda  |
| q3     | Y            | q3           | Y              | Izquierda  |
| q3     | X            | q0           | X              | Derecha    |
| qf     | -            | -            | -              | -          |

## Ejecucion

Para ejecutar la Maquina de Turing crea una instancia de la clase `MaquinaTuringUnitario` y llama al metodo `ejecutar` Tambien puedes utilizar la funcion `realizar_operacion` para ejecutar operaciones matematicas

### Ejemplo de Uso

```python
from maquina_turing_unitaria import MaquinaTuringUnitario

# Crear una instancia de la Maquina de Turing con una cinta unitaria
mt = MaquinaTuringUnitario("111+11")
resultado = mt.ejecutar()
print("Resultado de la ejecucion de la Maquina de Turing Unitaria:", resultado)

# Ejemplo de operaciones matematicas
operacion, tiempo = mt.realizar_operacion('suma', 5, 3)
print(f"Suma {operacion} Tiempo {tiempo:.6f} segundos")
```

## Pruebas y Resultados Esperados

| Entrada   | Salida esperada | Explicacion |
|-----------|----------------|-------------|
| "111+11"  | 5              | La maquina suma dos numeros en notacion unitaria |
| "111-11"  | 1              | La maquina resta dos numeros en notacion unitaria |

### Pruebas de Operaciones Matematicas

| Operacion          | Entrada       | Salida esperada |
|--------------------|--------------|----------------|
| Suma              | (105 203)    | 308            |
| Resta             | (512 312)    | 200            |
| Multiplicacion    | (512 312)    | 159744         |
| Division          | (512 312)    | 1641           |
| Raiz cuadrada     | (9)          | 3              |
| Potencia          | (2 4)        | 16             |
| Logaritmo         | (100)        | 2              |
| Seno              | (90 grados)  | 1              |

## Errores Esperados

El codigo maneja errores en casos de
- Division por cero
- Raiz cuadrada de un numero negativo
- Exponentes negativos en la funcion de potencia
- Logaritmos con base no valida

## Requisitos
- Librerias estandar de Python math time



