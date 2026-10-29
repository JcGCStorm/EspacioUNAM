# Códigos para platinar Espacio UNAM

Recopilación comunitaria de los códigos de **Espacio UNAM**, en \LaTeX{}, con un archivo por plantel para que sea fácil contribuir sin perder información.

## Estructura

```
main.tex                            documento principal (portada, índice e \input's)
especiales/medallas-secretas.tex    medallas secretas
especiales/pokemones.tex            carreras sin código / pokemones muy difíciles
especiales/sedes.tex                sedes y bachillerato a distancia
prepas-CCH/cch.tex                  Colegios de Ciencias y Humanidades
prepas-CCH/preparatorias.tex        Preparatorias (1 a 9)
enes/                               Escuelas Nacionales de Educación Superior
fes/                                Facultades de Estudios Superiores
facultades/                         Facultades de Ciudad Universitaria
escuelas/                           Escuelas Nacionales y otras entidades
especiales/tocayo.tex               códigos ordenados por primer nombre
especiales/casi-familia.tex         códigos ordenados por primer apellido
especiales/pastel-compartido.tex    códigos ordenados por mes de cumpleaños
especiales/casi-gemelos.tex         códigos ordenados por día de cumpleaños
especiales/compa-de-banca.tex       código por carrera/plantel/generación
especiales/toda-la-republica.tex    códigos ordenados por estado
reportes.tex                        códigos reportados como no funcionales
estructuralatex/notas.tex           créditos, enlaces y cómo contribuir
imagenesPortada/                    logos de la UNAM
```

Cada archivo de plantel contiene una sección por plantel/facultad y una subsección por carrera, así que solo editas el archivo de tu entidad.

## Comandos útiles

- `\codigos{AAAAAA, BBBBBB}` — muestra los códigos en amarillo.
- `\sincodigo` — marca una carrera que todavía no tiene código.

## Reportar un código que no funciona

Si un código ya no sirve, agrega una entrada en `reportes.tex`:

```latex
\reporte{CODIGO}{Carrera -- Plantel}{Motivo}{ruta/archivo.tex}
```

No necesitas permisos especiales, cualquiera con cuenta de GitHub puede usar el botón
**Editar y borrar**. Si no eres colaborador, GitHub **no** escribe en el repo original, más bien crea automáticamente un *fork* y te propone un *pull request* que un mantenedor revisa y fusiona. Si prefieres, también puedes abrir un *issue* describiendo el código que falla, ese es más sencillo y directo, es como reportar un bug.

## Compilar

Necesita una distribución de \LaTeX{} (por ejemplo TeX Live / TinyTeX).

```
pdflatex -jobname=EspacioUNAMCodigos main.tex
pdflatex -jobname=EspacioUNAMCodigos main.tex   # segunda pasada para el índice
```

o simplemente:

```
latexmk -pdf -jobname=EspacioUNAMCodigos main.tex
```

## Cómo contribuir

1. Busca el archivo de tu plantel (por ejemplo `fes/acatlan.tex`).
2. Agrega tu código en la subsección de tu carrera, separado por comas.
3. **No borres** códigos que ya estén publicados.
4. Abre un *pull request*.

Créditos a toda la comunidad de la UNAM que cooperó aportando códigos.
