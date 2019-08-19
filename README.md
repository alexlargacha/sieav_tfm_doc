<p align="center">
</p>

# TFM para el máster SIEAV

[![made-with-latex](https://img.shields.io/badge/Made%20with-LaTeX-1f425f.svg)](https://www.latex-project.org/) [![GitHub release](https://img.shields.io/github/release/jonatanlv/templateTFM.svg)](https://GitHub.com/jonatanlv/templateTFM/releases/) [![GitHub watchers](https://img.shields.io/github/watchers/jonatanlv/templateTFM.svg?label=Watch&style=social)](https://GitHub.com/jonatanlv/templateTFM)

```bash
git clone git@github.com:alexlargacha/sieav_tfm_doc.git
```
desde una terminal y comenzar a modificar los archivos o directamente con el botón de `Clonar o descargar` en la página del proyecto.

## Compilación separada del documento

A medida que el tfm va aumentando en tamaño, y sobre todo tras la inclusión de imágenes, el tiempo de compilado aumenta considerablemente. Lo normal, sobre todo al principio, es que la mayoría del tiempo se escriba en un solo capítulo.

La plantilla se ha estructurado de forma modular para permitir la compilación de los capítulos por separado. Para esto se ha usado el paquete `newclude` que incluye los comandos `\includeonly` y `\include*`.

Su uso es bastante sencillo, cada capítulo se ponen en un fichero aparte (excepto los capítulos de resumen y abstract que van en un mismo fichero ya que no deben ser muy extensos). En el punto donde se quiera incluir el capítulo, en el archivo principal (*TemplateTFM.tex*), usamos `\include*{nombre_fichero_sin_extension}`. Cuando queramos compilar solamente dicho capítulo, en el preámbulo usamos `\includeonly{nombre_fichero_sin_extension}`.

> **AVISO IMPORTANTE**: Cuando se usa la compilación separada, el resto de capítulos *no existen* con lo cual las referencias a dichos capítulos (los no incluidos) aparecerán con el típico **??**. Además, a veces cuando se modifica el `\includeonly` la numeración de las páginas hace saltos erróneos, los índices muestran información incorrecta,... mi consejo es que cada vez que se modifique el comando `\includeonly`, ya sea el capítulo incluido o si se quita o pone de nuevo, se haga una compilación limpia, es decir, borrar los archivos temporales y compilar.
