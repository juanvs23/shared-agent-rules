# Feedback Ledger — Zero-Infra Mirror for Profile A Memory

> This file is the filesystem floor for **Profile A** feedback (see
> `development-rules.md` rule 12 and `MANIFESTO.md`): a process correction or
> confirmation tied to a documented incident, a repeated violation, or a
> standing decision — cross-project by nature, not tied to one repo.
>
> It exists so this specific class of memory survives even when no external
> memory backend is configured or reachable, in any runtime (Claude Code,
> OpenCode, or another). It plays the same role `PERSONA.md` plays for
> conversational voice — same dated-ledger format, same reasoning: a flat
> file has no MCP server to go down.
>
> **When to write here:** every time a `feedback`-type (or causally-justified
> `decision`/`architecture`-type) memory is saved to external memory and it
> qualifies as Profile A, mirror it here in the same action — dual-write, not
> instead-of.
>
> **Format:** `fecha | regla | por qué (incidente/causa) | alcance`

## Registro

<!-- autoescrito por el agente; no reordenar ni reescribir entradas existentes, solo agregar -->

- `2026-10-04 | redactar reglas/archivos always-on compactos desde el primer borrador, no recién al pedírmelo | pidió reducir verbosidad dos veces en la misma sesión (regla 10, luego regla 3) sin perder sustancia — el propio MANIFESTO.md ya establece que cada línea en estos archivos tiene costo recurrente por sesión, principio que no apliqué por defecto al redactar | global, cualquier archivo always-on en cualquier proyecto`
- `2026-10-04 | las reglas deben abrir con una frase imperativa determinista ("Don't trust X"), nunca con un título descriptivo que pueda leerse de más de una forma | malinterpreté la regla 6 original (la leí como redundante con la 5) porque su apertura era ambigua — si el análisis cuidadoso del propio modelo la malinterpreta, la regla ya falló antes de llegar a cualquier tarea real; determinismo en la apertura pesa más que brevedad | global, cualquier archivo de reglas en cualquier proyecto`
- `2026-10-04 | validar claridad de una regla con un cold-read aislado: un modelo chico (Haiku), sin contexto, sin ver las reglas relacionadas una al lado de la otra, parafraseando qué/cuándo/por qué con sus propias palabras | mostrar las reglas juntas deja que el modelo infiera la distinción por yuxtaposición de redacción en vez de que cada regla se sostenga sola — que es la condición real cuando se aplica una regla aislada en una tarea | global, técnica de validación para cualquier archivo de reglas`
