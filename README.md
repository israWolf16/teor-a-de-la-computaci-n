Aquí tienes un **README.md** claro y adecuado para acompañar tu programa. Está pensado para un repositorio (por ejemplo en GitHub) o para entregar junto con el código.

---

# Operaciones con Cadenas — Prefijos, Sufijos, Subcadenas y Cerraduras

Aplicación con interfaz gráfica desarrollada en **Python (Tkinter)** para trabajar con conceptos básicos de **Teoría de la Computación y Lenguajes Formales**.
Permite calcular **prefijos, sufijos, subcadenas**, así como generar la **cerradura de Kleene (Σ*)** y la **cerradura positiva (Σ⁺)** de un alfabeto.

---

# Características

La aplicación incluye las siguientes funcionalidades:

### 1. Operaciones con una cadena

Dada una cadena de entrada, el programa puede calcular:

* **Prefijos**
* **Sufijos**
* **Subcadenas** (únicas y en orden de aparición)

Opcionalmente se puede **incluir la cadena vacía (ε)** en los resultados.

---

### 2. Cerradura de Kleene (Σ*) y Cerradura Positiva (Σ⁺)

Dado un **alfabeto Σ** y una **longitud máxima n**, el programa genera:

**Σ***
Todas las cadenas posibles con longitud:

0..n

Incluye la **cadena vacía**.

**Σ⁺**
Todas las cadenas posibles con longitud:

1..n

No incluye la cadena vacía.

---

# Cómo ejecutar el programa

## 1. Requisitos

* **Python 3.x**
* Tkinter (normalmente incluido con Python)

Verifica Python con:

```bash
python --version
```

o

```bash
python3 --version
```

---

## 2. Ejecutar el programa

Guarda el archivo como:

```
gui_string_ops.py
```

Luego ejecuta:

```bash
python gui_string_ops.py
```

o

```bash
python3 gui_string_ops.py
```

Se abrirá una **interfaz gráfica**.

---

# Uso del programa

## Pestaña 1 — Sub/Pref/Suf

1. Introduce una **cadena**.
2. Marca si deseas **incluir la cadena vacía**.
3. Presiona **Calcular**.

El programa mostrará:

* Prefijos
* Subcadenas
* Sufijos

Cada resultado incluye el **total generado**.

También puedes **guardar cada resultado** en un archivo `.txt`.

---

## Pestaña 2 — Cerraduras (Σ*, Σ⁺)

1. Introduce el **alfabeto**.

Se aceptan formatos como:

```
a,b,c
```

```
a b c
```

```
abc
```

2. Introduce la **longitud máxima (n)**.
3. Presiona **Generar Σ* y Σ+**.

El programa mostrará:

* Σ* (cerradura de Kleene)
* Σ⁺ (cerradura positiva)

Cada resultado incluye el **número total de cadenas generadas**.

---

# Crecimiento exponencial

La generación de cadenas crece **exponencialmente**.

Si:

* el alfabeto tiene tamaño **k**
* la longitud es **L**

Entonces el número de cadenas posibles es:

[
k^L
]

Ejemplo:

| Alfabeto | n | Cadenas |
| -------- | - | ------- |
| {a,b}    | 3 | 15      |
| {a,b,c}  | 4 | 121     |

Por esta razón el programa incluye un límite de seguridad.

---

# Límite de generación

Para evitar que el programa **consuma demasiada memoria**, existe un límite:

```
MAX_RESULTS = 20000
```

Si la generación supera este valor, el programa **detiene la operación**.

Si necesitas generar más cadenas puedes modificar:

```python
MAX_RESULTS = 20000
```

en el código fuente.

⚠️ Aumentarlo demasiado puede **congelar la aplicación o saturar la memoria**.

---

# Exportar resultados

Cada sección incluye botones **Guardar...** que permiten exportar los resultados a un archivo de texto:

```
prefijos.txt
subcadenas.txt
sufijos.txt
sigma_star.txt
sigma_plus.txt
```

---

# Estructura del programa

El programa contiene tres partes principales:

### 1. Lógica de operaciones con cadenas

Funciones:

* `get_prefixes()`
* `get_suffixes()`
* `get_substrings()`

---

### 2. Generación de cerraduras

Funciones:

* `parse_alphabet()`
* `generate_kleene()`

Estas generan:

* Σ*
* Σ⁺

usando `itertools.product`.

---

### 3. Interfaz gráfica (Tkinter)

Clase principal:

```
StringOpsApp
```

Contiene:

* Pestaña **Sub/Pref/Suf**
* Pestaña **Cerraduras**
* Pestaña **Ayuda**

---

# Aplicación académica

Este programa es útil para estudiar conceptos de:

* **Teoría de la Computación**
* **Lenguajes Formales**
* **Autómatas**
* **Alfabetos y cadenas**
* **Operaciones sobre lenguajes**

---

# Autor

Proyecto desarrollado para prácticas de **Teoría de la Computación**.

---

Si quieres, también puedo darte una **versión más corta del README (tipo tarea)** o una **versión más profesional para GitHub con diagramas y ejemplos matemáticos**.
