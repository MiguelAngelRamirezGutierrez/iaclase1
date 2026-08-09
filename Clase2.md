# Inteligencia Artificial – Clase 2
## Estructuras de Datos y Funciones en Python

**Asignatura:** Inteligencia Artificial  
**Clave:** InteligenciaArtificialN  
**Duración:** 90 minutos  
**Semana:** 2

---

## 1. Portada

### Título de la clase
- Inteligencia Artificial – Clase 2
- Estructuras de Datos y Funciones en Python

### Información del curso
- **Docente:** [Nombre del docente]
- **Fecha:** Semana 2
- **Clave:** InteligenciaArtificialN

---

## 2. Repaso de la Clase Anterior

### ¿Qué vimos la clase pasada?
- Definición de IA y objetivo del curso.
- Instalación de Python, VSCode y Git.
- Creación de cuenta en GitHub.
- Variables, tipos de datos y condicionales (`if` / `else`).
- Primer script en Python y primer commit en GitHub.
- Introducción a Markdown.

### Actividad independiente entregada
- Investigación de 3 proyectos en formato Markdown (`investigacion_proyectos.md`).

---

## 3. Agenda de la Clase de Hoy

### Explicación teórica (25-30 min)
- Listas: creación, indexación, métodos básicos.
- Diccionarios: clave-valor, acceso y modificación.
- Funciones: definición, parámetros y retorno.

### Definición de proyectos (10 min)
- Presentación de propuestas.
- Aprobación de proyectos.

### Actividad práctica en clase (40-45 min)
- Ejercicio integrador con listas, diccionarios y funciones.

### Actividad independiente
- Tarea para la próxima semana.

---

## 4. Listas en Python (Parte 1)

### ¿Qué es una lista?
Una lista es una colección ordenada de elementos que puede contener diferentes tipos de datos (números, textos, booleanos, etc.).

### Creación de listas
```python
frutas = ["manzana", "banana", "cereza"]
numeros = [10, 20, 30, 40]
mixta = [1, "hola", True, 3.14]
```

### Acceso a elementos (indexación)
```python
print(frutas[0])   # "manzana" (primer elemento)
print(frutas[1])   # "banana" (segundo elemento)
print(frutas[-1])  # "cereza" (último elemento)
```

### Modificar un elemento
```python
frutas[1] = "pera"
print(frutas)  # ["manzana", "pera", "cereza"]
```

> Nota: En Python, las posiciones empiezan en `0`. Si usamos `-1`, accedemos al último elemento.

---

## 5. Listas en Python (Parte 2) – Métodos Básicos

### Agregar elementos al final: `append()`
```python
frutas.append("naranja")
print(frutas)  # ["manzana", "pera", "cereza", "naranja"]
```

### Insertar en una posición específica: `insert(posición, elemento)`
```python
frutas.insert(1, "mango")
print(frutas)  # ["manzana", "mango", "pera", "cereza", "naranja"]
```

### Eliminar un elemento por su valor: `remove()`
```python
frutas.remove("pera")
print(frutas)  # ["manzana", "mango", "cereza", "naranja"]
```

### Eliminar por posición: `pop(posición)` o `pop()` (último)
```python
frutas.pop(1)  # elimina "mango"
frutas.pop()   # elimina "naranja"
print(frutas)  # ["manzana", "cereza"]
```

### Longitud de una lista: `len()`
```python
print(len(frutas))  # 2
```

---

## 6. Diccionarios en Python

### ¿Qué es un diccionario?
Un diccionario es una colección de pares clave-valor. Cada clave es única y se usa para acceder a su valor asociado.

### Creación de un diccionario
```python
persona = {
    "nombre": "Carlos",
    "edad": 25,
    "ciudad": "Cartago"
}
```

### Acceso a valores
```python
print(persona["nombre"])  # "Carlos"
print(persona["edad"])    # 25
```

### Modificar un valor
```python
persona["edad"] = 26
```

### Agregar un nuevo par clave-valor
```python
persona["profesion"] = "Ingeniero"
```

### Eliminar una clave
```python
del persona["ciudad"]
```

### Verificar si existe una clave
```python
if "nombre" in persona:
    print("La clave 'nombre' existe")
```

> Nota: Los diccionarios son como una agenda telefónica: usamos claves (como nombres) para acceder a valores (como números de teléfono).

---

## 7. Funciones en Python (Parte 1)

### ¿Qué es una función?
Una función es un bloque de código reutilizable que realiza una tarea específica. Nos ayuda a organizar el código y evitar repetir instrucciones.

### Definir una función (sin parámetros)
```python
def saludar():
    print("¡Hola desde una función!")
```

### Llamar (ejecutar) una función
```python
saludar()  # ¡Hola desde una función!
```

### Definir una función con parámetros
```python
def saludar_persona(nombre):
    print("Hola", nombre)
```

### Llamar con argumentos
```python
saludar_persona("María")  # Hola María
```

> Nota: Una función es como una receta de cocina: tiene pasos definidos que se ejecutan cuando la invocamos.

---

## 8. Funciones en Python (Parte 2) – Retorno de Valores

### Función con retorno (`return`)
```python
def sumar(a, b):
    resultado = a + b
    return resultado
```

### Usar el valor retornado
```python
total = sumar(5, 3)
print(total)  # 8
```

### Función que retorna un valor calculado
```python
def calcular_promedio(lista_numeros):
    suma = sum(lista_numeros)
    cantidad = len(lista_numeros)
    promedio = suma / cantidad
    return promedio


temperaturas = [28, 30, 25, 27, 29]
promedio = calcular_promedio(temperaturas)
print("Promedio:", promedio)
```

> Nota: `sum()` es una función incorporada que suma todos los elementos de una lista.

---

## 9. Integración de Conceptos – Ejemplo Práctico

### Problema
Tenemos datos de cultivos en Cartago. Queremos calcular el rendimiento promedio por cultivo.

### Datos
```python
cultivos = [
    {"nombre": "Café", "hectareas": 5, "produccion_toneladas": 3.2},
    {"nombre": "Caña", "hectareas": 10, "produccion_toneladas": 8.5},
    {"nombre": "Maíz", "hectareas": 3, "produccion_toneladas": 1.8}
]
```

### Función para calcular rendimiento por hectárea
```python
def rendimiento_por_hectarea(cultivo):
    return cultivo["produccion_toneladas"] / cultivo["hectareas"]
```

### Uso
```python
for cultivo in cultivos:
    rend = rendimiento_por_hectarea(cultivo)
    print(f"{cultivo['nombre']}: {rend:.2f} ton/ha")
```

### Explicación
- `for` recorre cada diccionario en la lista.
- La función calcula el rendimiento.
- `f"{...}"` es un f-string que permite insertar variables en un texto.

---

## 10. Definición de Proyectos

### Proceso para elegir el proyecto
Cada estudiante o equipo presenta su propuesta basada en la investigación de la semana pasada.

El docente valida que sea:
- Aplicable a una problemática real de Cartago, Valle.
- Factible con los conocimientos del curso.
- Interesante para los estudiantes.
- Aprobado oficialmente.

### Requisitos del proyecto
- Debe utilizar Python.
- Debe incluir al menos una estructura de datos (listas o diccionarios).
- Debe tener al menos una función definida por el estudiante.
- Se versionará en GitHub con commits regulares.
- Se presentará al final del semestre con documentación y demo.

---

## 11. Estructura Sugerida para el Proyecto

### Nombre del proyecto
- Descriptivo y claro.

### Problemática
- ¿Qué situación real quiere mejorar o resolver?

### Datos
- ¿Qué información necesita?
- ¿Dónde la va a obtener? (datos abiertos, archivos CSV, APIs, etc.)

### Objetivo
- ¿Qué va a lograr su sistema de IA? (por ejemplo, predecir, clasificar, recomendar).

### Tecnologías
- Python
- Librerías sugeridas: NumPy, Pandas, Scikit-learn, etc.

### Entregables
- Código fuente en GitHub.
- Documentación (`README.md`).
- Presentación final (demo).

---

## 12. Actividad en Clase (Guía Paso a Paso)

### Objetivo
Crear un programa que gestione información de cultivos en Cartago, usando listas, diccionarios y funciones.

### Instrucciones detalladas
1. Crear un archivo nuevo: `gestion_cultivos.py`.
2. Definir una lista de diccionarios con datos de al menos 5 cultivos. Cada diccionario debe tener:
   - `nombre` (texto)
   - `hectareas` (número)
   - `produccion_toneladas` (número)
3. Definir las siguientes funciones:
   - `calcular_rendimiento(cultivo)` → retorna la producción por hectárea.
   - `mostrar_cultivos(lista_cultivos)` → recorre la lista y muestra el nombre y el rendimiento de cada cultivo con un mensaje formateado.
   - `cultivo_mayor_rendimiento(lista_cultivos)` → retorna el nombre del cultivo con mayor rendimiento.
4. En el programa principal:
   - Llamar a `mostrar_cultivos()` para ver todos los datos.
   - Llamar a `cultivo_mayor_rendimiento()` y mostrar el resultado.
   - Ejecutar el script y verificar que la salida sea correcta.
5. Agregar cambios a Git:
```bash
git add gestion_cultivos.py
git commit -m "Agregar gestión de cultivos con listas, diccionarios y funciones"
git push
```

### Criterios de evaluación
- El script ejecuta sin errores.
- Las funciones están correctamente definidas y retornan lo esperado.
- El código está subido a GitHub.

---

## 13. Actividad Independiente (Complementaria)

### Objetivo
Aplicar los conceptos de listas, diccionarios y funciones para procesar un archivo de datos real y preparar el terreno para el proyecto.

### Instrucciones detalladas
1. Buscar un archivo de datos (`CSV` o `JSON`) relacionado con la problemática de su proyecto. Pueden usar:
   - Datos abiertos de la Alcaldía de Cartago.
   - Kaggle (datasets de Colombia).
   - Datos de agricultura, clima, movilidad, etc.
2. Crear un script `cargar_datos.py` que:
   - Defina una función `leer_datos(ruta_archivo)` que lea el archivo y lo convierta en una lista de diccionarios.
   - Defina una función `mostrar_resumen(datos)` que muestre:
     - Cantidad total de registros.
     - Tres estadísticas básicas (por ejemplo, promedio de una columna numérica, valor máximo y mínimo).
3. Ejecutar el script y verificar que funciona.
4. Subir los cambios a GitHub con un commit descriptivo.

### Preparación para la próxima clase
- Tener listo el archivo de datos que usarán en su proyecto.
- Tener una idea clara de cómo van a estructurar sus datos en Python.

### Fecha de entrega
- Antes de la próxima sesión (Clase 3).

nombre (texto)

hectareas (número)

produccion_toneladas (número)

Definir las siguientes funciones:

calcular_rendimiento(cultivo): retorna la producción por hectárea.

mostrar_cultivos(lista_cultivos): recorre la lista y muestra el nombre y el rendimiento de cada cultivo con un mensaje formateado.

cultivo_mayor_rendimiento(lista_cultivos): retorna el nombre del cultivo con mayor rendimiento.

En el programa principal:

Llamar a mostrar_cultivos() para ver todos los datos.

Llamar a cultivo_mayor_rendimiento() y mostrar el resultado.

Ejecutar el script y verificar que la salida sea correcta.

Agregar cambios a Git:

bash
git add gestion_cultivos.py
git commit -m "Agregar gestión de cultivos con listas, diccionarios y funciones"
git push
Criterios de evaluación
El script ejecuta sin errores.

Las funciones están correctamente definidas y retornan lo esperado.

El código está subido a GitHub.

13. Actividad Independiente (Complementaria)
Objetivo: Aplicar los conceptos de listas, diccionarios y funciones para procesar un archivo de datos real y preparar el terreno para el proyecto.

Instrucciones detalladas
Buscar un archivo de datos (CSV o JSON) relacionado con la problemática de su proyecto. Pueden usar:

Datos abiertos de la Alcaldía de Cartago.

Kaggle (buscar datasets de Colombia).

Datos de agricultura, clima, movilidad, etc.

Crear un script cargar_datos.py que:

Defina una función leer_datos(ruta_archivo) que lea el archivo y lo convierta en una lista de diccionarios (similar a la actividad en clase).

Defina una función mostrar_resumen(datos) que muestre:

Cantidad total de registros.

Tres estadísticas básicas (por ejemplo, promedio de una columna numérica, valor máximo y mínimo).

Ejecutar el script y verificar que funciona.

Subir los cambios a GitHub con un commit descriptivo.

Preparación para la próxima clase:

Tener listo el archivo de datos que usarán en su proyecto.

Tener una idea clara de cómo van a estructurar sus datos en Python.

Fecha de entrega: Antes de la próxima sesión (Clase 3).
