# Programación Estructurada

Materiales del curso de Programación Estructurada (Python) en CUTLAJO, Universidad de Guadalajara.

## Estructura

```
datos/    conjuntos de datos para ejemplos y ejercicios
```

## Cómo usar los datos

Lee los archivos directamente desde GitHub, sin descargarlos:

```python
import pandas as pd

URL = "https://raw.githubusercontent.com/strahlenguy/programacion-estructurada/main/datos/pacientes.csv"
df = pd.read_csv(URL)
```

La URL debe ser la versión **raw** (`raw.githubusercontent.com`). La dirección normal de GitHub (`github.com/.../blob/...`) devuelve la página web, no el CSV.

Si vas a trabajar sin internet, guarda una copia local una vez y después usa el archivo:

```python
df.to_csv("pacientes.csv", index=False)
```

## Conjuntos de datos

### `datos/pacientes.csv`

120 pacientes, 9 columnas. **Datos sintéticos** generados para la clase; no corresponden a personas reales. Incluyen valores faltantes a propósito en `peso_kg`, `temp_c` y `glucosa_mgdl`.

| Columna        | Descripción                              | Unidad  |
|----------------|------------------------------------------|---------|
| `id`           | identificador del paciente               | texto   |
| `sexo`         | F o M                                    | texto   |
| `edad`         | edad en años                             | entero  |
| `peso_kg`      | peso                                     | kg      |
| `estatura_m`   | estatura                                 | m       |
| `temp_c`       | temperatura corporal                     | °C      |
| `fc_lpm`       | frecuencia cardiaca                      | lat/min |
| `glucosa_mgdl` | glucosa en ayuno                         | mg/dL   |
| `servicio`     | Consulta, Urgencias u Hospitalización    | texto   |

Se usa en la Unidad 6 (introducción a NumPy y pandas).
