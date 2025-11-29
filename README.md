<!doctype html>
<html lang="es">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>CATÁLOGO — Disc Night Producciones</title>
<style>
  :root{
    --bg:#030417;
    --panel:#071827;
    --accent:#0ea5ff;
    --muted:#a9bac6;
    --glass: rgba(255,255,255,0.03);
    --max-width:1200px;
  }
  *{box-sizing:border-box}
  html,body{height:100%;margin:0;font-family:Inter, "Segoe UI", Roboto, Arial, sans-serif;background:var(--bg);color:#fff;-webkit-font-smoothing:antialiased}
  body{
    background-image:
      linear-gradient(rgba(0,0,0,0.35), rgba(0,0,0,0.35)),
      url('https://i.ibb.co/B2mDdYcm/imagen-de-fondo.jpg'),
      url('images/bg-stage.jpg');
    background-size:cover;
    background-position:center;
    background-attachment:fixed;
    padding:16px;
    display:flex;
    justify-content:center;
    align-items:flex-start;
    min-height:100vh;
  }
  .logo {
    position:fixed;
    top:12px; left:12px;
    width:72px; height:72px;
    padding:6px; border-radius:14px;
    background:linear-gradient(180deg,rgba(255,255,255,0.03),rgba(0,0,0,0.35));
    border:1px solid rgba(255,255,255,0.06);
    box-shadow:0 8px 30px rgba(0,0,0,0.6);
    z-index:120;
  }
  .logo img{width:100%;height:100%;object-fit:cover;border-radius:10px;display:block}
  .wrap{width:100%;max-width:var(--max-width);margin:32px 0;display:flex;flex-direction:column;gap:18px;align-items:center;padding:12px}
  .hero{width:100%;max-width:920px;padding:28px 18px;display:flex;flex-direction:column;align-items:center;gap:6px;text-align:center;background:linear-gradient(180deg,rgba(0,0,0,0.45),rgba(0,0,0,0.2));border-radius:14px;border:1px solid rgba(255,255,255,0.04);box-shadow:0 18px 60px rgba(0,0,0,0.6);position:relative;}
  .hero h1{margin:0;font-size:28px;letter-spacing:6px;text-transform:uppercase;color:rgba(255,255,255,0.98);font-weight:800;text-shadow:0 6px 26px rgba(0,0,0,0.6);}
  .hero h2{margin:6px 0 0;font-size:18px;color:var(--accent);letter-spacing:2px;font-weight:700;}
  .welcome{margin-top:10px;font-size:16px;color:var(--muted);text-align:center;padding:8px 14px;border-radius:8px;background:rgba(255,255,255,0.015);border:1px solid rgba(255,255,255,0.02);max-width:780px;}
  .btn-instagram {
    display: inline-block;
    margin-top:16px;
    margin-bottom:8px;
    padding:11px 20px;
    border-radius:10px;
    background: linear-gradient(90deg,#d6249f 60%, #285AEB 100%);
    color:#fff;
    font-weight:800;
    font-size:16px;
    text-decoration:none;
    box-shadow:0 2px 18px rgba(214,36,159,0.12);
    text-align:center;
    transition:background .2s;
    border:none;
  }
  .btn-instagram:hover,
  .btn-instagram:focus {
    background: linear-gradient(90deg,#285AEB 40%, #d6249f 100%);
    color:#fff;
  }
  .catalog{width:100%;max-width:980px;display:grid;grid-template-columns:1fr;gap:12px;margin-top:6px;}
  .card{display:flex;gap:12px;align-items:center;padding:14px;border-radius:12px;background:linear-gradient(180deg,rgba(255,255,255,0.02),rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.03);box-shadow:0 8px 24px rgba(0,0,0,0.45);}
  .thumb{width:88px;height:88px;min-width:88px;border-radius:10px;overflow:hidden;background:linear-gradient(180deg,#022b3a,#00131a);display:flex;align-items:center;justify-content:center;border:2px solid rgba(14,165,255,0.06);}
  .thumb img{width:100%;height:100%;object-fit:cover;display:block;}
  .meta{flex:1;display:flex;flex-direction:column;gap:8px;}
  .meta h3{margin:0;font-size:15px;color:var(--accent);text-transform:uppercase;letter-spacing:1.4px}
  .meta p{margin:0;color:var(--muted);font-size:13px;line-height:1.35}
  .meta .row{display:flex;gap:8px;align-items:center;flex-wrap:wrap;margin-top:6px}
  .btn{padding:8px 12px;border-radius:8px;border:1px solid rgba(14,165,255,0.12);background:transparent;color:var(--accent);font-weight:700;cursor:pointer}
  .hint{color:var(--muted);font-size:13px;text-align:center;margin-top:10px}
  .modal{position:fixed;inset:0;display:none;align-items:center;justify-content:center;background:linear-gradient(90deg, rgba(0,0,0,0.6), rgba(0,0,0,0.9));padding:18px;z-index:210}
  .modal.show{display:flex}
  .panel{width:100%;max-width:720px;background:linear-gradient(180deg,#071a28,#041426);border-radius:12px;padding:16px;border:1px solid rgba(14,165,255,0.06);box-shadow:0 28px 80px rgba(0,0,0,0.7)}
  .panel .head{display:flex;align-items:center;justify-content:space-between;gap:12px}
  .panel img{width:160px;height:120px;object-fit:cover;border-radius:8px;border:2px solid rgba(255,255,255,0.03)}
  .panel .desc{color:var(--muted);margin-top:8px;font-size:14px;line-height:1.4}
  @media(min-width:720px){
    .catalog{grid-template-columns:repeat(2, 1fr); gap:16px;}
    .hero h1{font-size:36px; letter-spacing:8px;}
    .logo{width:120px;height:120px;padding:8px;border-radius:16px;top:18px;left:18px;}
    .thumb{width:110px;height:110px;min-width:110px;}
  }
  @media(min-width:1100px){
    .catalog{grid-template-columns:repeat(3, 1fr);}
    .hero{padding:34px 28px;}
    .hero h1{font-size:52px;}
    .hero h2{font-size:22px;}
    .logo{width:160px;height:160px;padding:10px;border-radius:18px;top:22px;left:22px;}
    .thumb{width:140px;height:120px;min-width:140px;}
  }
  @media(max-width:420px){
    body{padding:10px;background-attachment:scroll;}
    .hero{padding:18px 10px;}
    .hero h1{font-size:22px;letter-spacing:4px;}
    .hero h2{font-size:16px;}
    .welcome{font-size:14px;}
    .card{padding:12px;}
    .thumb{width:72px;height:72px;min-width:72px;}
    .meta h3{font-size:14px;}
    .meta p{font-size:13px;}
    .logo{width:64px;height:64px;padding:6px;}
    .panel img{width:120px;height:90px;}
    .btn-instagram{font-size:13px;padding:8px 12px;}
  }
  @media(max-width:640px){
    body{ background-attachment:scroll; }
  }
  .card:focus{outline:3px solid rgba(14,165,255,0.12);outline-offset:4px}
  .btn:focus{outline:2px solid rgba(14,165,255,0.12)}
</style>
</head>
<body>
  <div class="logo" role="img" aria-label="Disc Night Producciones - logo" title="Disc Night Producciones">
    <img
      src="https://i.ibb.co/bgG0yc5j/Dnlogo.png"
      alt="Disc Night logo"
      loading="lazy"
      decoding="async"
      onerror="this.onerror=null; this.src='images/Dnlogo.png';"
    >
  </div>

  <main class="wrap" role="main" aria-labelledby="main-title">
    <section class="hero">
      <h1 id="main-title">CATÁLOGO DISC NIGHT</h1>
      <h2>BIENVENIDOS</h2>
      <!-- Botón Instagram aquí -->
      <a href="https://www.instagram.com/dnproducciones/" target="_blank" class="btn-instagram">
        <img src="https://cdn-icons-png.flaticon.com/512/87/87390.png" alt="Instagram" style="width:22px;height:22px;vertical-align:middle;margin-right:8px;">
        Ir al Instagram Oficial
      </a>
      <div class="welcome">Servicios profesionales para eventos — sonido, luces, pantallas y streaming. Toca un servicio para ver detalles.</div>
    </section>

    <section class="catalog" aria-label="Listado de servicios" id="catalog">
      <!-- Aquí todas tus cards de servicios -->
      <article class="card" tabindex="0" data-id="1" aria-label="Servicio técnico">
        <div class="thumb">
          <img src="https://i.ibb.co/pr2qctWP/Tecnico-en-sonido.jpg" alt="Técnico en sonido" loading="lazy"
               decoding="async" onerror="this.onerror=null; this.src='images/svc1.jpg';">
        </div>
        <div class="meta">
          <h3>Servicio técnico</h3>
          <p>Montaje, supervisión y operación técnica en sitio. Soporte y pruebas previas.</p>
          <div class="row"><button class="btn" data-id="1" aria-label="Ver productos servicio técnico">Ver productos</button></div>
        </div>
      </article>
      <article class="card" tabindex="0" data-id="2" aria-label="Microfonía">
        <div class="thumb">
          <img src="https://i.ibb.co/dyBsfNs/microfonos.jpg" alt="Microfonía" loading="lazy"
               decoding="async" onerror="this.onerror=null; this.src='images/svc2.jpg';">
        </div>
        <div class="meta">
          <h3>Microfonía</h3>
          <p>Micrófonos dinámicos y condensador con colocación y ajuste profesional.</p>
          <div class="row"><button class="btn" data-id="2" aria-label="Ver productos microfonía">Ver productos</button></div>
        </div>
      </article>
      <article class="card" tabindex="0" data-id="3" aria-label="Sonido en general">
        <div class="thumb">
          <img src="https://i.ibb.co/KpVJ8T3T/sonido.jpg" alt="Sonido en general" loading="lazy"
               decoding="async" onerror="this.onerror=null; this.src='images/svc3.jpg';">
        </div>
        <div class="meta">
          <h3>Sonido en general</h3>
          <p>Sistemas PA, monitores y mezcla para conciertos y presentaciones de todo tamaño.</p>
          <div class="row"><button class="btn" data-id="3" aria-label="Ver productos sonido">Ver productos</button></div>
        </div>
      </article>
      <article class="card" tabindex="0" data-id="4" aria-label="Pantallas LED">
        <div class="thumb">
          <img src="https://i.ibb.co/WWHKbzMk/pantallaled.jpg" alt="Pantallas LED" loading="lazy"
               decoding="async" onerror="this.onerror=null; this.src='images/svc4.jpg';">
        </div>
        <div class="meta">
          <h3>Pantallas LED</h3>
          <p>Alquiler, instalación y operación de pantallas LED para shows y publicidad.</p>
          <div class="row"><button class="btn" data-id="4" aria-label="Ver productos pantallas LED">Ver productos</button></div>
        </div>
      </article>
      <article class="card" tabindex="0" data-id="5" aria-label="Luces LED">
        <div class="thumb">
          <img src="https://i.ibb.co/ccS6gNZ6/luces-eventos.jpg" alt="Luces LED" loading="lazy"
               decoding="async" onerror="this.onerror=null; this.src='images/svc5.jpg';">
        </div>
        <div class="meta">
          <h3>Luces LED</h3>
          <p>Iluminación y efectos: uplights, wash, móviles y programación para eventos.</p>
          <div class="row"><button class="btn" data-id="5" aria-label="Ver productos luces LED">Ver productos</button></div>
        </div>
      </article>
      <article class="card" tabindex="0" data-id="6" aria-label="Estructuras">
        <div class="thumb">
          <img src="https://i.ibb.co/YxZfNb4/structura.jpg" alt="Estructuras" loading="lazy"
               decoding="async" onerror="this.onerror=null; this.src='images/svc6.jpg';">
        </div>
        <div class="meta">
          <h3>Estructuras</h3>
          <p>Montaje e instalación de estructuras, tarimas y soportes para escenarios y producción de eventos.</p>
          <div class="row"><button class="btn" data-id="6" aria-label="Ver productos estructuras">Ver productos</button></div>
        </div>
      </article>
    </section>

    <div class="hint">© 2025 Disc Night Producciones — contacto@discnigth.pro · Tel: +00 000 0000</div>
  </main>
  <div id="modal" class="modal" aria-hidden="true" onclick="closeModal(event)">
    <div class="panel" role="dialog" aria-modal="true" onclick="event.stopPropagation()">
      <div class="head">
        <strong id="m-title" style="color:var(--accent)"></strong>
        <button class="btn close" aria-label="Cerrar" onclick="closeModal()">✕</button>
      </div>
      <div style="display:flex;gap:12px;align-items:flex-start;flex-wrap:wrap;margin-top:12px">
        <img id="m-img" src="" alt="" onerror="this.style.display='none'">
        <div class="desc" id="m-desc"></div>
      </div>
      <div style="display:flex;justify-content:flex-end;gap:8px;margin-top:12px">
        <button class="btn" onclick="contact()">Solicitar cotización</button>
        <button class="btn" onclick="closeModal()">Cerrar</button>
      </div>
    </div>
  </div>
  <script>
    document.addEventListener('click', e=>{
      const btn = e.target.closest('.btn[data-id]');
      if(btn && btn.dataset.id){
        window.location.href = 'Productos.html';
        return;
      }
    });
    document.addEventListener('keydown', e=>{
      if((e.key === 'Enter' || e.key === ' ') && document.activeElement?.classList?.contains('card')){
        e.preventDefault();
        document.activeElement.querySelector('.btn[data-id]').click();
      }
    });
    if(window.matchMedia('(max-width:640px)').matches) document.body.style.backgroundAttachment = 'scroll';
    function openModal(id){}
    function closeModal(e){}
    function contact(){ window.location.href = 'mailto:contacto@discnigth.pro?subject=Cotización%20Disc%20Night'; }
  </script>
</body>
</html>
