# Cierre → Cobro → Entrega (10 días)

## Día 0: cerrar (en el local, 15 min)
1. Mostrar demo + ROI con sus números. Cerrar con: "¿Lo activamos en tu WhatsApp en 10 días?"
2. Precio Córdoba 2026: Setup $500-900 USD + retainer $150-250/mes. Seña 50% hoy (USD fijo, ARS cambio día, transferencia/Wise).
3. Papel 1 carilla: alcance (1 flujo turnos), fecha entrega, retainer desde día 1, vos tenés acceso a cuentas. Firmas foto WhatsApp.

## Día 1: pedir accesos (WhatsApp mensaje)
- [ ] Email Google del dueño (Calendar + Sheets)
- [ ] Número del negocio (chip/eSIM, NO personal) + acceso Meta Business Manager (admin)
- [ ] Lista servicios + precios + horarios + dirección + fotos local
- [ ] 10 preguntas frecuentes reales (copiar de su WhatsApp)

## Día 2-4: armar (2h/noche después turno 19-7)
1. Duplicar `n8n-turnos.json` → renombrar `cliente-X`.
2. Pegar `system-prompt.md` con sus datos. Cambiar NEGOCIO, SERVS, horarios.
3. Meta App → WA_PHONE_ID + WA_TOKEN en `.env`. Calendar `CAL_ID`, Sheets `SHEET_ID`.
4. Importar en n8n (cloud $0 prueba o tu VPS). Webhook `/wa-turnos-X`.

## Día 5-7: probar con él
- Número prueba Meta → 5 casos: turno ok, precio, horario, humano, fuera hora 23h.
- Calendar + Sheets ok + recordatorio 24h (Schedule Trigger).
- Ajustar tono con dueño (1 call 20 min).

## Día 8-10: pasar a real + cobrar
1. Migrar webhook al número oficial. 1 turno real con dueño al lado.
2. Cobrar 50% restante + primer retainer. Entregar: link Calendar, Sheet Turnos, video 2 min cómo leer panel.
3. Pedir 2 referidos: "¿a quién le pasa esto mismo?" + reseña Google + permiso caso.

## Reglas que te salvan
- Nunca número personal. Solo Cloud API oficial.
- Retainer = monitoreo + reporte citas/mes, no "mantenimiento".
- Prometé 70% auto + humano, no 100%.
- Todo en TUS cuentas n8n/Cloudflare, acceso para él viewer. Si se va, apagás.
- Upsell mes 2: reseñas Google ($60-120/mes) + seguimiento cotizaciones ($100-180/mes).
