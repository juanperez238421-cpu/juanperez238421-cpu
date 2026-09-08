# Punto 8 — Taller 1 Diseño Mecánico 2026-2

Solución desarrollada paso a paso a partir del diagrama del punto 8 del taller.

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

## Resultados

| Magnitud | Punto A | Punto B |
|---|---:|---:|
| Esfuerzo normal | +5.732 ksi | -2.268 ksi |
| Esfuerzo cortante transversal | 0 | 0 |
| Esfuerzos principales | (5.732, 0, 0) ksi | (0, 0, -2.268) ksi |
| Cortante máximo | 2.866 ksi | 1.134 ksi |
| von Mises | 5.732 ksi | 2.268 ksi |
| Factor de seguridad | 6.98 | 17.64 |

La condición crítica corresponde al **punto A**, con `n ≈ 6.98`.

## Archivo fuente

- `Punto_8_Solucion_Diseno_Mecanico.tex`

El documento usa LaTeX + TikZ para reconstruir de forma profesional el diagrama, el cuerpo libre, la sección transversal, la distribución de esfuerzo, los elementos de esfuerzo y los círculos de Mohr.

Compilación recomendada:

```bash
pdflatex Punto_8_Solucion_Diseno_Mecanico.tex
pdflatex Punto_8_Solucion_Diseno_Mecanico.tex
```
