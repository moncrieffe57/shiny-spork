# Protocolo JMS — Investigación legal Costa Rica

Aplica a TODA consulta o análisis bajo "Protocolo JMS" (normativa, reglamentos,
jurisprudencia, reformas, acuerdos DNN). Sin excepciones.

## 1. Búsqueda obligatoria antes de citar
- Ejecutar `WebSearch` (sin límite de consultas) ANTES de cualquier cita legal.
- Abrir la fuente oficial con `WebFetch` y leer el texto vigente.
- Si una herramienta falla, NO responder "no puedo": intentar la siguiente fuente
  de la lista (sección 2) y reportar exactamente qué dominio quedó bloqueado.
- Usar subagentes (`Agent`) en paralelo cuando la consulta abarque varias normas.

## 2. Fuentes, en orden de prioridad
| # | Fuente | Dominio | Uso |
|---|--------|---------|-----|
| 1 | SCIJ / SINALEVI (PGR) | pgrweb.go.cr, www.pgrweb.go.cr | Texto vigente, reformas, concordancias, dictámenes PGR |
| 2 | Nexus PJ (Poder Judicial) | nexuspj.poder-judicial.go.cr | Jurisprudencia Salas I, II, III, IV y tribunales |
| 3 | Sala Constitucional | salaconstitucional.poder-judicial.go.cr | Votos y acciones de inconstitucionalidad |
| 4 | Poder Judicial (portales) | poder-judicial.go.cr, sitiooij.poder-judicial.go.cr, pjenlinea3.poder-judicial.go.cr | Circulares, códigos compilados, biblioteca |
| 5 | Dirección Nacional de Notariado | www.dnn.go.cr | Lineamientos y acuerdos DNN (cambios 2026 frecuentes) |
| 6 | Imprenta Nacional — La Gaceta | www.imprentanacional.go.cr | Publicación oficial, fecha de vigencia |
| 7 | Asamblea Legislativa | www.asamblea.go.cr | Expedientes de ley, textos aprobados |
| 8 | Registro Nacional | www.rnpdigital.com, www.registronacional.go.cr | Directrices registrales |
| 9 | MTSS / CCSS / Hacienda | www.mtss.go.cr, www.ccss.sa.cr, www.hacienda.go.cr | Laboral, seguridad social, tributario |

Fuentes secundarias (vLex, bufetes, Studocu, PDFs de terceros) sirven solo
para ubicar la norma; nunca son base de la cita final.

## 3. Verificación por cada norma
1. ¿Vigente a la fecha de la consulta?
2. Última reforma: número de ley y fecha de publicación en La Gaceta.
3. ¿Artículos derogados, reformados o anulados por la Sala Constitucional?

## 4. Formato de cita (obligatorio)
`Art. X [Código/Ley], Ley N.° [número] del [fecha], vigente desde [fecha],
última reforma Ley N.° [X] ([fecha Gaceta]). Fuente: [URL oficial], consultada [fecha].`

Jurisprudencia: `[Sala], Resolución N.° [AAAA-NNNNNN], Exp. [NN-NNNNNN-NNNN-XX],
de las [hora] del [fecha]. Fuente: Nexus PJ [URL].` Nunca citar de memoria.

## 5. Niveles de verificación (etiqueta obligatoria en cada cita)
- `[Verificado SCIJ/Nexus]`: texto leído en la fuente oficial en esta sesión.
- `[Verificado fuente secundaria]`: confirmado solo por fuente no oficial; señalar el riesgo.
- `[sin verificar en web]`: no localizado. Va ANTES de la cita, o no se cita.

## 6. Registro
Cada verificación se guarda en `normativa-verificada/[norma].md` (usar
`normativa-verificada/_PLANTILLA.md`) con norma, URL, fecha/hora de consulta y
nivel de verificación, y se añade una línea a `normativa-verificada/LOG.md`.
Nunca incluir nombres de clientes ni datos de expedientes en estos archivos.

## 7. Requisito de red del entorno
El entorno en la nube debe permitir los dominios de la sección 2
(Network access → Custom → Allowed domains, o acceso completo). Si un
dominio aparece como `EGRESS_BLOCKED`, informarlo de inmediato a Jorge
indicando el dominio exacto.
