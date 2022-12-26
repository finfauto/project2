# Proyecto 2

Tenemos una estructura de datos que contiene todas las notas del curso de todos los alumnos. La estructura tiene la siguiente forma:

```python

[
    {
        "nombre": "Luisa López",
        "exercises": [4, 6.5, 10, 8],
        "practise_passed": True,
        "partial_exam": 7.5,
        "final_exam": 8
    },
    {
        "nombre": "Pedro García",
        "exercises": [2, 0, 5, 6],
        "practise_passed": True,
        "partial_exam": 3.3,
        "final_exam": 5.5
    },
    {
        "nombre": "Fermín Gutiérrez",
        "exercises": [8, 8, 10, 9.5],
        "practise_passed": False,
        "partial_exam": 8.2,
        "final_exam": 9
    }
]
```

Es decir, disponemos de una lista donde cada elemento es un diccionario que contiene los datos de un alumno. Dichos datos son:

* nombre
* notas de ejercicios durante el curso
* si ha pasado o no la práctica
* nota del examen parcial
* nota del examen final

## Parte 1

Nos piden hacer una función que devuelva la nota obtenida por el alumno durante el curso, sabiendo que los pesos para calcular la nota son:

* ejercicios durante el curso representa el 10% de la nota
* examen parcial representa el 15% de la nota
* examen final representa el 75% de la nota

Además, solamente se podrá aprobar el curso si se tiene la práctica aprobada. Si el alumno no tiene aprobada la práctica la nota que deberá devolver esta función será un 0.

La función a implementar tiene la siguiente interfaz:

```python
def calcula_nota_alumno(datos_alumno: {}) -> float:
```

Siendo **datos_alumno** un diccionario con los datos de un alumno, como se ha descrito anteriormente. Por ejemplo:

```python
    {
        "nombre": "Luisa López",
        "exercises": [4, 6.5, 10, 8],
        "practise_passed": True,
        "partial_exam": 7.5,
        "final_exam": 8
    }
```

## Parte 2

Una vez implementada la función **calcula_nota_alumno** y haciendo uso de ella, nos piden procesar todos los datos del curso para obtener una lista con los resultados de todos los alumnos.

El resultado será una lista de tuplas donde el primer término será el nombre del alumno y el segundo la nota obtenida mediante **calcula_nota_alumno**

La función a implemente tiene la siguiente interfaz:

```python
def calcula_notas_curso(datos_alumnos: []) -> [(str, float)]:
```
