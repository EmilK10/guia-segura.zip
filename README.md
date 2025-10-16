# guia-segura.zip
Sitio educativo y accesible sobre ciberseguridad para toda la comunidad: conceptos clave, delitos, datos personales, leyes, medidas prácticas, respuesta a incidentes, videos y campaña “Phishing: 3 señales + qué hacer”.
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Ciberseguridad: Tu Guía Segura en el Mundo Digital</title>
<meta name="description" content="Sitio educativo completo y accesible sobre ciberseguridad para todas las edades: conceptos esenciales, delitos, datos personales, leyes, consejos, configuraciones, respuesta a incidentes, videos oficiales, campaña #ProtegeTusDatos, contactos, FAQ, glosario y fuentes." />
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@700;800&family=Inter:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#f8fafc; --bg2:#ffffff; --text:#111827; --muted:#475569; --line:#e5e7eb;
    --brand:#0f766e; --brand2:#14b8a6; --ok:#16a34a; --warn:#d97706; --danger:#dc2626;
    --card:#ffffff; --r:16px; --shadow:0 8px 24px rgba(2,6,23,.08);
  }
  *{box-sizing:border-box}
  html{scroll-behavior:smooth}
  body{margin:0; color:var(--text); font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif; background:linear-gradient(180deg,var(--bg) 0%, var(--bg2) 100%)}
  a{color:var(--brand); text-decoration:none}
  a:focus-visible, button:focus-visible{outline:3px solid var(--brand2); outline-offset:2px}
  .skip{position:absolute;left:-9999px;top:auto;width:1px;height:1px;overflow:hidden}
  .skip:focus{left:12px;top:12px;width:auto;height:auto;background:#fff;color:#000;padding:8px 10px;border-radius:8px;z-index:2000}

  /* Header / Hero */
  header.hero{position:relative; overflow:hidden; padding:88px 20px 44px; text-align:center; border-bottom:1px solid var(--line); background:radial-gradient(1200px 600px at 50% -10%, rgba(20,184,166,.12), transparent 60%)}
  .title{font-family:Montserrat,system-ui; font-weight:800; font-size:clamp(28px,5vw,52px); margin:0 0 10px; background:linear-gradient(90deg,var(--text),#334155); -webkit-background-clip:text; background-clip:text; color:transparent}
  .lead{max-width:1100px; margin:0 auto; color:#334155; font-size:clamp(16px,2.2vw,19px)}
  .cta{margin-top:20px; display:flex; gap:10px; justify-content:center; flex-wrap:wrap}
  .btn{display:inline-block; padding:12px 16px; border-radius:12px; background:linear-gradient(135deg,var(--brand),var(--brand2)); color:#ffffff; font-weight:800; box-shadow:var(--shadow); transition:transform .25s ease, filter .25s ease}
  .btn:hover{transform:translateY(-2px); filter:saturate(1.05)}

  /* Nav */
  nav.sticky{position:sticky; top:0; z-index:1000; background:rgba(255,255,255,.92); backdrop-filter:blur(8px); border-bottom:1px solid var(--line)}
  .nav-inner{max-width:1200px; margin:0 auto; display:flex; align-items:center; justify-content:space-between; padding:10px 14px}
  .brand{font-weight:900; letter-spacing:.3px}
  .links{display:flex; flex-wrap:wrap; gap:6px}
  .links a{padding:8px 10px; border-radius:10px; color:#0f172a; opacity:.92}
  .links a:hover,.links a.active{background:#e2e8f0; opacity:1}

  /* Sections */
  main section{max-width:1100px; margin:0 auto; padding:32px 16px}
  h2{font-family:Montserrat,system-ui; font-size:clamp(22px,3.3vw,30px); margin:2px 0 12px; color:#0f172a}
  p,li{line-height:1.7}
  .muted{color:var(--muted)}
  .grid{display:grid; gap:16px}
  @media(min-width:900px){
    .grid.cols-2{grid-template-columns:1fr 1fr}
    .grid.cols-3{grid-template-columns:repeat(3,1fr)}
    .grid.cols-4{grid-template-columns:repeat(4,1fr)}
  }
  .card{background:var(--card); border:1px solid var(--line); border-radius:var(--r); padding:18px; box-shadow:var(--shadow)}

  /* Table */
  .table-wrap{overflow:auto; border:1px solid var(--line); border-radius:12px; background:#fff}
  table{width:100%; border-collapse:collapse; min-width:820px}
  th,td{padding:12px 10px; border-bottom:1px solid var(--line); text-align:left}
  th{position:sticky; top:0; background:#f1f5f9}
  tr:hover td{background:#f8fafc}

  /* Videos */
  .video-grid{display:grid; gap:16px}
  @media(min-width:900px){.video-grid{grid-template-columns:1fr 1fr}}
  .video{position:relative; aspect-ratio:16/9; border-radius:12px; overflow:hidden; border:1px solid var(--line); box-shadow:var(--shadow); background:#000}
  .video iframe, .video video{position:absolute; inset:0; width:100%; height:100%}

  /* Reveal on scroll */
  .reveal{opacity:0; transform:translateY(10px); transition:opacity .6s ease, transform .6s ease}
  .reveal.visible{opacity:1; transform:none}

  /* Small tags */
  .tag{display:inline-block; font-size:.85rem; font-weight:700; padding:6px 10px; border-radius:999px; background:#f1f5f9; border:1px solid var(--line); margin:2px 6px 8px 0}

  /* Back to top */
  .top{position:fixed; right:12px; bottom:12px; padding:10px 12px; border-radius:999px; background:linear-gradient(135deg,var(--brand),var(--brand2)); color:#ffffff; font-weight:900; box-shadow:var(--shadow); opacity:0; transform:translateY(8px); transition:.25s}
  .top.show{opacity:1; transform:none}

  /* Campaign */
  .banner{border-radius:16px; padding:18px; border:1px solid var(--line); background:linear-gradient(140deg, rgba(15,118,110,.08), rgba(20,184,166,.10)); box-shadow:var(--shadow)}
  .pillars{display:grid; gap:14px}
  @media(min-width:900px){.pillars{grid-template-columns:repeat(3,1fr)}}

  footer{border-top:1px solid var(--line); padding:24px 16px; color:#475569; text-align:center; background:#ffffff}

  /* Print */
  @media print{
    nav, .top, .video{display:none!important}
    body{background:#fff; color:#000}
    .card, .banner{background:#fff; color:#000; border:1px solid #000}
    a{color:#000}
  }
.link-card{display:block;color:inherit}
  .link-card:hover{box-shadow:0 10px 28px rgba(2,6,23,.12); transform:translateY(-1px)}
  a.card{display:block}
</style>
</head>
<body>
<a href="#main" class="skip">Saltar al contenido</a>

<header class="hero" id="inicio" role="banner">
  <h1 class="title">Ciberseguridad: Tu Guía Segura en el Mundo Digital</h1>
  <p class="lead">Un sitio claro, completo y accesible para toda la comunidad. Aquí encontrarás conceptos esenciales, tipos de delitos, datos personales a proteger, leyes y derechos, medidas prácticas, configuraciones clave, qué hacer ante un incidente, videos de referencia, una campaña accionable <strong>#ProtegeTusDatos</strong>, contactos de apoyo, preguntas frecuentes, glosario y fuentes oficiales.</p>
  <div class="cta" aria-label="Acciones principales">
    <a class="btn" href="#conceptos">Conceptos esenciales</a>
    <a class="btn" href="#videos">Ver videos</a>
  </div>
</header>

<nav class="sticky" aria-label="Navegación principal">
  <div class="nav-inner">
    <strong class="brand">Guía Segura</strong>
    <div class="links" id="navlinks">
      <a href="#inicio">Inicio</a>
      <a href="#conceptos">Conceptos</a>
      <a href="#delitos">Delitos</a>
      <a href="#datos">Datos personales</a>
      <a href="#leyes">Leyes</a>
      <a href="#consejos">Consejos</a>
      <a href="#config">Configuraciones</a>
      <a href="#incidentes">Incidentes</a>
      <a href="#videos">Videos</a>
      <a href="#campana">Campaña</a>
      <a href="#contactos">Contactos</a>
      <a href="#faq">FAQ</a>
      <a href="#glosario">Glosario</a>
      <a href="#fuentes">Fuentes</a>
    </div>
  </div>
</nav>

<main id="main">
  <!-- INICIO / PROPÓSITO -->
  <section class="reveal" aria-labelledby="sec-inicio">
    <h2 id="sec-inicio">Inicio</h2>
    <div class="card">
      <p>Este sitio resume, en un solo lugar, lo imprescindible para cuidarte en Internet. Su propósito es ayudarte a comprender la ciberseguridad sin tecnicismos innecesarios, aplicar medidas sencillas que marcan gran diferencia y saber responder ante riesgos. La navegación es simple: usa el menú superior para saltar a la sección que necesites y el botón “Volver arriba” para regresar al inicio. Todo el contenido está redactado en español claro y pensado para estudiantes, familias y personal escolar, con prácticas que funcionan en computadoras y dispositivos móviles.</p>
    </div>
  </section>

  <!-- CONCEPTOS ESENCIALES -->
  <section id="conceptos" class="reveal" aria-labelledby="sec-conceptos">
    <h2 id="sec-conceptos">Conceptos esenciales</h2>
    <div class="card">
      <p>La ciberseguridad es el conjunto de prácticas y tecnologías que protegen sistemas, redes y datos frente a accesos no autorizados, daños o interrupciones. Se apoya en el triángulo <em>CIA</em>: confidencialidad (solo las personas autorizadas pueden ver la información), integridad (la información no se altera sin permiso) y disponibilidad (la información y los servicios están accesibles cuando se necesitan). A este marco se suma la autenticación, que verifica la identidad de quien intenta acceder, y la autorización, que determina lo que cada identidad puede hacer dentro de un sistema.</p>
      <p>Para el día a día, conviene recordar cuatro ideas: usar contraseñas únicas y largas, activar la autenticación de dos factores (2FA) con aplicación de códigos, mantener sistemas y apps actualizados y ser prudente con lo que compartimos en línea. Estas medidas reducen la mayoría de los riesgos habituales, desde intentos de suplantación hasta malware, y fortalecen el control sobre nuestros propios datos personales y educativos.</p>
      <ul>
        <li><span class="tag">Confidencialidad</span> Limita quién puede ver datos sensibles.</li>
        <li><span class="tag">Integridad</span> Evita cambios no autorizados en archivos y registros.</li>
        <li><span class="tag">Disponibilidad</span> Mantiene servicios y copias accesibles cuando se requieren.</li>
        <li><span class="tag">Autenticación</span> Confirma identidades; mejor con 2FA basada en app.</li>
        <li><span class="tag">Autorización</span> Define permisos por rol o necesidad de saber.</li>
        <li><span class="tag">Principio de mínimo privilegio</span> Menos permisos, menor impacto ante errores.</li>
        <li><span class="tag">Seguridad en capas</span> Contraseñas + 2FA + copias + actualizaciones.</li>
        <li><span class="tag">Huella digital</span> Todo lo que publicas puede ser copiado y persistir.</li>
      </ul>
    </div>
  </section>

  <!-- DELITOS: TABLA GRANDE -->
  <section id="delitos" class="reveal" aria-labelledby="sec-delitos">
    <h2 id="sec-delitos">Delitos cibernéticos</h2>
    <div class="table-wrap" role="region" aria-label="Tabla de delitos cibernéticos con ejemplos y prevención">
      <table>
        <thead>
          <tr>
            <th>Delito</th>
            <th>En qué consiste</th>
            <th>Ejemplo cotidiano</th>
            <th>Cómo prevenir</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Phishing</td>
            <td>Mensajes que suplantan a instituciones o contactos para que reveles contraseñas, códigos 2FA o datos.</td>
            <td>Correo de “banco” con enlace a página falsa para “verificar tu cuenta”.</td>
            <td>Verificar remitente y dominio; no usar enlaces del mensaje; entrar tú al sitio oficial; activar 2FA.</td>
          </tr>
          <tr>
            <td>Malware</td>
            <td>Software malicioso que espía, daña o roba información sin tu permiso.</td>
            <td>Instalar una “app gratis” que añade barras y pop‑ups e instala troyanos.</td>
            <td>Descargar solo de tiendas oficiales; antivirus actualizado; no ejecutar adjuntos desconocidos.</td>
          </tr>
          <tr>
            <td>Ransomware</td>
            <td>Malware que cifra tus archivos y exige pago para liberarlos.</td>
            <td>Documento adjunto en correo que, al abrirse, cifra fotos y tareas.</td>
            <td>Copias 3‑2‑1; no abrir adjuntos sospechosos; parches al día; mínimo privilegio.</td>
          </tr>
          <tr>
            <td>Suplantación de identidad</td>
            <td>Alguien se hace pasar por ti o por otra persona para obtener beneficios o acceso.</td>
            <td>Cuenta de red social clonada que pide dinero a tus contactos.</td>
            <td>Perfiles privados; verificación de doble paso; reportar cuentas falsas; educación digital familiar.</td>
          </tr>
          <tr>
            <td>Fraude en compras en línea</td>
            <td>Venta de productos inexistentes o cobros indebidos mediante sitios falsos o anuncios engañosos.</td>
            <td>Tienda con ofertas “demasiado buenas” que nunca entrega ni devuelve.</td>
            <td>Comprar solo en comercios conocidos; revisar políticas claras; usar medios de pago seguros.</td>
          </tr>
          <tr>
            <td>Ciberacoso</td>
            <td>Acoso, amenazas o humillación mediante medios digitales.</td>
            <td>Mensajes ofensivos o difusión de contenido íntimo sin consentimiento.</td>
            <td>Guardar evidencias; bloquear y denunciar; pedir apoyo a docentes y tutores; rutas de atención.</td>
          </tr>
          <tr>
            <td>Robo de identidad</td>
            <td>Uso indebido de tus datos personales para abrir cuentas o realizar operaciones.</td>
            <td>Créditos a tu nombre sin autorización tras una filtración de datos.</td>
            <td>Monitorear movimientos; alertas bancarias; minimizar datos públicos; 2FA y contraseñas únicas.</td>
          </tr>
          <tr>
            <td>Ingeniería social</td>
            <td>Manipulación psicológica para que reveles información o realices acciones inseguras.</td>
            <td>Llamada de “soporte” que pide tu código de verificación “para ayudarte”.</td>
            <td>Verificar por un canal alterno; nunca compartir contraseñas ni códigos 2FA; política de verificación.</td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>

  <!-- DATOS PERSONALES -->
  <section id="datos" class="reveal" aria-labelledby="sec-datos">
    <h2 id="sec-datos">Datos personales que debemos proteger</h2>
    <div class="card">
      <p>Proteger los datos personales evita suplantaciones, fraudes y afectaciones a tu integridad. Los datos físicos incluyen información que te identifica en documentos y contextos presenciales; los digitales abarcan credenciales, metadatos y rastros de actividad. La exposición excesiva en redes sociales, formularios o dispositivos compartidos facilita que terceros perfilen hábitos y vulnerabilidades. Minimizar la recolección y compartir solo lo necesario es una regla básica que reduce el riesgo sin complicar tu vida diaria.</p>
      <p>En Internet, muchos servicios solicitan información que no siempre es imprescindible para brindarte el producto. Pregunta: ¿es obligatorio? ¿Puedo limitarlo o usar alias? Activa controles de privacidad, deshabilita permisos innecesarios y utiliza autenticación robusta. Mantener copias de respaldo, monitorear avisos de inicio de sesión y revisar dispositivos conectados te ayuda a detectar y responder a tiempo si alguien intenta acceder indebidamente a tus cuentas o archivos.</p>
      <div class="grid cols-2">
        <div>
          <h3>Datos físicos</h3>
          <ul>
            <li>Identificación oficial, CURP, actas y credenciales escolares.</li>
            <li>Domicilio, números de teléfono familiares y rutas cotidianas.</li>
            <li>Información médica básica y datos de contacto de emergencia.</li>
            <li>Comprobantes de domicilio y estados de cuenta impresos.</li>
          </ul>
        </div>
        <div>
          <h3>Datos digitales</h3>
          <ul>
            <li>Contraseñas, respuestas de recuperación y <abbr title="Autenticación de dos factores">2FA</abbr> (códigos y claves).</li>
            <li>Ubicación, historial de navegación y metadatos de fotos/documentos.</li>
            <li>Tokens de sesión, cookies, direcciones de correo y alias.</li>
            <li>Archivos en la nube, respaldos y chats con información sensible.</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- LEYES Y DERECHOS -->
  <section id="leyes" class="reveal" aria-labelledby="sec-leyes">
    <h2 id="sec-leyes">Leyes y derechos del ciudadano digital</h2>
    <div class="card">
      <p>En México, la protección de datos personales está respaldada por leyes como la LGPDPPSO (sector público) y la legislación aplicable al sector privado; además, el Código Penal Federal contempla conductas relacionadas con fraudes y acceso indebido. A nivel internacional, el Convenio de Budapest promueve la cooperación contra la ciberdelincuencia. Conocer estas bases te ayuda a ejercer tus derechos y a identificar rutas de denuncia.</p>
      <p>Como titular de datos cuentas con derechos ARCO: <strong>Acceso</strong> a tus datos, <strong>Rectificación</strong> cuando sean inexactos, <strong>Cancelación</strong> cuando ya no sean necesarios y <strong>Oposición</strong> a ciertos tratamientos. Las instituciones deben implementar medidas de seguridad, avisos de privacidad claros y mecanismos para atender solicitudes en plazos definidos.</p>
      <ul>
        <li>Exige <strong>aviso de privacidad</strong> claro y accesible; solicita copia cuando compartas datos.</li>
        <li>Presenta <strong>solicitudes ARCO</strong> ante el responsable para ejercer tus derechos.</li>
        <li>Si detectas mal uso de datos, conserva evidencias y acude a autoridades competentes.</li>
        <li>Antes de aceptar términos, revisa permisos innecesarios y opciones de rechazo.</li>
      </ul>
      <p class="muted">Aviso: esta sección es informativa y no sustituye asesoría legal.</p>
    </div>
  </section>

  <!-- CONSEJOS Y MEDIDAS -->
  <section id="consejos" class="reveal" aria-labelledby="sec-consejos">
    <h2 id="sec-consejos">Consejos y medidas de protección</h2>
    <div class="card">
      <ul>
        <li>Usa frases de contraseña de 12+ caracteres, únicas por servicio; apóyate en un gestor de contraseñas.</li>
        <li>Activa la autenticación de dos factores con una aplicación de códigos (mejor que SMS cuando sea posible).</li>
        <li>Actualiza sistema operativo, navegador y aplicaciones; activa actualizaciones automáticas.</li>
        <li>Aplica la regla 3‑2‑1 de copias: tres copias, dos medios distintos y una fuera de línea o en la nube.</li>
        <li>Evita redes Wi‑Fi públicas para pagos o datos sensibles; usa tu red móvil o una VPN confiable.</li>
        <li>Antes de hacer clic, pasa el cursor por el enlace (o mantén presionado en móvil) y verifica la URL real.</li>
        <li>No compartas códigos de verificación ni contraseñas por correo, chat o llamada.</li>
        <li>Revisa permisos de apps y elimina las que no uses; menos permisos, menos riesgo.</li>
        <li>Configura alertas de inicio de sesión, revisa dispositivos conectados y cierra sesiones antiguas.</li>
        <li>Privacidad en redes: limita datos sensibles, usa perfiles privados y listas de audiencia.</li>
        <li>Activa “Encontrar mi dispositivo” y bloqueo por PIN/biometría en el teléfono.</li>
        <li>Educa a tu familia y equipo con ejemplos reales una vez al mes; compartir refuerza hábitos.</li>
        <li>Para compras en línea, prefiere comercios conocidos, políticas claras y métodos de pago seguros.</li>
        <li>Desconfía de adjuntos inesperados (.zip/.exe) y mensajes con urgencia exagerada.</li>
      </ul>
    </div>
  </section>

  <!-- CONFIGURACIONES ESENCIALES -->
  <section id="config" class="reveal" aria-labelledby="sec-config">
    <h2 id="sec-config">Configuraciones esenciales</h2>
    <div class="card">
      <ol>
        <li><strong>Activar 2FA</strong> en correo, banca y redes con aplicación de códigos; guarda códigos de respaldo en lugar seguro.</li>
        <li><strong>Revisar permisos</strong> de aplicaciones: cámara, micrófono, ubicación y contactos solo cuando sea necesario.</li>
        <li><strong>Cifrado del dispositivo</strong> y pantalla bloqueada con PIN/biometría; activa borrado remoto.</li>
        <li><strong>Encontrar mi dispositivo</strong> en iOS/Android y paneles web; verifica que funcione.</li>
        <li><strong>Redes y router</strong>: cambia la contraseña por defecto, desactiva WPS y actualiza el firmware.</li>
        <li><strong>Actualizaciones automáticas</strong> del sistema y apps; programa reinicios semanales.</li>
        <li><strong>Cerrar sesiones antiguas</strong> y retirar dispositivos que no reconozcas.</li>
        <li><strong>Filtros de contenido</strong> y control parental cuando aplique; restringe descargas desconocidas.</li>
        <li><strong>Marcadores verificados</strong> para banca/servicios críticos; evita buscadores para iniciar sesión.</li>
        <li><strong>Respaldo periódico</strong> con verificación de restauración para datos críticos.</li>
      </ol>
    </div>
  </section>

  <!-- INCIDENTES -->
  <section id="incidentes" class="reveal" aria-labelledby="sec-incidentes">
    <h2 id="sec-incidentes">¿Qué hacer ante un incidente?</h2>
    <div class="grid cols-2">
      <div class="card">
        <ol>
          <li><strong>Detén</strong> la actividad: desconecta Wi‑Fi/datos o apaga el equipo si hay cifrado en curso.</li>
          <li><strong>Cambia contraseñas</strong> empezando por correo principal y cuentas críticas.</li>
          <li><strong>Cierra sesiones</strong> abiertas y retira dispositivos no reconocidos.</li>
          <li><strong>Renueva 2FA</strong> (regenera claves y códigos de respaldo).</li>
          <li><strong>Escaneo antimalware</strong> con herramientas actualizadas y revisión por un técnico si es necesario.</li>
          <li><strong>Respalda</strong> datos sanos y considera restaurar desde copias previas al incidente.</li>
          <li><strong>Reúne evidencias</strong>: capturas, correos, IDs de mensajes, hora/fecha y URL involucradas.</li>
          <li><strong>Denuncia y reporta</strong> por canales oficiales; avisa a tu institución y contactos afectados.</li>
        </ol>
      </div>
      <div class="card">
        <h3>Señales de impacto</h3>
        <ul>
          <li>Cargos no reconocidos o solicitudes de dinero desde tus cuentas.</li>
          <li>Alertas de inicio de sesión desde ubicaciones inusuales.</li>
          <li>Archivos cifrados, extensiones extrañas o accesos bloqueados.</li>
          <li>Mensajes enviados “por ti” que no recuerdas haber escrito.</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- VIDEOS (SOLO VIDEOS) -->
  <section id="videos" class="reveal" aria-labelledby="sec-videos">
    <h2 id="sec-videos">Videos</h2>
    <div class="grid cols-2">
      <a class="card link-card" href="https://youtu.be/ZjxUtcwX43g" target="_blank" rel="noopener">
        <h3>Hábitos digitales (INTERPOL) — abrir en YouTube</h3>
        <p class="muted">Haz clic en toda esta tarjeta para abrir el video en una pestaña nueva.</p>
        <p class="muted">Enlace directo: https://youtu.be/ZjxUtcwX43g</p>
      </a>
      <a class="card link-card" href="https://youtu.be/DyFEQv_KAQc" target="_blank" rel="noopener">
        <h3>Protección de datos personales (INAI) — abrir en YouTube</h3>
        <p class="muted">Haz clic en toda esta tarjeta para abrir el video en una pestaña nueva.</p>
        <p class="muted">Enlace directo: https://youtu.be/DyFEQv_KAQc</p>
      </a>
    </div>
  </section>

  <section id="campana" class="reveal" aria-labelledby="sec-campana">
    <h2 id="sec-campana">Campaña: Phishing — 3 señales + qué hacer</h2>

    <div class="card">
      <h3>Resumen</h3>
      <p><strong>Objetivo:</strong> que cualquier persona identifique mensajes de phishing en segundos y sepa actuar sin riesgo. <strong>Alcance:</strong> correo, SMS/chats, llamadas y códigos QR. <strong>Resultado esperado:</strong> menos clics peligrosos, 2FA activada y reportes oportunos.</p>
    </div>

    <div class="grid cols-2">
      <div class="card">
        <h3>Las 3 señales (qué son, ejemplo y cómo comprobar)</h3>
        <ol>
          <li><strong>Remitente/dominio raro</strong>
            <ul>
              <li><em>Qué es:</em> direcciones o dominios que no coinciden exactamente con los oficiales.</li>
              <li><em>Ejemplos:</em> <code>ban-co.com</code> por <code>banco.com</code>; nombre con letras extra (<code>soporte-bank</code>).</li>
              <li><em>Cómo comprobar sin riesgo:</em> mira la dirección completa; busca la web oficial tú mismo escribiendo la URL; compara dominios letra por letra.</li>
            </ul>
          </li>
          <li><strong>Urgencia/amenaza</strong>
            <ul>
              <li><em>Qué es:</em> presión para “actuar ya” (cierre de cuenta, multas, premios fugaces).</li>
              <li><em>Ejemplos:</em> “Último aviso en 1 hora”, “bloquearemos tu acceso”.</li>
              <li><em>Cómo comprobar:</em> respira 10 s; entra a la app/sitio oficial o llama al número real del organismo (no al del mensaje).</li>
            </ul>
          </li>
          <li><strong>Enlace/adjunto sospechoso</strong>
            <ul>
              <li><em>Qué es:</em> URLs que no llevan al dominio oficial o archivos inesperados (.zip/.exe).</li>
              <li><em>Ejemplos:</em> botón “Verificar” que abre una página con dominio distinto; “comprobante.zip”.</li>
              <li><em>Cómo comprobar:</em> revisa la URL real antes de abrir; en móvil, mantén presionado para previsualizar; jamás compartas <strong>códigos 2FA</strong>.</li>
            </ul>
          </li>
        </ol>
      </div>
      <div class="card">
        <h3>Qué hacer (protocolo sencillo)</h3>
        <ol>
          <li>No abras enlaces ni adjuntos; no respondas.</li>
          <li>Abre tú la <strong>app</strong> o escribe la <strong>URL oficial</strong> en el navegador.</li>
          <li>Reporta como phishing en tu correo/red y avisa a soporte si aplica.</li>
          <li>Cambia la contraseña afectada y activa/renueva <strong>2FA</strong>.</li>
        </ol>
        <h4>Si ya hiciste clic</h4>
        <ul>
          <li>Cierra sesión desde otro dispositivo, cambia contraseña y renueva 2FA.</li>
          <li>Escanea con antimalware y revisa movimientos o mensajes enviados “por ti”.</li>
        </ul>
        <h4>Si compartiste datos</h4>
        <ul>
          <li>Bloquea o congela cuenta si es financiero; monitorea alertas.</li>
          <li>Notifica a tus contactos para que ignoren mensajes sospechosos.</li>
        </ul>
      </div>
    </div>

    <div class="grid cols-2">
      <div class="card">
        <h3>Guía por canal</h3>
        <ul>
          <li><strong>Correo:</strong> revisa remitente completo; desconfía de “verifica aquí”. Usa marcadores para entrar a banca/escuela.</li>
          <li><strong>SMS/Chats:</strong> no sigas links acortados; verifica con la app oficial o por llamada al número legítimo.</li>
          <li><strong>Llamadas (vishing):</strong> cuelga y devuelve la llamada al número del sitio oficial; nadie serio pide contraseñas o códigos.</li>
          <li><strong>Códigos QR:</strong> no escanees carteles dudosos; si lo haces, revisa la URL antes de abrir.</li>
          <li><strong>Redes sociales:</strong> confirma por un canal alterno antes de enviar paga/datos.</li>
        </ul>
      </div>
      <div class="card">
        <h3>Lista de verificación en 60 segundos</h3>
        <ul>
          <li>1) Remitente/dominio exacto</li>
          <li>2) ¿Hay urgencia/amenaza?</li>
          <li>3) Enlace/adjunto sospechoso</li>
          <li>4) Verifica por app/sitio oficial</li>
          <li>5) Reporta, cambia clave y activa 2FA</li>
        </ul>
      </div>
    </div>

    <div class="grid cols-3">
      <div class="card">
        <h3>Actividad rápida (clase o familia)</h3>
        <p>Muestra un correo ficticio. Pide: “señala 3 pistas de phishing” y “qué harías”. Repite el protocolo de 4 pasos.</p>
      </div>
      <div class="card">
        <h3>Plantillas útiles</h3>
        <ul>
          <li><em>Reportar:</em> “Mensaje sospechoso de suplantación. No he hecho clic. ¿Pueden confirmar por canal oficial?”</li>
          <li><em>Avisar a contactos:</em> “Si recibes mensajes pidiendo dinero/códigos de ‘mi parte’, ignóralos. Te confirmo por llamada.”</li>
          <li><em>Soporte técnico:</em> “Posible phishing con dominio no oficial. Solicito verificación y bloqueo.”</li>
        </ul>
      </div>
      <div class="card">
        <h3>Mitos y realidades</h3>
        <ul>
          <li><strong>Mito:</strong> “Si tiene candado, es seguro”. <strong>Realidad:</strong> el candado no valida la identidad del sitio.</li>
          <li><strong>Mito:</strong> “Solo le pasa a quien no sabe”. <strong>Realidad:</strong> todos podemos caer si hay prisa o distracción.</li>
          <li><strong>Mito:</strong> “Los bancos piden contraseñas por correo”. <strong>Realidad:</strong> nunca deben pedir contraseñas ni códigos 2FA.</li>
        </ul>
      </div>
    </div>

    <a class="card link-card" href="https://www.youtube.com/watch?v=Pd_0EbJU2cg" target="_blank" rel="noopener" id="camp-video-link">
      <h3>Video de la campaña — abrir en YouTube</h3>
      <p class="muted">Reemplaza este enlace por tu URL de YouTube cuando la tengas.</p>
      <p class="muted">Enlace actual: https://www.youtube.com/watch?v=Pd_0EbJU2cg</p>
    </a>

    <div class="card">
      <p class="muted">Fuentes base para esta campaña (ver <strong>Fuentes y créditos</strong>): INTERPOL, INAI, SSPC/Gob.mx y LGPDPPSO. El contenido se simplifica para uso educativo.</p>
    </div>
  </section>

  <!-- CONTACTOS -->
  <section id="contactos" class="reveal" aria-labelledby="sec-contactos">
    <h2 id="sec-contactos">Contactos de apoyo</h2>
    <div class="card">
      <ul>
        <li><strong>Policía Cibernética CDMX (SSC):</strong> 55 5242 5100 ext. 5086 · policia.cibernetica@ssc.cdmx.gob.mx</li>
        <li><strong>Línea 088 (24/7):</strong> atención a delitos y emergencias federales.</li>
        <li><strong>Tel‑INAI:</strong> 800 835 4324 — asesoría sobre datos personales.</li>
      </ul>
      <p class="muted">Verifica los canales oficiales según tu región.</p>
    </div>
  </section>

  <!-- FAQ -->
  <section id="faq" class="reveal" aria-labelledby="sec-faq">
    <h2 id="sec-faq">Preguntas frecuentes (FAQ)</h2>
    <div class="card">
      <details><summary>Revelé mi contraseña, ¿qué hago?</summary><p>Cambia la contraseña de inmediato, cierra sesiones abiertas, habilita o renueva 2FA y revisa movimientos. Si usaste esa clave en otros sitios, cámbialas todas. Considera escaneo antimalware.</p></details>
      <details><summary>¿Cómo sé si una web es oficial?</summary><p>Escribe tú la dirección o usa marcadores verificados. Revisa el dominio exacto, el candado (https) y evita enlaces de mensajes sospechosos.</p></details>
      <details><summary>¿Qué es 2FA?</summary><p>Un segundo paso que añade un código temporal generado en una app o llave física. Aun con contraseña robada, tu cuenta queda protegida.</p></details>
      <details><summary>¿Cuándo cambiar contraseñas?</summary><p>Cuando haya indicios de filtración, si la compartiste o si la reutilizaste. Prioriza correo, banca y redes principales.</p></details>
      <details><summary>¿Sirve un antivirus en el móvil?</summary><p>Puede ayudar, pero lo esencial es instalar apps de fuentes oficiales, revisar permisos y mantener el sistema actualizado.</p></details>
      <details><summary>¿Cómo proteger a niñas y niños?</summary><p>Perfiles privados, control parental ajustado a la edad, diálogo sobre privacidad y reglas simples: no compartir datos sensibles ni códigos.</p></details>
    </div>
  </section>

  <!-- GLOSARIO -->
  <section id="glosario" class="reveal" aria-labelledby="sec-glosario">
    <h2 id="sec-glosario">Glosario</h2>
    <div class="card">
      <ul>
        <li><strong>Autenticación:</strong> verificar la identidad de una persona o dispositivo.</li>
        <li><strong>Autorización:</strong> permisos que determinan qué acciones están permitidas.</li>
        <li><strong>Cifrado:</strong> proceso para proteger datos haciéndolos ilegibles sin clave.</li>
        <li><strong>Token:</strong> dato que demuestra identidad o sesión activa.</li>
        <li><strong>Malware:</strong> software malicioso que daña o espía.</li>
        <li><strong>Ransomware:</strong> malware que cifra archivos para exigir pago.</li>
        <li><strong>Phishing:</strong> engaño para robar datos a través de suplantación.</li>
        <li><strong>Ingeniería social:</strong> manipulación psicológica para obtener información o acceso.</li>
        <li><strong>Metadatos:</strong> datos sobre datos (por ejemplo, fecha y ubicación de una foto).</li>
        <li><strong>VPN:</strong> red privada virtual que cifra tu conexión.</li>
        <li><strong>Gestor de contraseñas:</strong> software para crear y guardar claves únicas y seguras.</li>
        <li><strong>2FA/MFA:</strong> verificación en dos o más factores para reforzar el acceso.</li>
        <li><strong>Huella digital:</strong> rastro de información que dejas al usar servicios en línea.</li>
        <li><strong>Principio de mínimo privilegio:</strong> otorgar solo los accesos estrictamente necesarios.</li>
      </ul>
    </div>
  </section>

  <!-- FUENTES Y CRÉDITOS -->
  <section id="fuentes" class="reveal" aria-labelledby="sec-fuentes">
    <h2 id="sec-fuentes">Fuentes y créditos</h2>
    <div class="card">
      <ul>
        <li>INTERPOL — <a href="https://www.interpol.int/en/Crimes/Cybercrime/Be-Cyber-Aware" target="_blank" rel="noopener">Be Cyber Aware</a></li>
        <li>SSPC/Gob.mx — <a href="https://www.gob.mx/sspc/documentos/ciberguia?idiom=es" target="_blank" rel="noopener">Ciberguía</a></li>
        <li>INAI (México) — <a href="https://inicio.inai.org.mx/Guias/Gu%C3%ADa_Prevenir_RI.pdf" target="_blank" rel="noopener">Guía para prevenir robo de identidad</a></li>
        <li>LGPDPPSO — <a href="https://www.diputados.gob.mx/LeyesBiblio/pdf/LGPDPPSO.pdf" target="_blank" rel="noopener">Protección de datos personales</a></li>
      </ul>
      <p class="muted">Última actualización: <span id="last-update"></span></p>
    </div>
  </section>
  <section id="infografias" class="reveal" aria-labelledby="sec-infografias">
    <h2 id="sec-infografias">Infografías</h2>
    <div class="grid cols-3">
      <figure class="card">
        <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD..." alt="Infografía: Ciberseguridad — cartel principal" loading="lazy" style="width:100%;height:auto;border-radius:12px;"/>
        <figcaption class="muted">Crédito: Equipo del proyecto (Canva). Si no se visualiza aquí, se insertará directamente en Google Sites como imagen.</figcaption>
      </figure>
      <figure class="card">
        <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD..." alt="Infografía: Conceptos de ciberseguridad" loading="lazy" style="width:100%;height:auto;border-radius:12px;"/>
        <figcaption class="muted">Crédito: Equipo del proyecto (Canva).</figcaption>
      </figure>
      <figure class="card">
        <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD..." alt="Infografía: Consejos de ciberseguridad" loading="lazy" style="width:100%;height:auto;border-radius:12px;"/>
        <figcaption class="muted">Crédito: Equipo del proyecto (Canva).</figcaption>
      </figure>
    </div>
  </section>
</main>

<a class="top" href="#inicio" aria-label="Volver arriba" id="backtop">↑</a>
<footer role="contentinfo">
  <p>© Guía Segura — Sitio educativo para toda audiencia.</p>
</footer>

<script>
  // Respeta preferencias de movimiento
  const prefersReduced = window.matchMedia('(prefers-reduced-motion: reduce)').matches;

  // Aparición al hacer scroll
  if(!prefersReduced){
    const io = new IntersectionObserver((entries)=>{
      entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('visible'); io.unobserve(e.target);} });
    },{threshold:0.12});
    document.querySelectorAll('.reveal').forEach(el=>io.observe(el));
  } else {
    document.querySelectorAll('.reveal').forEach(el=>el.classList.add('visible'));
  }

  // Scrollspy (enlace activo)
  const sections = Array.from(document.querySelectorAll('main section[id], header.hero#inicio'));
  const links = Array.from(document.querySelectorAll('#navlinks a'));
  const byId = id => links.find(a=>a.getAttribute('href') === '#' + id);
  const spy = new IntersectionObserver((entries)=>{
    entries.forEach(entry=>{
      const id = entry.target.getAttribute('id') || 'inicio';
      const link = byId(id);
      if(link){ if(entry.isIntersecting){ links.forEach(a=>a.classList.remove('active')); link.classList.add('active'); }}
    });
  },{rootMargin:'-40% 0px -55% 0px', threshold:[0, .5, 1]});
  sections.forEach(sec=>spy.observe(sec));

  // Botón volver arriba
  const topBtn = document.getElementById('backtop');
  const showTop = ()=>{ if(window.scrollY > 600){ topBtn.classList.add('show'); } else { topBtn.classList.remove('show'); } };
  window.addEventListener('scroll', showTop); showTop();

  // Sello de última actualización
  const d = new Date();
  const fmt = d.toLocaleDateString('es-MX', {year:'numeric', month:'long', day:'numeric'});
  const out = document.getElementById('last-update'); if(out) out.textContent = fmt;
</script>
</body>
</html>
