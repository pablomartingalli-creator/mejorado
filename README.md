<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <title>Método Persaltum – Presentación oficial</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta
    name="description"
    content="Presentación oficial del Método Persaltum: un sistema simple para crear y automatizar tu negocio digital paso a paso."
  />

  <style>
    :root {
      --bg-main: #050509;
      --bg-card: #111117;
      --accent-gold: #f5c45b;
      --accent-gold-soft: rgba(245, 196, 91, 0.2);
      --text-main: #f8f8ff;
      --text-muted: #b3b3c2;

      --gold: #f5c45b;
      --gold-hover: #d6a945;

      --hotmart: #ff5c00;
      --stripe: #635bff;

      --whatsapp: #25d366;

      --radius-xl: 18px;
      --shadow-soft: 0 18px 40px rgba(0, 0, 0, 0.45);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: radial-gradient(circle at top, #1a1a27 0%, #050509 60%);
      color: var(--text-main);
      line-height: 1.5;
      overflow-x: hidden;
      position: relative;
    }

    /* LOGO DE FONDO (LEÓN PERSALTUM) */
    body::before {
      content: "";
      position: fixed;
      top: -40px;
      left: 50%;
      transform: translateX(-50%);
      width: 620px;
      height: 620px;
      background: url("logo-persaltum.jpeg.jpeg") no-repeat center;
      background-size: contain;
      opacity: 0.18;
      filter: drop-shadow(0 0 16px rgba(0, 0, 0, 0.6));
      pointer-events: none;
      z-index: 0;
    }

    .page {
      max-width: 1120px;
      margin: 0 auto;
      padding: 24px 16px 64px;
      position: relative;
      z-index: 2;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    /* HEADER SOLO TEXTO */
    header {
      text-align: center;
      margin-bottom: 22px;
      margin-top: 4px;
    }

    .brand-title {
      font-size: 26px;
      color: var(--accent-gold);
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.06em;
    }

    .brand-sub {
      font-size: 13px;
      color: var(--text-muted);
      letter-spacing: 0.14em;
      text-transform: uppercase;
      margin-top: 4px;
    }

    .brand-method {
      font-size: 13px;
      color: var(--text-main);
      margin-top: 6px;
      opacity: 0.9;
    }

    /* HERO */
    .hero {
      display: grid;
      grid-template-columns: minmax(0, 1.15fr) minmax(0, 1fr);
      gap: 28px;
      align-items: center;
      margin-bottom: 32px;
    }

    .eyebrow {
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--accent-gold);
      margin-bottom: 8px;
    }

    .hero-title {
      font-size: 30px;
      line-height: 1.1;
      margin-bottom: 12px;
    }

    .hero-title .highlight {
      color: var(--accent-gold);
    }

    .hero-subtitle {
      font-size: 14px;
      color: var(--text-muted);
      max-width: 480px;
      margin-bottom: 16px;
    }

    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      font-size: 11px;
      padding: 6px 10px;
      border-radius: 999px;
      border: 1px solid var(--accent-gold-soft);
      background: rgba(5, 5, 12, 0.9);
      color: var(--text-muted);
      margin-bottom: 16px;
    }

    .dot {
      width: 6px;
      height: 6px;
      border-radius: 999px;
      background: var(--accent-gold);
    }

    .price-card {
      background: rgba(10, 10, 18, 0.9);
      border-radius: var(--radius-xl);
      padding: 14px;
      border: 1px solid rgba(245, 196, 91, 0.22);
      box-shadow: var(--shadow-soft);
      margin-bottom: 12px;
      font-size: 13px;
    }

    .price-row {
      display: flex;
      align-items: baseline;
      justify-content: space-between;
      gap: 10px;
      margin-bottom: 8px;
      flex-wrap: wrap;
    }

    .price-main {
      display: flex;
      align-items: baseline;
      gap: 8px;
      flex-wrap: wrap;
    }

    .price-main .currency {
      font-size: 16px;
      opacity: 0.85;
    }

    .price-main .amount {
      font-size: 26px;
      font-weight: 800;
    }

    .price-main .amount-old {
      font-size: 18px;
      font-weight: 700;
      opacity: 0.55;
      text-decoration: line-through;
    }

    .price-main .once {
      font-size: 13px;
      color: var(--text-muted);
    }

    .price-tagline {
      font-size: 11px;
      color: var(--accent-gold);
      text-transform: uppercase;
      letter-spacing: 0.12em;
    }

    .price-extra {
      font-size: 11px;
      color: var(--text-muted);
    }

    .hero-list {
      list-style: none;
      font-size: 13px;
      color: var(--text-muted);
      margin-bottom: 12px;
    }

    .hero-list li {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 6px;
    }

    .bullet {
      width: 14px;
      height: 14px;
      border-radius: 999px;
      border: 1px solid var(--accent-gold-soft);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 10px;
      color: var(--accent-gold);
      flex-shrink: 0;
    }

    .hero-ctas {
      display: flex;
      flex-direction: column;
      gap: 10px;
      margin-bottom: 10px;
    }

    .cta-row-label {
      font-size: 11px;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.16em;
      margin-bottom: 4px;
    }

    /* BOTONES */
    .payment-buttons {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 10px;
      margin-bottom: 6px;
    }

    .btn {
      border-radius: 999px;
      padding: 12px 14px;
      font-size: 14px;
      font-weight: 800;
      text-align: center;
      border: none;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      transition: 0.18s ease;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.35);
      white-space: normal;
    }

    .btn:hover {
      transform: translateY(-1px);
      box-shadow: 0 12px 22px rgba(0, 0, 0, 0.45);
      opacity: 0.98;
    }

    .btn:active {
      transform: translateY(0);
      box-shadow: none;
      opacity: 0.95;
    }

    .btn-hotmart {
      background: var(--hotmart);
      color: #ffffff;
    }

    .btn-stripe {
      background: var(--stripe);
      color: #ffffff;
    }

    .btn .sub {
      font-size: 10px;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      opacity: 0.95;
      font-weight: 700;
    }

    .hero-note {
      font-size: 11px;
      color: var(--text-muted);
      margin-top: 2px;
    }

    .hero-note strong {
      color: var(--accent-gold);
      font-weight: 600;
    }

    /* VIDEO HERO */
    .hero-video-card {
      background: rgba(8, 8, 15, 0.9);
      border-radius: var(--radius-xl);
      border: 1px solid rgba(245, 196, 91, 0.15);
      padding: 12px;
      box-shadow: var(--shadow-soft);
      position: relative;
      overflow: hidden;
    }

    .hero-video-tag {
      position: absolute;
      top: 10px;
      left: 12px;
      font-size: 10px;
      padding: 4px 8px;
      border-radius: 999px;
      background: rgba(0, 0, 0, 0.55);
      border: 1px solid rgba(245, 196, 91, 0.35);
      text-transform: uppercase;
      letter-spacing: 0.12em;
    }

    .video-wrapper {
      position: relative;
      padding-top: 56.25%;
      border-radius: 14px;
      overflow: hidden;
    }

    .video-wrapper iframe {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      border: 0;
    }

    .video-caption {
      font-size: 11px;
      color: var(--text-muted);
      margin-top: 8px;
    }

    .video-caption .highlight {
      color: var(--accent-gold);
    }

    /* SECTION CARD */
    section {
      margin-top: 30px;
    }

    .section-card {
      background: var(--bg-card);
      border-radius: var(--radius-xl);
      border: 1px solid rgba(255, 255, 255, 0.04);
      padding: 18px 16px;
      box-shadow: var(--shadow-soft);
    }

    .section-title {
      font-size: 18px;
      margin-bottom: 8px;
    }

    .section-subtitle {
      font-size: 13px;
      color: var(--text-muted);
      margin-bottom: 14px;
    }

    .grid-2 {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1fr);
      gap: 18px;
    }

    .check-list {
      list-style: none;
      font-size: 13px;
      color: var(--text-muted);
    }

    .check-list li {
      display: flex;
      align-items: flex-start;
      gap: 8px;
      margin-bottom: 6px;
    }

    .check {
      width: 16px;
      height: 16px;
      border-radius: 999px;
      border: 1px solid var(--accent-gold-soft);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 11px;
      color: var(--accent-gold);
      flex-shrink: 0;
    }

    .pill-list {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-top: 6px;
    }

    .pill {
      font-size: 11px;
      padding: 4px 8px;
      border-radius: 999px;
      border: 1px solid rgba(245, 196, 91, 0.25);
      background: rgba(245, 196, 91, 0.06);
      color: var(--text-muted);
    }

    .quote-block {
      font-size: 12px;
      color: var(--text-muted);
      border-left: 2px solid rgba(245, 196, 91, 0.4);
      padding-left: 10px;
      margin-top: 8px;
    }

    .quote-block strong {
      color: var(--accent-gold);
    }

    /* FAQ */
    .faq-list {
      display: grid;
      gap: 10px;
      font-size: 13px;
    }

    .faq-item {
      border-radius: 12px;
      border: 1px solid rgba(255, 255, 255, 0.05);
      padding: 10px 12px;
      background: rgba(8, 8, 15, 0.9);
    }

    .faq-q {
      font-weight: 600;
      margin-bottom: 4px;
    }

    .faq-a {
      color: var(--text-muted);
    }

    .btn-wa {
      background: var(--whatsapp);
      color: #ffffff;
      box-shadow: 0 0 10px rgba(37, 211, 102, 0.35);
    }

    .btn-wa:hover {
      background: #1eb457;
      box-shadow: 0 0 18px rgba(37, 211, 102, 0.45);
    }

    .wa-card {
      display: flex;
      flex-direction: column;
      gap: 10px;
      align-items: flex-start;
    }

    footer {
      margin-top: 28px;
      font-size: 11px;
      color: var(--text-muted);
      text-align: center;
      opacity: 0.75;
    }

    .brand {
      color: var(--accent-gold);
    }

    /* RESPONSIVE */
    @media (max-width: 880px) {
      .hero { grid-template-columns: 1fr; }
      .hero-video-card { order: -1; }
      body::before { width: 420px; height: 420px; top: -10px; opacity: 0.22; }
      .payment-buttons { grid-template-columns: 1fr; }
    }

    @media (max-width: 640px) {
      .hero-title { font-size: 24px; }
      .page { padding-inline: 14px; }
    }
  </style>
</head>

<body>
  <div class="page">

    <!-- HEADER -->
    <header>
      <div class="brand-title">PERSALTUM</div>
      <div class="brand-sub">Universidad Digital del Infoproducto</div>
      <div class="brand-method">Presentación del Método Persaltum</div>
    </header>

    <!-- HERO -->
    <main>
      <section class="hero">
        <!-- TEXTO HERO -->
        <div>
          <div class="eyebrow">Presentación oficial</div>

          <h1 class="hero-title">
            Te explico <span class="highlight">paso a paso</span> cómo crear y automatizar tu negocio digital.
          </h1>

          <p class="hero-subtitle">
            Un sistema simple para ordenar tus ideas, entender cómo funciona un negocio digital y dejar de vender a ciegas.
          </p>

          <div class="hero-badge">
            <span class="dot"></span>
            <span>PDF estratégico + video explicativo completo</span>
          </div>

          <div class="price-card">
            <div class="price-row">
              <div class="price-main">
                <span class="currency">USD</span>
                <span class="amount-old">37</span>
                <span class="amount">17</span>
                <span class="once">pago único · precio fundacional (30 días)</span>
              </div>
              <div class="price-tagline">Promoción limitada de lanzamiento</div>
            </div>
            <div class="price-extra">
              Acceso inmediato al PDF del Método Persaltum + clase explicativa donde ves el sistema completo aplicado a negocios reales.
            </div>
          </div>

          <ul class="hero-list">
            <li><span class="bullet">✓</span>Guía estratégica del Método Persaltum en PDF.</li>
            <li><span class="bullet">✓</span>Video explicativo donde te llevo paso a paso.</li>
            <li><span class="bullet">✓</span>Acceso inmediato después del pago.</li>
          </ul>

          <!-- BOTONES PAGO (2) -->
          <div class="hero-ctas">
            <div class="cta-row-label">Elegí tu forma de pago</div>

            <div class="payment-buttons">
              <a class="btn btn-hotmart" href="https://pay.hotmart.com/V101694536F?off=uyadaend" target="_blank" rel="noopener noreferrer">
                Comprar en Hotmart <span class="sub">recomendado</span>
              </a>

              <a class="btn btn-stripe" href="https://buy.stripe.com/8x228q3HL8H14qx1OKbwk0n" target="_blank" rel="noopener noreferrer">
                Pagar con tarjeta (Stripe)
              </a>
            </div>

            <div class="hero-note">
              <strong>Garantía:</strong> 7 días por Hotmart · <strong>Acceso:</strong> inmediato por email.
            </div>
          </div>

          <div class="hero-note">
            <strong>Importante:</strong> si pagás por Hotmart, antes de finalizar la compra vas a ver productos adicionales opcionales para acelerar tus resultados.
          </div>
        </div>

        <!-- VIDEO HERO -->
        <div class="hero-video-card">
          <div class="hero-video-tag">VSL + clase explicativa</div>

          <div class="video-wrapper">
            <iframe
              src="https://www.youtube.com/embed/SJCvhQZMuT4"
              title="Presentación del Método Persaltum"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
              allowfullscreen
            ></iframe>
          </div>

          <div class="video-caption">
            En este video, <span class="highlight">Pablo Galli</span> te muestra el sistema que vas a aplicar para dejar de improvisar y empezar a vender con método.
          </div>
        </div>
      </section>

      <!-- QUÉ INCLUYE -->
      <section>
        <div class="section-card">
          <h2 class="section-title">¿Qué incluye el Método Persaltum?</h2>
          <p class="section-subtitle">
            Es el resumen estratégico de años de experiencia, pruebas reales y miles de dólares invertidos en formación, condensado en un sistema simple.
          </p>

          <div class="grid-2">
            <div>
              <ul class="check-list">
                <li>
                  <div class="check">✓</div>
                  <div>
                    <strong>PDF estratégico del Método Persaltum</strong><br />
                    El mapa completo del sistema: captación, contenido, automatización y venta.
                  </div>
                </li>
                <li>
                  <div class="check">✓</div>
                  <div>
                    <strong>Video explicativo paso a paso</strong><br />
                    Entendés claramente cómo funciona el sistema y cómo aplicarlo en tu caso.
                  </div>
                </li>
                <li>
                  <div class="check">✓</div>
                  <div>
                    <strong>Ruta simple para automatizar</strong><br />
                    Qué herramientas usar, cómo conectarlas y qué evitar para no trabarte.
                  </div>
                </li>
                <li>
                  <div class="check">✓</div>
                  <div>
                    <strong>Enfoque sin tecnicismos</strong><br />
                    Todo explicado en lenguaje claro, aplicable aunque estés empezando desde cero.
                  </div>
                </li>
              </ul>
            </div>

            <div>
              <div class="quote-block">
                Después de años estudiando negocios digitales, probando sistemas, herramientas y estrategias, entendí una cosa:<br /><br />
                <strong>No necesitás más información suelta. Necesitás un método claro que te diga qué hacer y en qué orden, para configurar un sistema que trabaje 24/7.</strong>
              </div>

              <div class="pill-list">
                <div class="pill">Ideal si recién empezás</div>
                <div class="pill">Sirve si ya vendés y querés orden</div>
                <div class="pill">Aplicable a cursos y mentorías</div>
                <div class="pill">Pensado para Latinoamérica y el mundo</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- PARA QUIÉN ES / NO ES -->
      <section>
        <div class="section-card">
          <h2 class="section-title">¿Para quién es y para quién no es?</h2>
          <div class="grid-2">
            <div>
              <h3 class="section-subtitle" style="margin-bottom:8px;">Sí es para vos si...</h3>
              <ul class="check-list">
                <li><div class="check">✓</div><div>Querés dejar de adivinar cómo vender online y tener un mapa claro.</div></li>
                <li><div class="check">✓</div><div>Tenés una idea, un conocimiento o un servicio y no sabés cómo llevarlo a un sistema digital.</div></li>
                <li><div class="check">✓</div><div>Estás cansado de consumir contenido sin ver resultados y querés algo aplicable.</div></li>
              </ul>
            </div>
            <div>
              <h3 class="section-subtitle" style="margin-bottom:8px;">No es para vos si...</h3>
              <ul class="check-list">
                <li><div class="check">✕</div><div>Buscás una solución mágica sin hacer nada.</div></li>
                <li><div class="check">✕</div><div>No estás dispuesto a sentarte 1 o 2 horas a leer, ver la clase y tomar notas.</div></li>
                <li><div class="check">✕</div><div>Querés un negocio “suerte” y no un negocio con método.</div></li>
              </ul>
            </div>
          </div>
        </div>
      </section>

      <!-- RESULTADOS -->
      <section>
        <div class="section-card">
          <h2 class="section-title">¿Qué vas a lograr con este material?</h2>
          <p class="section-subtitle">
            El objetivo es que termines el PDF y la clase explicativa con claridad, foco y un plan simple para avanzar.
          </p>

          <ul class="check-list">
            <li><div class="check">✓</div><div>Entender cuál es el modelo de negocio digital que mejor encaja con vos.</div></li>
            <li><div class="check">✓</div><div>Ver cómo funciona un sistema que capta, educa y vende por vos.</div></li>
            <li><div class="check">✓</div><div>Dejar de improvisar contenido y empezar a comunicar con estrategia.</div></li>
            <li><div class="check">✓</div><div>Saber qué herramientas usar para automatizar sin complicarte.</div></li>
            <li><div class="check">✓</div><div>Tener un mapa claro para escalar después a mentorías, cursos o una universidad digital.</div></li>
          </ul>
        </div>
      </section>

      <!-- FAQ + WHATSAPP -->
      <section>
        <div class="grid-2">
          <div class="section-card">
            <h2 class="section-title">Preguntas frecuentes</h2>

            <div class="faq-list">
              <div class="faq-item">
                <div class="faq-q">¿Cuándo recibo el material?</div>
                <div class="faq-a">
                  El acceso es inmediato. Apenas se acredita el pago, recibís el PDF del Método Persaltum y el acceso al video explicativo en tu correo.
                </div>
              </div>
              <div class="faq-item">
                <div class="faq-q">¿Necesito experiencia previa en marketing o tecnología?</div>
                <div class="faq-a">
                  No. El material está pensado para que lo entienda alguien que recién empieza. Si ya tenés experiencia, te va a ayudar a ordenar y simplificar lo que venís haciendo.
                </div>
              </div>
              <div class="faq-item">
                <div class="faq-q">¿Qué pasa con los productos adicionales (upsells)?</div>
                <div class="faq-a">
                  Dentro del checkout de Hotmart vas a ver opciones extra para acelerar tus resultados. Son completamente opcionales: podés aceptarlos o no, y seguís teniendo el Método Persaltum igual.
                </div>
              </div>
              <div class="faq-item">
                <div class="faq-q">¿Es una suscripción?</div>
                <div class="faq-a">
                  No. Es un pago único por el acceso al PDF y al video explicativo de la presentación del Método Persaltum.
                </div>
              </div>
            </div>
          </div>

          <div class="section-card wa-card">
            <h2 class="section-title">Unite al grupo de novedades</h2>
            <p class="section-subtitle">
              Sumate al grupo de WhatsApp donde comparto novedades, lanzamientos y avisos importantes del Método Persaltum.
            </p>

            <a class="btn btn-wa" href="https://chat.whatsapp.com/Gg1xzEhj28vEJVSth0VLzG" target="_blank" rel="noopener noreferrer">
              <span>💬</span>
              <span>Unirme al grupo de WhatsApp de novedades</span>
            </a>
          </div>
        </div>
      </section>

      <!-- CTA FINAL -->
      <section>
        <div class="section-card">
          <h2 class="section-title">Si te dijera que no podés fracasar, ¿cuán grande sería tu sueño?</h2>
          <p class="section-subtitle">
            Este es el primer paso. El resto lo vamos a construir juntos.
          </p>

          <div class="hero-ctas">
            <div class="cta-row-label">Empezá ahora con el Método Persaltum</div>

            <div class="payment-buttons">
              <a class="btn btn-hotmart" href="https://pay.hotmart.com/V101694536F?off=uyadaend" target="_blank" rel="noopener noreferrer">
                Comprar en Hotmart <span class="sub">recomendado</span>
              </a>

              <a class="btn btn-stripe" href="https://buy.stripe.com/8x228q3HL8H14qx1OKbwk0n" target="_blank" rel="noopener noreferrer">
                Pagar con tarjeta (Stripe)
              </a>
            </div>

            <div class="hero-note">
              <strong>Garantía:</strong> 7 días por Hotmart · <strong>Acceso:</strong> inmediato por email.
            </div>
          </div>
        </div>
      </section>
    </main>

    <footer>
      <p><span class="brand">Persaltum</span> · Universidad Digital del Infoproducto · Todos los derechos reservados.</p>
    </footer>
  </div>
</body>
</html>
