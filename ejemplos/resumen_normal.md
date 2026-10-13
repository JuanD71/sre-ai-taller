# Informe de observabilidad y AIOps (laboratorio sintético)

- Solicitudes evaluadas: **120**
- SLI (solicitud 2xx/3xx con latencia < 200 ms): **100.00%**
- SLO del ejercicio: **99%**; estado: **CUMPLE**
- Latencia p95: **121 ms**
- Presupuesto de solicitudes malas: **1.2**
- Solicitudes malas observadas: **0**
- Anomalías IsolationForest: **3** (2.50%)
- Eventos de auditoría simulados: **0**
- Incidente propuesto: **False**, severidad **sin-incidente**
- Respuesta: **triaje y documentación; ninguna contención automática**

## Observaciones y límites

El modelo IsolationForest ofrece detección estadística, no causalidad ni evidencia definitiva de ataque. El evento de auditoría es ficticio y está marcado como autorizado para fines didácticos.
MTTD y MTTR no se miden con la ejecución por lotes.

## Correlación de trazas

Consultar `datos/trazas.jsonl` por `trace_id` de `ejemplos_trazas_anomalas` en `resultados/informe.json`. Los spans son **simulados**, no exportaciones OTLP de OpenTelemetry.

## Revisión humana / cierre

- [ ] Verificar si el cambio estaba autorizado
- [ ] Revisar `trace_id`, solicitudes y degradación del SLI
- [ ] Proponer acción correctiva reversible (sin ejecutarla)
- [ ] Registrar hipótesis, responsable y postmortem
