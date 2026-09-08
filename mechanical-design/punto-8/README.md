# Punto 8 — Taller 1 Diseño Mecánico 2026-2

Solución desarrollada, revisada y verificada paso a paso a partir del diagrama del punto 8 del taller.

## Interpretación geométrica

- La sección `a-a` es normal al tramo inclinado.
- El tramo inclinado forma 30° con la vertical (60° con la horizontal).
- Carga aplicada: `F = 750 lb`, vertical.
- Tramo inclinado: `2 in`.
- Excentricidad indicada respecto al tramo vertical inferior: `1.25 in`.
- Sección rectangular: `0.75 in × 0.50 in`.
- Límite de fluencia: `Sy = 40 ksi`.

## Estática en la sección a-a

- `N = 750 cos(30°) = 649.52 lb`
- `V = 750 sin(30°) = 375.00 lb`
- Proyección horizontal del tramo inclinado: `2 sin(30°) = 1.00 in`
- Excentricidad efectiva: `e = 1.25 - 1.00 = 0.25 in`
- Momento flector: `M = 750(0.25) = 187.5 lb·in`

## Propiedades de sección

- `A = (0.75)(0.50) = 0.375 in²`
- `c = 0.75/2 = 0.375 in`
- `I = (1/12)(0.50)(0.75)^3 = 0.0175781 in^4`
- `σ_N = N/A = +1.732 ksi`
- `|σ_b| = Mc/I = 4.000 ksi`

## Resultados verificados

| Magnitud | Punto A | Punto B |
|---|---:|---:|
| Esfuerzo normal | **-2.268 ksi** | **+5.732 ksi** |
| Estado | Compresión | Tracción |
| Esfuerzo cortante transversal | 0 | 0 |
| Principales, esfuerzo plano | (0, -2.268) ksi | (5.732, 0) ksi |
| Cortante máximo absoluto | 1.134 ksi | 2.866 ksi |
| von Mises | 2.268 ksi | 5.732 ksi |
| Factor de seguridad | 17.64 | **6.98** |

La condición crítica corresponde al **punto B**, con `n_min ≈ 6.98`.

## QA realizado

- Revisión completa del equilibrio y del brazo de momento.
- Verificación del eje de flexión correcto y del momento de inercia `I = (1/12)(0.50)(0.75)^3`.
- Corrección de la asignación de signos de flexión en A y B.
- Verificación de que `τ_A = τ_B = 0` por encontrarse en fibras extremas.
- Revisión de esfuerzos principales, círculos de Mohr, von Mises y factores de seguridad.
- Compilación LaTeX sin warnings, overfull boxes ni underfull boxes.
- Inspección visual de las seis páginas renderizadas.

## Archivo fuente

- `Punto_8_Solucion_Diseno_Mecanico.tex`

El documento usa LaTeX + TikZ para reconstruir de forma profesional la geometría, el cuerpo libre, la sección transversal, la distribución de esfuerzo, los elementos de esfuerzo y los círculos de Mohr.

Compilación recomendada:

```bash
pdflatex Punto_8_Solucion_Diseno_Mecanico.tex
pdflatex Punto_8_Solucion_Diseno_Mecanico.tex
```
