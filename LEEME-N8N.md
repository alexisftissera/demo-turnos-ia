# Pasar demo → WhatsApp real (n8n) — 30 min

Trabajás 19-7: hacé esto de día en 3 bloques de 10 min.

## 1. Meta (10 min, gratis)
1. developers.facebook.com → Crear App → WhatsApp → número de PRUEBA.
2. Copiá: `WA_TOKEN` (temporal 24h), `WA_PHONE_ID`, tu `from` para probar.
3. Webhook: `https://TU-N8N/webhook/wa-turnos` → campo `messages`. Verificá con token que inventes.
4. REGLA: nunca automatices el número personal del dueño. Siempre Cloud API oficial o te banean.

## 2. n8n (10 min)
- Cloud ($0 prueba) o self-host: `docker run -d -p 5678:5678 n8nio/n8n`.
- Importar → `n8n-turnos.json` (este repo).
- Variables `.env`: `OPENAI_KEY` (o Claude), `SYSTEM_PROMPT` (copiar `system-prompt.md`), `WA_TOKEN`, `WA_PHONE_ID`, `CAL_ID`, `SHEET_ID`.
- Credenciales: Google Calendar + Sheets (OAuth 1-click).

Flujo: `WA Entrada:index.html:1` → `Normalizar` → `IA Responde` → `Parsear Acción` → `Router` → `Agendar Calendar` / `Log Sheets` / `Enviar WA`.

## 3. Probar (10 min)
1. WA prueba → "quiero turno" → nombre → servicio → día → hora → Confirmar.
2. Ver evento en Google Calendar + fila en Sheets + respuesta WA <1 min.
3. Probá fuera de hora (cambiá hora PC a 23h): debe decir "🌙 te agendo igual".
4. Probá "precio", "dónde quedan", "humano".

## Costo / precio Córdoba 2026
Costo: Meta $15-30 + n8n $0-24 + IA $5-15 = $25-70/mes.
Cobrá: setup $500-900 USD + $150-250/mes. Fijá USD, cobrá ARS día. Recordatorio 24h = -30% ausencias, eso vende solo.

## 3 errores que te queman
1. Prometer 100% autónomo → promete 70% + escala a humano.
2. Sin retainer → se degrada y volvés a cero. Retainer = monitoreo + reporte citas.
3. Sin medir 60 días → mostrá "7 citas recuperadas x $15k = $105k".

Siguiente upsell: reseñas Google + seguimiento cotizaciones (ya tenés Sheets).
