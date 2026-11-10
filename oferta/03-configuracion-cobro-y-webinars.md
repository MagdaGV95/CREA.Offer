# Configuración de la oferta: cobro, thank you page y webinars (10 nov 2026)

Oferta única en el sitio: **Todo comienza contigo**. Decisiones de Magda (10 nov):
- 3 pagos con **pequeño recargo**.
- El paquete deja de estar en la página de venta: pasa a **mejora (upsell) en la thank you page** durante la preventa.
- **Webinar semanal: miércoles 9–10 pm hora de Nueva York**, para presentar la oferta de valor.
- Clases bono del **8 y 29 de diciembre: solo para quienes ya entraron en la preventa** (no se anuncian en la página de venta).
- Cuentas: Stripe, PayPal, Mercado Pago. Stripe se configurará con el conector de Claude cuando Magda lo autorice.

---

## 1. Precios de Todo comienza contigo
| Ventana | Fechas (hora NY) | Contado (USD) | 3 pagos (USD) | Total a plazos |
|---|---|---|---|---|
| Black Friday | vie 27 nov – dom 29 nov | 497 | 3 × 169 | 507 |
| Cyber Monday | lun 30 nov – mié 2 dic | 697 | 3 × 239 | 717 |
| Diciembre | jue 3 dic – sáb 19 dic | 897 | 3 × 309 | 927 |
| Navidad | dom 20 dic – sáb 26 dic | 1,097 | 3 × 379 | 1,137 |
| Último llamado | dom 27 dic – dom 10 ene | 1,297 | 3 × 449 | 1,347 |
| Regular | desde el 11 ene | 1,497 | 3 × 519 | 1,557 |

Cambio de precio: al cierre de cada ventana se cambia el link del botón de compra en la página de venta (o se desactiva el link anterior).

## 2. Mejora en la thank you page (solo preventa)
- Oferta: **"Agrega Lidera tu Hogar (15 mar – 7 may) por 697 USD"** en lugar de 2,497 (ahorras 1,800).
- 3 pagos: 3 × 239.
- Solo se muestra justo después de comprar Todo comienza contigo, hasta el 10 ene.
- Equivale a lo que antes era el paquete (ej. Black Friday: 497 + 697 = 1,194).
- Si se prefiere mantener exactamente 1,167 en Black Friday: mejora a 667 solo ese fin de semana.

## 3. Lidera tu Hogar (no está en el sitio)
- Precio regular 2,497 USD.
- Graduadas: cupón **VICTORIA1000** (−1,000 → 1,497), solo correos que pagaron el nivel 1, 1 uso, vence a los 7 días.

## 4. Qué crear en cada plataforma
### Stripe (con el conector, cuando esté autorizado)
- Producto **Todo comienza contigo**: 6 precios de contado + 6 precios de 3 pagos (mensuales).
- Producto **Lidera tu Hogar**: precio 2,497; precio de mejora 697 (y 3 × 239).
- Cupón de 1,000 USD de descuento fijo, válido solo para Lidera tu Hogar, con código promocional **VICTORIA1000** (vencimiento y límite de usos).
- Un link de pago por cada precio, con correo obligatorio y redirección a la thank you page.
- Plazos: Stripe no detiene solo una suscripción después de 3 cobros desde un link de pago. Opciones: cancelar tras el 3.er cobro (recordatorio o automatización), usar PayPal para los 3 pagos, o activar Affirm/Klarna/Afterpay (clientas de EE. UU.).

### PayPal
- Botón de pago de contado por ventana.
- Plan de suscripción con **3 ciclos** por ventana (se detiene solo).

### Mercado Pago (México)
- Link de pago por ventana, en **pesos mexicanos** (pendiente fijar el tipo de cambio y redondear).
- Meses sin intereses con tarjeta.

## 5. Webinar semanal (miércoles 9–10 pm NY)
| Fecha | Momento | Propósito |
|---|---|---|
| mié 18 nov | antes de la preventa | Presentar el método y abrir lista de espera |
| mié 25 nov | víspera de Thanksgiving | Último aviso antes de Black Friday (o grabado si hay poca asistencia) |
| mié 2 dic | último día de Cyber Monday | Cierre de ventana Cyber Monday |
| mié 9 dic | | Webinar + historias de compradoras |
| mié 16 dic | cierre de ventana diciembre (19 dic) | |
| mié 23 dic | víspera de Nochebuena | Opcional / grabado |
| mié 30 dic | víspera de Año Nuevo | Opcional / grabado |
| mié 6 ene | último llamado | Cierre de inscripciones (10 ene) |

Estructura base: plantilla de Jun Yuh en `evento-conversion/01-plantilla-webinar-jun-yuh.md` (historia → método → 3 módulos → oferta).

## 6. Pendientes de configuración
1. Autorizar el conector de Stripe en claude.ai.
2. Precios en pesos para Mercado Pago.
3. Links de cada ventana en los botones de 2clicks.
4. Correos automáticos: confirmación, acceso a bonos ocultos, recordatorios de clase.
