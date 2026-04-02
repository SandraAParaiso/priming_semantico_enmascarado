# Priming Semántico Enmascarado — Tarea de Decisión Léxica

Experimento de priming semántico enmascarado basado en la **Tarea de Decisión Léxica (TDL)** que se ejecuta íntegramente en un único archivo HTML, sin dependencias externas, servidor ni instalación. Compatible con ordenador, tablet y móvil.

---

## Paradigma

Cada ensayo sigue la secuencia estándar del priming enmascarado:

| Fase | Duración |
|---|---|
| Cruz de fijación | 400 ms |
| Máscara forward (`####`) | 500 ms |
| Prime (subliminal) | 55 ms |
| Máscara backward | 32 ms |
| Target | 200 ms |
| Máscara post-target | hasta respuesta |
| Respuesta (SÍ / NO) | libre |

El target desaparece antes de que se abra la ventana de respuesta, de modo que el participante responde desde la memoria — el procedimiento estándar en los estudios de TDL enmascarada. El tiempo de reacción se mide desde el inicio de la ventana de respuesta.

---

## Tarea

El participante decide lo más rápidamente posible si la cadena de letras que acaba de ver es una **palabra real** del español (SÍ) o una **pseudopalabra** inventada (NO). En ordenador también se puede responder con teclado (`S` / `N` o las teclas de flecha).

Los tres bloques experimentales se presentan sin etiquetas — el participante no conoce el tipo de relación prime-target, evitando así la contaminación estratégica.

---

## Diseño experimental

Tres bloques intra-sujeto de 12 ensayos cada uno (36 ensayos en total). Los ensayos se aleatorizan dentro de cada bloque.

| Bloque | Condición | Ejemplo |
|---|---|---|
| I | Semántico + asociativo | PERRO → GATO |
| II | Solo asociativo | ARAÑA → TELA |
| III | Solo semántico | DELFÍN → BALLENA |

Cada bloque contiene:
- 4 ensayos **congruentes** (prime relacionado + target palabra real)
- 4 ensayos **incongruentes** (prime no relacionado + target palabra real)
- 4 ensayos **relleno** (prime cualquiera + pseudopalabra)

La medida crítica es el **efecto de priming**: la diferencia de TR entre los ensayos incongruentes y los congruentes. Una diferencia positiva indica activación semántica subliminal por parte del prime.

---

## Pantalla de resultados

Al finalizar los 36 ensayos, el participante ve:

- Tarjetas resumen por bloque con precisión (%) y TR medio (ms) para las condiciones congruente e incongruente por separado
- Gráfico de barras — precisión por condición y bloque
- Gráfico de barras — TR medio (solo respuestas correctas) por condición y bloque
- Interpretación automática del mayor efecto de priming observado

---

## Uso

No requiere instalación. Descarga `priming_semantico.html` y ábrelo en cualquier navegador moderno.

```bash
git clone https://github.com/tu-usuario/priming-semantico-enmascarado
open priming_semantico.html
```

Probado en Chrome, Firefox y Safari (escritorio y móvil).

---

## Estímulos

Todos los estímulos están en español. Las palabras prime y target son sustantivos comunes del español emparejados aproximadamente en longitud y frecuencia dentro de cada condición. Las pseudopalabras son violaciones fonológicas mínimas de palabras reales (p. ej. *GAMO*, *TENORO*, *BALLENO*) para mantener la dificultad de la decisión léxica.

---

## Limitaciones

- El número de ensayos por celda es reducido (4 por celda) — suficiente para demostración pero no para inferencia estadística publicable.
- No está implementado el guardado de datos ni la exportación de resultados; los resultados se muestran únicamente en pantalla.
- El TR se mide con `performance.now()`, con una precisión aproximada de 1 ms en la mayoría de entornos, aunque sujeto a la variabilidad del planificador del sistema operativo.
- El experimento está en español; para adaptarlo a otro idioma basta con editar el array `PHASES` en la sección de script.

---

## Referencias

Forster, K. I., & Davis, C. (1984). Repetition priming and frequency attenuation in lexical access. Journal of experimental psychology: Learning, Memory, and Cognition, 10(4), 680.

Neely, J. H. (2012). Semantic priming effects in visual word recognition: A selective review of current findings and theories. Basic processes in reading, 264-336.

Deacon, D., Hewitt, S., Yang, C. M., & Nagata, M. (2000). Event-related potential indices of semantic priming using masked and unmasked words: evidence that the N400 does not reflect a post-lexical process. Cognitive Brain Research, 9(2), 137-146.
