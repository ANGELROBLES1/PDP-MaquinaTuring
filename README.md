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


