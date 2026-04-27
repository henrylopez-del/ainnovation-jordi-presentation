# Test Mascota A/B/C — Prompts ordenados (mascotas → stock → solo texto)

> Test de personaje sobre 4 ads piloto: D1-01, D1-02, D1-03, D2-10
> Orden de producción: primero todas las mascotas (A), luego todas las stock (B), al final solo texto (C — control existente)

## Reglas del test (corrección crítica 2026-04-26)

- **Variantes A y B son ADICIONES al ad original — NO rediseños.**
- **Mismo background brand del ad original** (NO negro). Cada vertical tiene su color: violet / magenta / navy.
- **Mismo copy literal del ad original** (NO sustituir, NO abreviar).
- **Mismo layout, brand sandwich, tipografía, paleta** del ad original.
- **Solo cambia:** la zona decorativa bottom (y=1280-1920) que antes tenía wavy pattern, ahora tiene mascota (variante A) o stock photo (variante B).
- **Adición debe ser RELATABLE al buyer del ad** — mascota con shenanigans contextuales o stock con persona contextual al persona del ad.

| Variante | Adición visual | Background | Posición de adición |
|---|---|---|---|
| **A · Los AI** | Mascota A&I haciendo shenanigans relatable al buyer | MISMO brand del ad original | Bottom decorative zone (y=1280-1920) |
| **B · Stock** | Persona stock relatable al buyer persona del ad | MISMO brand del ad original | Bottom decorative zone (y=1280-1920) |
| **C · Control** | Sin adición — el ad original con su wavy pattern | MISMO brand del ad original | (ya existe — no requiere prompt nuevo) |

## Specs comunes para Los AI (variante A)

- Personajes: las letras "A" y "I" del wordmark vivas — cuerpo blanco geométrico flat
- Caras: 2 puntos negros (eyes) + 1 línea negra recta (mouth), nada más
- Sin ropa, sin manos detalladas, sin género
- Brazos y piernas: líneas blancas finas
- Estilo: pictogramas Otl Aicher 1972 / Linear / Anthropic abstracto
- Tamaño: ~480px tall, posicionados en bottom decorative zone
- Shenanigans: contextual al copy del ad — la mascota "ejecuta" o "celebra" lo que el copy promete

## Specs comunes para Stock model (variante B)

- 1 sola persona representativa del buyer persona del ad
- Sonriendo natural (no toothy, no forced)
- Vestimenta casual profesional acorde al persona
- Sin objetos de marca visibles (no Apple, Samsung, Coca-Cola)
- Sin props que distraigan (no laptop, no celular, no oficina)
- Foto realista, NO ilustrada NO 3D NO cartoon
- Tamaño: media silueta cropped, posición bottom decorative zone
- Etnia: latino mexicano (todos los ads son México)

## Status de producción

| Cluster | Ad piloto | Variante A (Los AI) | Variante B (Stock) | Variante C (Solo texto) |
|---|---|---|---|---|
| General | D1-01 | ⏳ pendiente (Prompt #1) | ✅ ya generada | ✅ existe (control) |
| Belleza | D1-02 | ⏳ pendiente (Prompt #2) | ⏳ pendiente (Prompt #5) | ✅ existe (control) |
| Retail | D1-03 | ⏳ pendiente (Prompt #3) | ⏳ pendiente (Prompt #6) | ✅ existe (control) |
| Premium | D2-10 | ⏳ pendiente (Prompt #4) | ⏳ pendiente (Prompt #7) | ✅ existe (control) |

= 7 prompts pendientes (4 variante A + 3 variante B). Variante C no requiere prompt nuevo — es el ad original.

---

# SECCIÓN 1 · MASCOTAS (Variante A — Los AI) · 4 prompts

---

## Prompt #1 · D1-01 EL DATO (General) · Variante A — Los AI

```
[FORMAT] Advertisement poster, 1080x1920px vertical Meta Stories/Reels, 9:16, mobile-first, flat vector editorial.

[BASE — TOMAR AD ORIGINAL D1-01 EXACTAMENTE COMO ESTÁ]
- Background: solid violet electric #8B5CF6 (todo el canvas)
- y=60: "AINNOVATION" wordmark Open Sauce One Bold 14pt tracked +200 white 80% centered
- y=180: eyebrow "UN VENDEDOR AI. UN MES. UN NEGOCIO EN MÉXICO." Open Sauce One Medium 22pt caps pink pastel #F8C8DC tracked +80 centered
- y=240: hairline white separator 120px centered
- y=310-620: hero number "1,532" Clash Display 360pt white centered tight tracking
- y=640: sub-label "mensajes contestados" Open Sauce One Medium 28pt caps pink pastel centered
- y=720: hairline separator
- y=760-920: 3 stats: "87 citas agendadas" / "541 follow-ups" / "24/7" — Clash Display 72pt white + label Open Sauce One 22pt caps pink pastel
- y=960: hairline separator
- y=1000-1080: price "$1,999/mes" Clash Display 120pt white centered
- y=1200-1260: brand footer "AINNOVATION" Clash Display 38pt white + "ARTIFICIAL / INTELLIGENCE / FOR BUSINESS" Open Sauce One Bold 12pt caps pink pastel tracked +300

[ADITION — Bottom decorative zone (y=1280-1920) — REEMPLAZAR wavy pattern original con Los AI]
- "A" character at x=120-340, y=1340-1820, ~480px tall: white triangular A-letter shaped body with thin white legs and arms. 2 black dot eyes + 1 short black line mouth in slight "wide eyes overwhelmed" expression. A is leaning back, arms thrown wide trying to catch a cascade of ~15 small white square chat-bubble shapes (with rounded corners, thin violet outline) flying down from above. Some bubbles bounce off A's outstretched arms and scatter mid-air around her.
- "I" character at x=740-960, y=1340-1820, ~480px tall: white rectangular I-letter shaped body with thin white legs and arms. 2 black dot eyes + 1 short line mouth in slight upward curve (subtle smirk). I is standing calm, holding ONE big white chat-bubble in one raised hand, casually replied with a thin white "✓" check mark inside the bubble.
- Implies: while A panics with the volume of 1,532 messages, I handles them effortlessly. Visual storytelling of the hero number.

[BACKGROUND] Solid violet electric #8B5CF6 across full canvas. Bottom third stays violet (no wavy pattern — characters and chat bubbles take that space). NO cambiar a negro NI a otro color.

[TYPOGRAPHY] Mantener fonts del ad original. No drop shadows. Cero modificaciones.

[EXACT TEXT TO RENDER]
"AINNOVATION"
"UN VENDEDOR AI. UN MES. UN NEGOCIO EN MÉXICO."
"1,532"
"mensajes contestados"
"87 citas agendadas"
"541 follow-ups"
"24/7"
"$1,999/mes"
"AINNOVATION"
"ARTIFICIAL / INTELLIGENCE / FOR BUSINESS"

[STYLE] Flat vector editorial poster. Brutalist swiss del ad original + character vignette en zona decorativa bottom. Linear/Vercel/Anthropic minimalism con storytelling visual.

[RENDER ONLY TEXT FROM EXACT TEXT TO RENDER] Do not render font names, point sizes, pixel coordinates, hex codes, tracking values, percentages as visible text.

[NEGATIVE] NO modificar el ad original (copy, layout, brand sandwich, paleta). NO cambiar background a negro. NO 1:1 ni 4:5. NO 3D. NO drop shadows. NO realistic faces — caras de personajes ÚNICAMENTE 2 dots + 1 line. NO ropa, NO manos detalladas. NO emoji. Las chat bubbles deben ser flat geometric (squares con rounded corners), NO realistic chat UI screenshots.
```

---

## Prompt #2 · D1-02 BELLEZA (Una Semana) · Variante A — Los AI

```
[FORMAT] Advertisement poster, 1080x1920px vertical Meta Stories/Reels, 9:16, mobile-first, flat vector editorial.

[BASE — TOMAR AD ORIGINAL D1-02 EXACTAMENTE COMO ESTÁ]
- Background: solid magenta #E040FB (todo el canvas)
- y=60: "AINNOVATION" wordmark Open Sauce One Bold 14pt tracked white 80% centered
- y=170-220: eyebrow "UN SALON DE BELLEZA · UN VENDEDOR AI · UNA SEMANA" Open Sauce One Medium 20pt caps pink pastel #F8C8DC centered, two lines
- y=250: hairline white separator 120px
- y=310-1090: 2x2 stats grid 980x780px divided by hairline white cross
  - TL "184" Clash Display 220pt white + "mensajes contestados" Open Sauce One Medium 22pt caps pink pastel
  - TR "23" Clash Display 220pt white + "citas agendadas" Open Sauce One Medium 22pt caps pink pastel
  - BL "7" Clash Display 220pt white + "clientas recuperadas" Open Sauce One Medium 22pt caps pink pastel
  - BR "0" Clash Display 220pt navy #1A1A2E + "veces que la dueña tocó el teléfono" Open Sauce One Medium 20pt caps navy
- y=1120: hairline separator
- y=1140-1200: price "$1,999/mes" Clash Display 88pt white centered
- y=1215-1270: brand footer "AINNOVATION" Clash Display 34pt white + "ARTIFICIAL / INTELLIGENCE / FOR BUSINESS" Open Sauce One Bold 11pt caps pink pastel tracked

[ADITION — Bottom decorative zone (y=1280-1920) — REEMPLAZAR wavy pattern original con Los AI]
- "A" character at x=80-280, y=1340-1820, ~480px tall: white triangular A-letter body, 2 black dot eyes + 1 line mouth (focused little frown). A is mid-sweep with a thin white outline broom angled at 45 degrees, a tiny pile of white dots/dust at the broom tip. The salon is being cleaned at night.
- "I" character at x=820-1020, y=1340-1820, ~480px tall: white rectangular I-letter body, same minimal face but mouth a tiny upward curve (warm smile). I is holding up a small white chat-bubble shape in one raised arm — the bubble has a small white "♥" heart-shape inside (replied to a client lovingly). Other arm holds a small flat outline of a calendar/agenda icon (booked the appointment).
- Implies: while the dueña sleeps, A&I run the salon — A cleans, I responds to clients with care and books appointments. Visual storytelling of "0 veces que la dueña tocó el teléfono".

[BACKGROUND] Solid magenta #E040FB across full canvas. Bottom third stays magenta (no wavy pattern — characters and props take that space). NO cambiar a negro.

[TYPOGRAPHY] Mantener fonts del ad original. No drop shadows.

[EXACT TEXT TO RENDER]
"AINNOVATION"
"UN SALON DE BELLEZA · UN VENDEDOR AI · UNA SEMANA"
"184"
"mensajes contestados"
"23"
"citas agendadas"
"7"
"clientas recuperadas"
"0"
"veces que la dueña tocó el teléfono"
"$1,999/mes"
"AINNOVATION"
"ARTIFICIAL / INTELLIGENCE / FOR BUSINESS"

[STYLE] Flat vector editorial poster, brutalist-swiss del ad original + character vignette femenino-aspiracional en zona decorativa. Premium feminine sin kitsch.

[RENDER ONLY TEXT FROM EXACT TEXT TO RENDER]

[NEGATIVE] NO modificar el ad original. NO cambiar background a negro. Caras de personajes ÚNICAMENTE 2 dots + 1 line. NO ropa, NO manos detalladas. NO emoji (el ♥ es flat unicode-style, no emoji). NO realistic broom — flat outline. NO 1:1 ni 4:5. NO 3D. NO realistic faces.
```

---

## Prompt #3 · D1-03 RETAIL (150 → 12) · Variante A — Los AI

```
[FORMAT] Advertisement poster, 1080x1920px vertical Meta Stories/Reels, 9:16, mobile-first, flat vector editorial.

[BASE — TOMAR AD ORIGINAL D1-03 EXACTAMENTE COMO ESTÁ]
- Background: solid navy #1A1A2E (todo el canvas)
- y=60: "AINNOVATION" wordmark Open Sauce One Bold 14pt white 80% centered
- y=170: eyebrow "TU NUEVO FUNNEL DE VENTAS" Open Sauce One Medium 22pt caps violet #8B5CF6 centered
- y=220: hairline white separator 120px
- y=270-350: Node 1 card rounded rect 2px violet stroke 880x80px "150 mensajes al dia" Clash Display 44pt white centered
- y=370: down arrow ↓ violet 40pt centered
- y=410-500: Node 2 card 880x90px "Tu vendedor AI contesta los 150 en 60 seg" Open Sauce One Bold 26pt white centered
- y=520: down arrow ↓ violet
- y=560-640: Node 3 card 880x80px "Califica cada uno automaticamente" Open Sauce One Bold 26pt white centered
- y=660: down arrow ↓ violet
- y=700-840: Node 4 card HIGHLIGHT 880x140px solid violet #8B5CF6 fill "Solo 12 llegan a ti:" Clash Display 42pt white + "los que quieren comprar" Open Sauce One Bold 28pt white
- y=880: hairline separator
- y=910-990: price "$1,999/mes. Tu solo cierras." Clash Display 56pt white centered
- y=1020-1090: CTA strip "MANDA DEMO" full-width violet band Clash Display 58pt caps white centered
- y=1120-1270: brand footer "AINNOVATION" + tagline pink pastel

[ADITION — Bottom decorative zone (y=1280-1920) — REEMPLAZAR "138" watermark con Los AI]
- "A" character at x=60-260, y=1340-1820, ~480px tall: white triangular A-letter body, 2 black dot eyes + 1 line mouth (serious bouncer face, no smile). A stands in side profile facing right, one arm extended FORWARD with palm out blocking entry. A small group of ~5-7 tiny white square chat-bubble shapes bounce off A's outstretched palm and scatter backward (away from the screen).
- "I" character at x=820-1020, y=1340-1820, ~480px tall: white rectangular I-letter body, same minimal face but mouth slight smirk. I stands in side profile facing the opposite direction (left), one arm extended FORWARD pointing/welcoming a single tiny white chat-bubble shape forward (toward the right edge). The bubble has a tiny white "$" symbol inside (the buyer that passed the filter).
- Together they form a visual "filter": A rejects, I welcomes the one buyer. Implies "bouncers separating signal from noise" — exactamente el concepto FILTRO 150 → 12 del ad.

[BACKGROUND] Solid navy #1A1A2E across full canvas. Bottom third stays navy. NO cambiar a negro (navy ya es navy, mantener navy del ad original).

[TYPOGRAPHY] Mantener fonts del ad original.

[EXACT TEXT TO RENDER]
"AINNOVATION"
"TU NUEVO FUNNEL DE VENTAS"
"150 mensajes al dia"
"Tu vendedor AI contesta los 150 en 60 seg"
"Califica cada uno automaticamente"
"Solo 12 llegan a ti:"
"los que quieren comprar"
"$1,999/mes. Tu solo cierras."
"MANDA DEMO"
"AINNOVATION"
"ARTIFICIAL / INTELLIGENCE / FOR BUSINESS"

[STYLE] Flat vector editorial engineering diagram (parte superior — el ad original) + character vignette de bouncers (parte inferior). Surgical clarity. La metáfora del bouncer materializa el concepto FILTRO.

[RENDER ONLY TEXT FROM EXACT TEXT TO RENDER]

[NEGATIVE] NO modificar el ad original. NO realistic security uniforms — characters stay en sus letter shapes. Caras ÚNICAMENTE 2 dots + 1 line. NO ropa. NO 1:1 ni 4:5. NO 3D. NO drop shadows. Chat bubbles flat geometric, NO realistic UI.
```

---

## Prompt #4 · D2-10 SISTEMA COMPLETO $4,999 · Variante A — Los AI

```
[FORMAT] Advertisement poster, 1080x1920px vertical Meta Stories/Reels, 9:16, mobile-first.

[BASE — TOMAR AD ORIGINAL D2-10 EXACTAMENTE COMO ESTÁ]
- Background: solid violet electric #8B5CF6 (todo el canvas)
- y=60: "AINNOVATION" wordmark Clash Display 38px letter-spacing 6px white top-centered
- y=120-150: eyebrow "NIVEL 2: EL SISTEMA COMPLETO" Open Sauce One Bold 24px pink pastel #F8C8DC letter-spacing 4px centered
- y=190-240: headline line 1 "CONTESTAR WHATSAPP" Clash Display 68px white centered
- y=245-295: headline line 2 "ES SOLO EL PRINCIPIO." Clash Display 68px white centered
- y=340-500: questions stack 4 lines Open Sauce One Bold 28px white centered, each ending with HUGE Clash Display 60px magenta #E040FB "?":
  "CUÁNTOS LEADS LLEGARON ESTA SEMANA?"
  "CUÁNTOS COMPRARON?"
  "CUÁNTOS SE FUERON?"
  "DE DONDE VINIERON?"
- y=530-580: punchline "SI NO SABES, NO TIENES SISTEMA." Clash Display 44px white centered
- y=610-680: price "$4,999/MES." Clash Display 96px magenta #E040FB centered
- y=720-1080: feature grid 2x3, 6 cells, monoline white icons + labels Open Sauce One Bold 26px white: TODOS LOS CANALES / PIPELINE / DASHBOARD / 3 FOLLOW-UPS / BROADCASTS / NO-SHOWS
- y=1110-1170: CTA pill "MANDA SISTEMA." magenta #E040FB rounded rect, white Open Sauce One Bold 34px
- y=1220: "AINNOVATION" wordmark Clash Display 32px white centered
- y=1252: tagline "ARTIFICIAL / INTELLIGENCE / FOR BUSINESS" Open Sauce One Regular 14px pink pastel centered

[ADITION — Bottom decorative zone (y=1280-1920) — REEMPLAZAR wavy pattern original con Los AI]
- "A" character at x=200-440, y=1320-1820, ~500px tall: white triangular A-letter body, 2 black dot eyes + 1 line mouth in tiny upward curve (joyful celebration). A is mid-jump in the air, slightly tilted, body angled toward the right (toward I), one arm raised diagonally up-right reaching for a high-five. Both legs bent mid-air showing motion. A small dashed white motion arc behind A indicating jump trajectory.
- "I" character at x=640-880, y=1320-1820, ~500px tall: white rectangular I-letter body, same minimal face with tiny upward smile. I is also mid-jump, mirrored — slightly tilted body angled toward the left (toward A), one arm raised diagonally up-left reaching for the same high-five. Their hands meet at the apex around x=540 y=1380 with a small white "BAM" star-burst shape (4-pointed flat star) at the contact point.
- Implies: A&I celebrando un cierre de venta. La celebración del Sistema Completo funcionando. Para audiencia premium $4,999, la mascota representa "esto es lo que se siente cerrar con el sistema".

[BACKGROUND] Solid violet electric #8B5CF6 across full canvas. Bottom third stays violet (no wavy pattern — characters take that space). NO cambiar a negro.

[TYPOGRAPHY] Mantener fonts del ad original.

[EXACT TEXT TO RENDER]
"AINNOVATION"
"NIVEL 2: EL SISTEMA COMPLETO"
"CONTESTAR WHATSAPP"
"ES SOLO EL PRINCIPIO."
"CUÁNTOS LEADS LLEGARON ESTA SEMANA?"
"CUÁNTOS COMPRARON?"
"CUÁNTOS SE FUERON?"
"DE DONDE VINIERON?"
"SI NO SABES, NO TIENES SISTEMA."
"$4,999/MES."
"TODOS LOS CANALES"
"PIPELINE"
"DASHBOARD"
"3 FOLLOW-UPS"
"BROADCASTS"
"NO-SHOWS"
"MANDA SISTEMA."
"AINNOVATION"
"ARTIFICIAL / INTELLIGENCE / FOR BUSINESS"

[STYLE] Flat vector editorial SaaS dashboard poster (parte superior — el ad original) + character celebration vignette (parte inferior). Linear/Vercel/Anthropic minimalism con character joy. Premium tier visual.

[RENDER ONLY TEXT FROM EXACT TEXT TO RENDER]

[NEGATIVE] NO modificar el ad original. Caras de personajes ÚNICAMENTE 2 dots + 1 line. NO ropa, NO manos detalladas. El "BAM" burst es flat 4-pointed star, NO comic-book bubble NO text. NO 1:1 ni 4:5. NO 3D. NO drop shadows. NO emoji.
```

---

# SECCIÓN 2 · STOCK MODELS (Variante B) · 3 prompts

> Nota: D1-01 Variante B ya fue generada. Solo restan D1-02, D1-03, D2-10.

---

## Prompt #5 · D1-02 BELLEZA (Una Semana) · Variante B — Stock model

```
[FORMAT] Advertisement poster, 1080x1920px vertical Meta Stories/Reels, 9:16, mobile-first.

[BASE — TOMAR AD ORIGINAL D1-02 EXACTAMENTE COMO ESTÁ]
- Background: solid magenta #E040FB (todo el canvas)
- y=60: "AINNOVATION" wordmark Open Sauce One Bold 14pt tracked white 80% centered
- y=170-220: eyebrow "UN SALON DE BELLEZA · UN VENDEDOR AI · UNA SEMANA" Open Sauce One Medium 20pt caps pink pastel #F8C8DC centered, two lines
- y=250: hairline white separator 120px
- y=310-1090: 2x2 stats grid 980x780px divided by hairline white cross
  - TL "184" Clash Display 220pt white + "mensajes contestados" Open Sauce One Medium 22pt caps pink pastel
  - TR "23" Clash Display 220pt white + "citas agendadas" Open Sauce One Medium 22pt caps pink pastel
  - BL "7" Clash Display 220pt white + "clientas recuperadas" Open Sauce One Medium 22pt caps pink pastel
  - BR "0" Clash Display 220pt navy #1A1A2E + "veces que la dueña tocó el teléfono" Open Sauce One Medium 20pt caps navy
- y=1120: hairline separator
- y=1140-1200: price "$1,999/mes" Clash Display 88pt white centered
- y=1215-1270: brand footer "AINNOVATION" Clash Display 34pt white + "ARTIFICIAL / INTELLIGENCE / FOR BUSINESS" Open Sauce One Bold 11pt caps pink pastel tracked

[ADITION — Bottom decorative zone (y=1280-1920) — REEMPLAZAR wavy pattern original con stock model]
- 1 stock photo: Latin Mexican woman, age 28-42, dueña de salón de belleza. Casual professional attire (plain t-shirt or button-up — NO uniforme branded, NO bata de spa). Sonrisa natural confident, NO toothy, NO forced. Mirando ligeramente off-camera con expresión "satisfecha pero descansada" (la dueña que ya delega). Hair styled but not over-the-top. Skin tone natural Latin/Mexican (medio).
- Photo cropped vertical: head-to-mid-torso shot, x=300-780, y=1340-1900, taking up the bottom decorative zone
- Diversidad: NO la "Mariana cliché blanca delgada joven". Tipo de cuerpo natural, edad rangeada 28-42 (preferentemente 32-38, más relatable a la mayoría de Marianas reales del mercado mexicano)
- Background del stock photo: blend con el magenta #E040FB del ad — fondo neutro magenta o studio gris suave que se mezcle con el brand color
- NO props (no celular, no laptop, no tijeras, no implementos de salón) — la persona se vende sola

[BACKGROUND] Solid magenta #E040FB across full canvas. Bottom third con stock photo integrada al magenta brand. NO cambiar a negro.

[TYPOGRAPHY] Mantener fonts del ad original.

[EXACT TEXT TO RENDER]
"AINNOVATION"
"UN SALON DE BELLEZA · UN VENDEDOR AI · UNA SEMANA"
"184"
"mensajes contestados"
"23"
"citas agendadas"
"7"
"clientas recuperadas"
"0"
"veces que la dueña tocó el teléfono"
"$1,999/mes"
"AINNOVATION"
"ARTIFICIAL / INTELLIGENCE / FOR BUSINESS"

[STYLE] Flat vector editorial poster (parte superior — el ad original) + photographic stock hero (parte inferior — adición). Premium feminine sin kitsch. Stock photo integrada visualmente al brand magenta.

[RENDER ONLY TEXT FROM EXACT TEXT TO RENDER]

[NEGATIVE] Stock photo debe ser REALISTIC PHOTOGRAPHY — NO illustrated, NO 3D, NO cartoon, NO AI-generated faces obvias. NO toothy smile. NO exaggerated beauty industry stereotypes (NO over-makeup, NO salon background con sillas/lavabos). NO props en mano. NO branded clothing. Subtle confident expression, NO salesy. NO modificar el ad original arriba.
```

---

## Prompt #6 · D1-03 RETAIL (150 → 12) · Variante B — Stock model

```
[FORMAT] Advertisement poster, 1080x1920px vertical Meta Stories/Reels, 9:16.

[BASE — TOMAR AD ORIGINAL D1-03 EXACTAMENTE COMO ESTÁ]
- Background: solid navy #1A1A2E (todo el canvas)
- y=60: "AINNOVATION" wordmark Open Sauce One Bold 14pt white 80% centered
- y=170: eyebrow "TU NUEVO FUNNEL DE VENTAS" Open Sauce One Medium 22pt caps violet #8B5CF6 centered
- y=220: hairline white separator 120px
- y=270-350: Node 1 card rounded rect 2px violet stroke 880x80px "150 mensajes al dia" Clash Display 44pt white centered
- y=370: down arrow ↓ violet 40pt centered
- y=410-500: Node 2 card 880x90px "Tu vendedor AI contesta los 150 en 60 seg" Open Sauce One Bold 26pt white centered
- y=520: down arrow ↓ violet
- y=560-640: Node 3 card 880x80px "Califica cada uno automaticamente" Open Sauce One Bold 26pt white centered
- y=660: down arrow ↓ violet
- y=700-840: Node 4 card HIGHLIGHT 880x140px solid violet #8B5CF6 fill "Solo 12 llegan a ti:" Clash Display 42pt white + "los que quieren comprar" Open Sauce One Bold 28pt white
- y=880: hairline separator
- y=910-990: price "$1,999/mes. Tu solo cierras." Clash Display 56pt white centered
- y=1020-1090: CTA strip "MANDA DEMO" full-width violet band Clash Display 58pt caps white centered
- y=1120-1270: brand footer "AINNOVATION" + tagline pink pastel

[ADITION — Bottom decorative zone (y=1280-1920) — REEMPLAZAR "138" watermark con stock model]
- 1 stock photo: Latin Mexican man, age 32-50, dueño de retail / automotriz / mueblería / refaccionaria. Casual button-up shirt o polo (NO branded). Brazos cruzados o mano en mentón en pose "thinking confident". Slight confident smile (NO toothy, NO forced). Mirando a cámara con expresión "operador serio que toma decisiones".
- Photo cropped vertical: head-to-mid-torso shot, x=300-780, y=1340-1900
- Diversidad: NO el "ejecutivo cliché en traje". Tipo de cuerpo natural, edad rangeada 35-45, preferentemente con ligera barba o look de "dueño que está en la operación", NO oficina corporate
- Background del stock photo: blend con el navy #1A1A2E del ad — fondo neutro navy oscuro o grayscale dark que se mezcle con el brand color
- NO props (no celular, no autopartes, no productos en mano) — la persona se vende sola

[BACKGROUND] Solid navy #1A1A2E across full canvas. Bottom third con stock photo integrada al navy brand.

[TYPOGRAPHY] Mantener fonts del ad original.

[EXACT TEXT TO RENDER]
"AINNOVATION"
"TU NUEVO FUNNEL DE VENTAS"
"150 mensajes al dia"
"Tu vendedor AI contesta los 150 en 60 seg"
"Califica cada uno automaticamente"
"Solo 12 llegan a ti:"
"los que quieren comprar"
"$1,999/mes. Tu solo cierras."
"MANDA DEMO"
"AINNOVATION"
"ARTIFICIAL / INTELLIGENCE / FOR BUSINESS"

[STYLE] Flat vector engineering diagram (parte superior) + photographic stock confident operational man (parte inferior). Stock integrada visualmente al brand navy.

[RENDER ONLY TEXT FROM EXACT TEXT TO RENDER]

[NEGATIVE] Stock photo REALISTIC PHOTOGRAPHY. NO toothy smile. NO traje corporate. NO retail store background con productos. NO branded clothing. NO props en mano. Subtle confident, NO salesy. NO modificar el ad original arriba.
```

---

## Prompt #7 · D2-10 SISTEMA COMPLETO $4,999 · Variante B — Stock model

```
[FORMAT] Advertisement poster, 1080x1920px vertical Meta Stories/Reels, 9:16.

[BASE — TOMAR AD ORIGINAL D2-10 EXACTAMENTE COMO ESTÁ]
- Background: solid violet electric #8B5CF6 (todo el canvas)
- y=60: "AINNOVATION" wordmark Clash Display 38px letter-spacing 6px white top-centered
- y=120-150: eyebrow "NIVEL 2: EL SISTEMA COMPLETO" Open Sauce One Bold 24px pink pastel #F8C8DC letter-spacing 4px centered
- y=190-240: headline line 1 "CONTESTAR WHATSAPP" Clash Display 68px white centered
- y=245-295: headline line 2 "ES SOLO EL PRINCIPIO." Clash Display 68px white centered
- y=340-500: questions stack 4 lines Open Sauce One Bold 28px white centered, each ending with HUGE Clash Display 60px magenta #E040FB "?":
  "CUÁNTOS LEADS LLEGARON ESTA SEMANA?"
  "CUÁNTOS COMPRARON?"
  "CUÁNTOS SE FUERON?"
  "DE DONDE VINIERON?"
- y=530-580: punchline "SI NO SABES, NO TIENES SISTEMA." Clash Display 44px white centered
- y=610-680: price "$4,999/MES." Clash Display 96px magenta #E040FB centered
- y=720-1080: feature grid 2x3, 6 cells, monoline white icons + labels Open Sauce One Bold 26px white: TODOS LOS CANALES / PIPELINE / DASHBOARD / 3 FOLLOW-UPS / BROADCASTS / NO-SHOWS
- y=1110-1170: CTA pill "MANDA SISTEMA." magenta #E040FB rounded rect, white Open Sauce One Bold 34px
- y=1220: "AINNOVATION" wordmark Clash Display 32px white centered
- y=1252: tagline "ARTIFICIAL / INTELLIGENCE / FOR BUSINESS" Open Sauce One Regular 14px pink pastel centered

[ADITION — Bottom decorative zone (y=1280-1920) — REEMPLAZAR wavy pattern original con stock model]
- 1 stock photo: Latin Mexican PyME owner, age 38-55, semi-formal attire (button-up shirt sin corbata, o polo profesional). Brazos cruzados confident enterprise pose. Mirando a cámara con expresión "yo dirijo este negocio". Slight confident smile.
- Photo cropped vertical: head-to-mid-torso shot, x=300-780, y=1320-1900
- Diversidad: género balanceado (puede ser hombre 40-50 O mujer 38-48 — alternar entre ediciones). NO el ejecutivo cliché de traje completo. Look "dueño exitoso de PyME mediana" — vestido bien pero NO corporate de Fortune 500
- Background del stock photo: blend con el violet #8B5CF6 del ad — fondo neutro violet o studio dark que se mezcle con el brand color
- NO props (no celular, no laptop, no oficina) — autoridad humana se vende sola

[BACKGROUND] Solid violet electric #8B5CF6 across full canvas. Bottom third con stock photo integrada al violet brand.

[TYPOGRAPHY] Mantener fonts del ad original.

[EXACT TEXT TO RENDER]
"AINNOVATION"
"NIVEL 2: EL SISTEMA COMPLETO"
"CONTESTAR WHATSAPP"
"ES SOLO EL PRINCIPIO."
"CUÁNTOS LEADS LLEGARON ESTA SEMANA?"
"CUÁNTOS COMPRARON?"
"CUÁNTOS SE FUERON?"
"DE DONDE VINIERON?"
"SI NO SABES, NO TIENES SISTEMA."
"$4,999/MES."
"TODOS LOS CANALES"
"PIPELINE"
"DASHBOARD"
"3 FOLLOW-UPS"
"BROADCASTS"
"NO-SHOWS"
"MANDA SISTEMA."
"AINNOVATION"
"ARTIFICIAL / INTELLIGENCE / FOR BUSINESS"

[STYLE] Flat vector SaaS dashboard poster (parte superior) + photographic stock enterprise PyME owner (parte inferior). Authority + transparency. Stock integrada visualmente al brand violet.

[RENDER ONLY TEXT FROM EXACT TEXT TO RENDER]

[NEGATIVE] Stock photo REALISTIC PHOTOGRAPHY. NO ejecutivo cliché de traje completo con corbata. NO toothy smile. NO oficina corporate de fondo. NO branded clothing. NO laptop NI celular en mano. Subtle confident, NO salesy. NO modificar el ad original arriba.
```

---

# SECCIÓN 3 · SOLO TEXTO (Variante C — Control) · 0 prompts nuevos

> **No requiere prompts nuevos.**
>
> La variante C es el ad original tal cual — sin mascota, sin stock photo, con el wavy pattern decorativo original en la zona bottom (y=1280-1920).
>
> Estos archivos ya existen en sus carpetas:

| Cluster | Ad piloto | Path del control (ya existe) |
|---|---|---|
| General | D1-01 | `AD DOC1-01 — EL DATO (General)/` (archivo principal del ad) |
| Belleza | D1-02 | `AD DOC1-02 — BELLEZA (Una Semana)/` (archivo principal del ad) |
| Retail | D1-03 | `AD DOC1-03 — RETAIL ALTO VOLUMEN/` (archivo principal del ad) |
| Premium | D2-10 | `AD DOC2-10 — SISTEMA COMPLETO 4999/` (archivo principal del ad) |

Si en el futuro Henry decide hacer una variante C distinta (ej: "solo texto" sin wavy pattern, fondo limpio), entonces sí habría 4 prompts adicionales. Hoy NO los hay.

---

## Resumen de output esperado

7 prompts → 7 imágenes nuevas. Junto con D1-01 variante B que ya tienes, completas los 8 creativos del test (4 ads × 2 variantes A/B). Las versiones C ya existen como los originales.

| # | Variante | Cluster | Carpeta destino |
|---|---|---|---|
| 1 | A · Los AI | D1-01 | `AD DOC1-01 — EL DATO (General)/_test-mascota-variantA-losai/doc1-01-variantA-losai.png` |
| 2 | A · Los AI | D1-02 | `AD DOC1-02 — BELLEZA (Una Semana)/_test-mascota-variantA-losai/doc1-02-variantA-losai.png` |
| 3 | A · Los AI | D1-03 | `AD DOC1-03 — RETAIL ALTO VOLUMEN/_test-mascota-variantA-losai/doc1-03-variantA-losai.png` |
| 4 | A · Los AI | D2-10 | `AD DOC2-10 — SISTEMA COMPLETO 4999/_test-mascota-variantA-losai/doc2-10-variantA-losai.png` |
| 5 | B · Stock | D1-02 | `AD DOC1-02 — BELLEZA (Una Semana)/_test-mascota-variantB-stock/doc1-02-variantB-stock.png` |
| 6 | B · Stock | D1-03 | `AD DOC1-03 — RETAIL ALTO VOLUMEN/_test-mascota-variantB-stock/doc1-03-variantB-stock.png` |
| 7 | B · Stock | D2-10 | `AD DOC2-10 — SISTEMA COMPLETO 4999/_test-mascota-variantB-stock/doc2-10-variantB-stock.png` |
| — | B · Stock | D1-01 | (ya generada) |
| — | C · Control | x4 | (ya existen — son los ads originales) |

## Decision log

| Fecha | Decisión | Razón |
|---|---|---|
| 2026-04-25 (versión inicial) | Variante A con background negro #000, layout 50/50 desde cero | Primer borrador |
| 2026-04-26 (corrección 1) | Variante A con background MISMO brand del ad original | Henry: "los adds de las mascotas no seran negros son de el mismo color que los otros" |
| 2026-04-26 (corrección 2) | Variantes A y B son ADICIONES al ad original (overlay en bottom decorative zone), NO rediseños 50/50 | Henry: "los exact same ads only difference is the addition of the mascots and the stock photos" |
| 2026-04-26 (corrección 3) | Prompts B (stock) expandidos con bloque BASE completo (antes referenciaban "ver variante A" — incompletos si se pegaban solos) | Henry: "why are the stock model prompts so small" |
| 2026-04-26 (reorden) | Orden del doc: primero las 4 mascotas (A), luego las 3 stock (B), al final nota de variante C (no requiere prompts nuevos) | Henry: "ponlos en orden empecemos con las mascotas luego stock y de ultimo solo text si es que hay" |
