# Demo Bot Turnos — para vender automatización

Negocio ficticio: **Barbería Centro Córdoba** (sirve para peluquería, consultorio, taller).

## Archivos
- `index.html` → demo completa (landing + chat + panel). Sin build, deploy gratis en Cloudflare Workers.

## Cómo mostrarla (30 seg)
1. `powershell -ExecutionPolicy Bypass -File servir-demo.ps1` o abrir `index.html`
2. En el celular del cliente: tocar "Reservar por WhatsApp" → el bot pide nombre → servicio → día → hora → confirma.
3. Mostrar panel: "Ver turnos" → se guardó solo, listo para recordar por WhatsApp.
4. Cierre: "Esto mismo lo conecto a tu WhatsApp real + Google Calendar. Sin que atiendas el teléfono."

## Qué decir (guion)
- "¿Cuántos turnos perdés por no contestar a tiempo?" → dejar que responda.
- "Este bot atiende 24/7, confirma y manda recordatorio. Vos solo cortás pelo."
- Precio ancla Córdoba 2026: setup $150-250k ARS + abono $50-80k/mes. Ofrecer 7 días prueba.

## Pasar a real (después que paga)
1. Copiar `index.html` → Cloudflare Worker estático.
2. Conectar n8n + WhatsApp API + Google Calendar (ya tenés el stack en tu CV).
3. Cambiar nombre, servicios, horarios, `wa.me/351...` por el del cliente.
