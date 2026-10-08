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
- `2026-10-05 | en informes de incidente/postmortem, anonimizar actores a rol ("el cliente", "la empresa") desde el primer borrador, nunca nombres/correos reales | el usuario aclaró que el objetivo es prevención y normativas futuras, no repartir responsabilidad — lo dijo justo cuando Claude Docs bloqueó el borrador por manejo de PII | global, cualquier informe de incidente/postmortem para este usuario o XMS`
- `2026-10-06 | tras confirmar una causa raíz puntual en una investigación de incidente, ampliar proactivamente la auditoría al resto del mismo evento/ventana temporal (ej. revisar el esquema completo) en vez de tratar el primer fix confirmado como el cierre del caso | el hallazgo de 104 tablas corruptas (un proyecto de cliente) solo salió a la luz porque el usuario aportó una consulta externa de information_schema — sin ese aporte, el foco exclusivo en la causa ya confirmada (Action Scheduler) lo habría dejado pasar por alto; el propio usuario lo señaló: "a veces nos enfocamos tanto en un punto que dejamos otros" | global, cualquier investigación de incidente/postmortem en cualquier proyecto`
- `2026-10-07 | atar la verificación de un script/SQL/migración destinado a producción al archivo EXACTO que se va a ejecutar, nunca al patrón o técnica ya probada antes — cualquier cambio de técnica dispara re-verificación automática e inmediata, sin esperar a que se pida | al redactar docs/script-produccion-completo.md (un proyecto de cliente) cambié de técnica respecto a lo ya probado 2 veces (subqueries dinámicas en vez de literales, DELETE por self-join en vez de _rowid manual, sin AUTO_INCREMENT=N explícito) y lo presenté como "production-ready" sin volver a probar ese archivo exacto; el usuario lo clasificó como fallo crítico porque producción no tiene red de seguridad (ALTER TABLE hace COMMIT implícito, sin ROLLBACK) y quien ejecuta el script paga el costo de cualquier técnica no verificada — solo se corrigió porque el usuario lo señaló ("estás variando el proceso"), no porque yo lo detectara primero | global, cualquier script/SQL/migración/código destinado a un entorno real en cualquier proyecto`
- `2026-10-08 | distinguir siempre "el repo" (dev-governance-kit = solo templates publicables, nada vivo) de "el sistema vivo" (shared-agent-rules = la capa que corre en esta máquina): todo archivo del repo es template, el contenido jamás fluye del vivo al repo, y no existe relación derivativa ni sync que documentar | el usuario me corrigió dos veces en la misma sesión — primero al señalar dónde va el persona ("no el correcto es... uno es la implementación el otro el repo") y luego al fijar el principio general ("todo archivo en el repo ES un template no el vivo"); yo había derivado un modelo equivocado de "copia anonimizada con sync unidireccional" que no existe | global, cualquier trabajo sobre gobernanza, el kit o shared-agent-rules en cualquier proyecto`
