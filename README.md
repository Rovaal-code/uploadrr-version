# uploadrr-version

Manifiesto de versión de **eMuwarez Uploadrr**. Un único archivo,
[`latest.json`](latest.json), que dice cuál es la última imagen publicada.

La aplicación lo consulta desde su pestaña **Configuración → Diagnóstico**
para avisarte de que hay una versión nueva que pullear.

## Por qué existe

El repositorio del código y el paquete de imágenes son privados, así que la
aplicación no puede preguntarle al registro si hay algo más nuevo. Este
archivo es la única salida: público, pequeño, y sin nada del código dentro.

## Qué contiene

| Campo | Qué es |
|---|---|
| `commit` | Identificador de la build publicada. Es contra esto que la aplicación compara la suya |
| `fecha` | Cuándo se publicó |
| `digest` | Digest de la imagen en el registro |
| `version` | Versión del paquete |
| `notas` | Una línea sobre qué trae, en neutro |

Las notas se redactan deliberadamente sin detalles: describir aquí un fallo
recién corregido le diría a cualquiera qué buscar en la versión anterior, que
es la que sigue ejecutando quien todavía no ha actualizado.
