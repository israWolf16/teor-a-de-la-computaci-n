Aquí tienes un **README.md minimalista** que **solo contiene lo que piden las instrucciones**, sin secciones extra, listo para GitHub.

```markdown
# Instrucciones de uso

- En la pestaña **'Sub/Pref/Suf'** introduce una cadena y presiona **'Calcular'**. Puedes marcar si quieres incluir la **cadena vacía**.

- En la pestaña **'Cerraduras (Σ*, Σ+)'** introduce el **alfabeto** y la **longitud máxima n**.  
  - **Σ*** genera todas las cadenas con longitud **0..n** (incluye la cadena vacía).  
  - **Σ+** genera todas las cadenas con longitud **1..n**.

- Ten en cuenta que la generación crece **exponencialmente**: si el alfabeto tiene tamaño **k** y **n** es la longitud máxima, el número de cadenas de longitud exactamente **L** es:

```

k^L

```

- Para proteger tu equipo, este programa limita la generación a **20000 cadenas**.  
  Si necesitas generar más, puedes aumentar el valor de **MAX_RESULTS** en el código (con precaución).

- Usa los botones **'Guardar...'** para exportar cualquier resultado a un **archivo de texto**.
```
