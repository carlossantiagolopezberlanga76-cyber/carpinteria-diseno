index.html
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>W. Carpintería & Diseño</title>
<meta name="description" content="Diseño y fabricación de muebles a medida, cocinas integrales, clósets y proyectos personalizados de carpintería.">
<meta name="theme-color" content="#3b2a1d">

<meta property="og:type" content="website">
<meta property="og:locale" content="es_MX">
<meta property="og:site_name" content="W. Carpintería & Diseño">
<meta property="og:title" content="W. Carpintería & Diseño">
<meta property="og:description" content="Diseño y fabricación de muebles a medida, cocinas integrales, clósets y proyectos personalizados de carpintería.">
<meta property="og:image" content="images/preview.jpg">
<meta property="og:image:secure_url" content="images/preview.jpg">
<meta property="og:image:type" content="image/jpeg">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
<meta property="og:image:alt" content="Proyecto de carpintería a medida de W. Carpintería & Diseño">
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="W. Carpintería & Diseño">
<meta name="twitter:description" content="Diseño y fabricación de muebles a medida, cocinas integrales, clósets y proyectos personalizados de carpintería.">
<meta name="twitter:image" content="images/preview.jpg">
<meta name="twitter:image:alt" content="Proyecto de carpintería a medida de W. Carpintería & Diseño">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="preload" as="image" href="images/proyectos/barras/barra-02.jpg" fetchpriority="high">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600;700&family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>
:root{
    --gold:#c89b3c;
    --gold-dark:#a67d29;
    --brown:#3b2a1d;
    --cream:#f8f6f2;
    --ink:#2d2926;
}

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
}

html{
    scroll-behavior:smooth;
}

body{
    background:#fff;
    color:var(--ink);
}

header{
    min-height:100vh;
    background:
    linear-gradient(90deg,rgba(20,14,10,.76),
    rgba(20,14,10,.3)),
    url('images/proyectos/barras/barra-02.jpg');
    background-size:cover;
    background-position:center;
    display:flex;
    flex-direction:column;
}

nav{
    position:absolute;
    top:0;
    left:0;
    width:100%;
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:18px 5%;
    background:rgba(35,25,18,.32);
    border-bottom:1px solid rgba(255,255,255,.12);
    backdrop-filter:blur(10px);
    z-index:10;
}

.logo{
    display:flex;
    align-items:center;
    gap:12px;
    color:white;
    text-decoration:none;
}

.logo-mark{
    display:block;
    flex:0 0 46px;
    width:46px;
    height:46px;
    color:var(--gold);
}

.logo-copy{
    display:flex;
    flex-direction:column;
    align-items:flex-start;
    gap:3px;
    line-height:1.1;
    white-space:nowrap;
}

.logo-copy strong{
    color:white;
    font:600 17px 'Playfair Display',serif;
    letter-spacing:.3px;
}

.logo-copy span{
    color:var(--gold);
    font-size:9px;
    font-weight:600;
    letter-spacing:2px;
}

.menu-toggle{
    display:none;
    width:44px;
    height:44px;
    padding:10px;
    border:1px solid rgba(255,255,255,.35);
    border-radius:10px;
    background:transparent;
    cursor:pointer;
}

.menu-toggle span{
    display:block;
    height:2px;
    margin:4px 0;
    background:#fff;
    transition:transform .2s,opacity .2s;
}

nav.menu-open .menu-toggle span:first-child{
    transform:translateY(6px) rotate(45deg);
}

nav.menu-open .menu-toggle span:nth-child(2){
    opacity:0;
}

nav.menu-open .menu-toggle span:last-child{
    transform:translateY(-6px) rotate(-45deg);
}

nav ul{
    display:flex;
    list-style:none;
    gap:16px;
}

nav ul li a{
    color:white;
    text-decoration:none;
    transition:color .18s ease-out;
    font-weight:500;
    font-size:14px;
}

nav ul li a:hover{
    color:var(--gold);
}

nav ul li .nav-cta{
    padding:11px 18px;
    border-radius:50px;
    background:var(--gold);
    color:white;
    font-weight:600;
    white-space:nowrap;
}

nav ul li .nav-cta:hover{
    background:var(--gold-dark);
    color:white;
}

.hero{
    flex:1;
    display:flex;
    justify-content:flex-start;
    align-items:center;
    color:white;
    padding:120px 8% 60px;
}

.hero-content{
    max-width:720px;
}

.hero-eyebrow,
.seccion-etiqueta{
    color:var(--gold);
    font-size:12px;
    font-weight:600;
    letter-spacing:2px;
    text-transform:uppercase;
}

.hero-eyebrow{
    margin-bottom:18px;
}

.hero-content h1{
    font-family:'Playfair Display',serif;
    font-size:clamp(48px,7vw,78px);
    font-weight:600;
    line-height:1.05;
    margin-bottom:22px;
}

.hero-content p{
    max-width:620px;
    font-size:18px;
    line-height:1.7;
    margin-bottom:28px;
    color:rgba(255,255,255,.9);
}

.hero-actions{
    display:flex;
    align-items:center;
    flex-wrap:wrap;
    gap:14px;
}

.btn{
    display:inline-block;
    padding:15px 35px;
    background:var(--gold);
    color:white;
    text-decoration:none;
    border-radius:50px;
    font-weight:600;
    transition:background-color .18s ease-out,transform .18s ease-out;
}

.btn:hover,
.btn:focus-visible{
    background:var(--gold-dark);
    transform:translateY(-2px);
}

.btn-secondary{
    display:inline-block;
    padding:13px 22px;
    border:1px solid rgba(255,255,255,.65);
    border-radius:50px;
    color:white;
    text-decoration:none;
    font-weight:500;
    transition:background-color .18s ease-out;
}

.btn-secondary:hover{
    background:rgba(255,255,255,.12);
}

.hero-note{
    margin-top:17px;
    color:rgba(255,255,255,.78);
    font-size:13px;
}

.beneficios{
    position:relative;
    z-index:2;
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:20px;
    width:min(90%,1080px);
    margin:-42px auto 0;
    padding:24px 30px;
    border:1px solid #eee7dc;
    border-radius:16px;
    background:white;
    box-shadow:0 16px 45px rgba(59,42,29,.1);
}

.beneficio{
    display:flex;
    align-items:center;
    gap:14px;
}

.beneficio-numero{
    display:grid;
    flex:0 0 42px;
    place-items:center;
    width:42px;
    height:42px;
    border-radius:50%;
    background:var(--cream);
    color:var(--gold-dark);
    font-family:'Playfair Display',serif;
    font-size:18px;
}

.beneficio strong,
.beneficio small{
    display:block;
}

.beneficio strong{
    color:var(--brown);
    font-size:14px;
}

.beneficio small{
    margin-top:3px;
    color:#746b63;
    font-size:12px;
}

section{
    padding:96px 10%;
}

.seccion-etiqueta{
    margin-bottom:12px;
    text-align:center;
}

.titulo{
    text-align:center;
    font-size:40px;
    margin-bottom:18px;
    color:var(--brown);
    font-family:'Playfair Display',serif;
    font-weight:600;
}

.seccion-descripcion{
    max-width:650px;
    margin:0 auto 48px;
    color:#665f59;
    line-height:1.8;
    text-align:center;
}

.servicios{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:25px;
}

.card{
    background:white;
    padding:38px 30px;
    border:1px solid #eee7dc;
    border-radius:18px;
    text-align:left;
    box-shadow:0 12px 35px rgba(59,42,29,.06);
    transition:transform .2s ease-out,box-shadow .2s ease-out;
}

.card:hover{
    transform:translateY(-4px);
    box-shadow:0 18px 40px rgba(59,42,29,.12);
}

.card h3{
    margin-bottom:12px;
    color:var(--brown);
}

.card p{
    line-height:1.7;
    color:#665f59;
}

.card-number{
    display:inline-grid;
    place-items:center;
    width:44px;
    height:44px;
    margin-bottom:20px;
    border-radius:50%;
    background:#f5eee1;
    color:var(--gold-dark);
    font-weight:700;
}

.proceso{
    background:var(--cream);
}

.pasos{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:28px;
    max-width:1050px;
    margin:0 auto;
}

.paso{
    padding:8px 26px 8px 0;
    border-right:1px solid #ded5c8;
}

.paso:last-child{
    border-right:0;
}

.paso-numero{
    display:block;
    margin-bottom:15px;
    color:var(--gold-dark);
    font:600 34px 'Playfair Display',serif;
}

.paso h3{
    margin-bottom:9px;
    color:var(--brown);
    font-size:18px;
}

.paso p{
    color:#665f59;
    line-height:1.7;
}

.categorias{
    display:grid;
    grid-template-columns:repeat(4,minmax(0,1fr));
    gap:20px;
}

.categoria-card{
    position:relative;
    height:270px;
    padding:0;
    overflow:hidden;
    border:0;
    border-radius:15px;
    background:var(--brown);
    color:white;
    cursor:pointer;
    text-align:left;
}

.categoria-card img{
    width:100%;
    height:100%;
    object-fit:cover;
    transition:transform .24s ease-out;
}

.categoria-card::after{
    position:absolute;
    inset:30% 0 0;
    background:linear-gradient(transparent,rgba(25,18,13,.86));
    content:"";
}

.categoria-card:hover img{
    transform:scale(1.03);
}

.categoria-card:focus-visible{
    outline:3px solid var(--gold);
    outline-offset:4px;
}

.categoria-info{
    position:absolute;
    z-index:1;
    right:0;
    bottom:0;
    left:0;
    display:flex;
    flex-direction:column;
    align-items:flex-start;
    gap:7px;
    padding:22px;
}

.categoria-info small{
    display:block;
    color:#f0d99e;
    font-size:10px;
    font-weight:600;
    letter-spacing:1.5px;
}

.categoria-info strong{
    font:600 25px 'Playfair Display',serif;
}

.categoria-info span{
    font-size:13px;
    font-weight:500;
}

.visor-categoria{
    width:min(94vw,1160px);
    max-height:88vh;
    max-width:none;
    margin:auto;
    padding:42px 32px 32px;
    overflow-y:auto;
    border:1px solid rgba(255,255,255,.16);
    border-radius:18px;
    background:#1d1916;
    color:white;
}

.visor-categoria[open]{
    display:block;
}

.visor-categoria::backdrop{
    background:rgba(15,12,10,.88);
    backdrop-filter:blur(5px);
}

.visor-categoria-cerrar{
    position:absolute;
    top:14px;
    right:14px;
    display:grid;
    place-items:center;
    width:40px;
    height:40px;
    border:1px solid rgba(255,255,255,.3);
    border-radius:50%;
    background:rgba(255,255,255,.08);
    color:white;
    cursor:pointer;
    font-size:25px;
}

.visor-categoria-cerrar:hover{
    border-color:var(--gold);
    background:var(--gold-dark);
}

.visor-categoria-header{
    padding-right:42px;
    margin-bottom:24px;
}

.visor-categoria-header p:first-child{
    margin-bottom:7px;
    color:#e7c77f;
    font-size:11px;
    font-weight:600;
    letter-spacing:1.6px;
    text-transform:uppercase;
}

.visor-categoria-header h2{
    margin-bottom:8px;
    font:600 34px 'Playfair Display',serif;
}

#visor-categoria-descripcion{
    color:rgba(255,255,255,.75);
    line-height:1.6;
}

.visor-categoria-cotizar{
    margin-top:16px;
    padding:12px 24px;
    font-size:14px;
}

.visor-categoria-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:16px;
}

.visor-categoria-grid figure{
    position:relative;
    height:230px;
    margin:0;
    overflow:hidden;
    border-radius:12px;
    background:var(--brown);
}

.visor-categoria-grid img{
    width:100%;
    height:100%;
    object-fit:cover;
}

.visor-categoria-grid figcaption{
    position:absolute;
    right:0;
    bottom:0;
    left:0;
    padding:28px 14px 12px;
    background:linear-gradient(transparent,rgba(25,18,13,.85));
    color:white;
    font-size:13px;
    font-weight:500;
}

.galeria-intro{
    max-width:650px;
    margin:0 auto 34px;
    color:#665f59;
    line-height:1.7;
    text-align:center;
}

.nosotros{
    text-align:left;
    max-width:900px;
    margin:auto;
    line-height:1.9;
    font-size:18px;
}

.contacto{
    background:var(--brown);
    color:white;
    text-align:center;
}

.contacto .seccion-etiqueta{
    color:#e7c77f;
}

.contacto h2{
    margin-bottom:15px;
    color:white;
    font:600 40px 'Playfair Display',serif;
}

.contacto > p{
    max-width:580px;
    margin:0 auto;
    color:rgba(255,255,255,.82);
    line-height:1.8;
}

.cotizacion-form{
    max-width:680px;
    margin:32px auto 0;
    padding:30px;
    border-radius:18px;
    background:white;
    box-shadow:0 18px 45px rgba(0,0,0,.16);
    color:var(--ink);
    text-align:left;
}

.form-fields{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:18px;
}

.form-group{
    margin-bottom:18px;
}

.form-group label{
    display:block;
    margin-bottom:7px;
    color:var(--brown);
    font-size:14px;
    font-weight:600;
}

.form-group input,
.form-group select,
.form-group textarea{
    width:100%;
    padding:12px 14px;
    border:1px solid #ded5c8;
    border-radius:10px;
    background:#fff;
    color:var(--ink);
    font-size:14px;
}

.form-group textarea{
    min-height:115px;
    resize:vertical;
}

.form-group input:focus,
.form-group select:focus,
.form-group textarea:focus{
    border-color:var(--gold);
    outline:2px solid rgba(200,155,60,.2);
}

.form-note{
    margin-bottom:16px;
    color:#746b63;
    font-size:12px;
    line-height:1.6;
}

.cotizacion-form .btn{
    width:100%;
    border:0;
    cursor:pointer;
}

.contacto .btn{
    margin-top:26px;
    color:#fff;
}

.contacto .cotizacion-form .btn{
    margin-top:0;
}

.contacto-links{
    display:flex;
    justify-content:center;
    flex-wrap:wrap;
    gap:14px;
    margin-top:28px;
}

.contacto-links a{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    min-width:220px;
    padding:14px 22px;
    border:1px solid rgba(255,255,255,.28);
    border-radius:50px;
    color:white;
    text-decoration:none;
    transition:background-color .18s ease-out,border-color .18s ease-out;
}

.contacto-links a:first-child{
    background:rgba(255,255,255,.08);
}

.contacto-links a:hover{
    background:var(--gold);
    border-color:var(--gold);
}

footer{
    background:#222;
    color:white;
    text-align:center;
    padding:20px;
}

.whatsapp{
    position:fixed;
    right:20px;
    bottom:20px;
    width:65px;
    height:65px;
    background:#25D366;
    border-radius:50%;
    display:flex;
    justify-content:center;
    align-items:center;
    text-decoration:none;
    color:white;
    box-shadow:0 5px 15px rgba(0,0,0,.3);
    z-index:999;
    transition:transform .18s ease-out;
}

.whatsapp svg{
    display:block;
    width:36px;
    height:36px;
    fill:currentColor;
    fill-rule:evenodd;
    clip-rule:evenodd;
}

.whatsapp:hover{
    transform:scale(1.05);
}

button:focus-visible,
a:focus-visible{
    outline:3px solid var(--gold);
    outline-offset:4px;
}

@media(max-width:900px){

nav{
    padding:16px 5%;
}

.logo-copy strong{
    font-size:15px;
}

.logo-copy span{
    font-size:8px;
}

.menu-toggle{
    display:block;
}

nav ul{
    display:none;
    position:absolute;
    top:100%;
    right:0;
    left:0;
    flex-direction:column;
    gap:0;
    padding:10px 5% 16px;
    background:rgba(35,25,18,.97);
    border-top:1px solid rgba(255,255,255,.12);
}

nav ul.is-open{
    display:flex;
}

nav ul li a{
    display:block;
    padding:11px 4px;
    font-size:15px;
}

nav ul li .nav-cta{
    margin-top:8px;
    padding:11px 16px;
    text-align:center;
}

.hero{
    align-items:flex-end;
    padding:140px 6% 70px;
}

.hero-content h1{
    font-size:42px;
}

.hero-content p{
    font-size:17px;
}

section{
    padding:72px 6%;
}

.titulo{
    font-size:32px;
}

.paso{
    padding-right:18px;
}

.categorias{
    grid-template-columns:repeat(2,minmax(0,1fr));
}

.visor-categoria{
    width:96vw;
    max-height:88vh;
    padding:46px 16px 18px;
}

.visor-categoria-grid{
    grid-template-columns:repeat(2,minmax(0,1fr));
    gap:10px;
}

.visor-categoria-grid figure{
    height:170px;
}
}

@media(max-width:560px){
.logo-mark{
    width:40px;
    height:40px;
    flex-basis:40px;
}

.logo{
    gap:9px;
}

.logo-copy{
    gap:2px;
}

.logo-copy strong{
    font-size:14px;
}

.logo-copy span{
    font-size:8px;
    letter-spacing:1.5px;
}

.hero-content h1{
    font-size:38px;
}

.categorias{
    grid-template-columns:1fr;
}

.categoria-card{
    height:230px;
}

.visor-categoria-header h2{
    font-size:28px;
}

.visor-categoria-grid figure{
    height:145px;
}

.cotizacion-form{
    padding:22px 18px;
}

.form-fields{
    grid-template-columns:1fr;
    gap:0;
}

.hero-actions{
    align-items:stretch;
    flex-direction:column;
}

.hero-actions .btn,
.hero-actions .btn-secondary{
    text-align:center;
}

.beneficios{
    grid-template-columns:1fr;
    gap:16px;
    margin-top:-28px;
    padding:20px;
}

.pasos{
    grid-template-columns:1fr;
    gap:22px;
}

.paso{
    padding:0 0 20px;
    border-right:0;
    border-bottom:1px solid #ded5c8;
}

.paso:last-child{
    border-bottom:0;
}

.seccion-descripcion{
    margin-bottom:34px;
}

.galeria-intro{
    margin-bottom:28px;
}
}

@media(prefers-reduced-motion:reduce){
html{
    scroll-behavior:auto;
}

*,*::before,*::after{
    transition-duration:.01ms !important;
    animation-duration:.01ms !important;
    animation-iteration-count:1 !important;
}
}
</style>
</head>

<body>

<header>

<nav aria-label="Navegación principal">
    <a class="logo" href="#inicio" aria-label="W. Carpintería y Diseño, inicio">
        <svg class="logo-mark" viewBox="0 0 56 56" aria-hidden="true" focusable="false">
            <rect x="1.5" y="1.5" width="53" height="53" rx="15" fill="rgba(255,255,255,.035)" stroke="currentColor" stroke-opacity=".72"/>
            <path d="M13 18 20.5 38 28 24 35.5 38 43 18" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M17 44h22" fill="none" stroke="currentColor" stroke-width="1.2" stroke-linecap="round" stroke-opacity=".7"/>
        </svg>
        <span class="logo-copy"><strong>W. CARPINTERÍA</strong><span>& DISEÑO</span></span>
    </a>
    <button class="menu-toggle" type="button" aria-label="Abrir menú" aria-expanded="false" aria-controls="menu-principal">
        <span></span><span></span><span></span>
    </button>

    <ul id="menu-principal">
        <li><a href="#inicio">Inicio</a></li>
        <li><a href="#servicios">Servicios</a></li>
        <li><a href="#galeria">Galería</a></li>
        <li><a href="#nosotros">Nosotros</a></li>
        <li><a href="#contacto">Contacto</a></li>
        <li><a class="nav-cta" href="https://wa.me/528126358909?text=Hola,%20quiero%20cotizar%20un%20proyecto%20de%20carpinter%C3%ADa" target="_blank" rel="noopener noreferrer">Cotizar ahora</a></li>
    </ul>
</nav>

<div class="hero" id="inicio">
    <div class="hero-content">
        <p class="hero-eyebrow">Carpintería y diseño a medida</p>
        <h1>Tu espacio,<br>diseñado para ti.</h1>
        <p>Muebles, cocinas y clósets creados para aprovechar cada espacio y reflejar tu estilo.</p>
        <div class="hero-actions">
            <a href="https://wa.me/528126358909?text=Hola,%20quiero%20cotizar%20un%20proyecto%20de%20carpinter%C3%ADa" class="btn" target="_blank" rel="noopener noreferrer">Cotiza tu proyecto por WhatsApp</a>
            <a href="#galeria" class="btn-secondary">Explora ideas</a>
        </div>
        <p class="hero-note">Atención personalizada · Cotización sin compromiso</p>
    </div>
</div>

</header>

<div class="beneficios" aria-label="Beneficios de W. Carpintería y Diseño">
    <div class="beneficio">
        <span class="beneficio-numero" aria-hidden="true">01</span>
        <span><strong>Diseño a tu medida</strong><small>Hecho para tu espacio</small></span>
    </div>
    <div class="beneficio">
        <span class="beneficio-numero" aria-hidden="true">02</span>
        <span><strong>Atención personalizada</strong><small>Escuchamos tu idea</small></span>
    </div>
    <div class="beneficio">
        <span class="beneficio-numero" aria-hidden="true">03</span>
        <span><strong>Cotización sin compromiso</strong><small>Da el primer paso</small></span>
    </div>
</div>

<section id="servicios">
    <p class="seccion-etiqueta">Soluciones para tu hogar</p>
    <h2 class="titulo">Diseño que aprovecha cada espacio</h2>
    <p class="seccion-descripcion">Cuéntanos qué necesitas. Creamos propuestas de carpintería personalizadas para que cada rincón tenga una función y un estilo propio.</p>

    <div class="servicios">

        <div class="card">
            <span class="card-number" aria-hidden="true">01</span>
            <h3>Muebles a Medida</h3>
            <p>Diseñamos y fabricamos muebles personalizados para cualquier espacio.</p>
        </div>

        <div class="card">
            <span class="card-number" aria-hidden="true">02</span>
            <h3>Cocinas Integrales</h3>
            <p>Proyectos modernos y funcionales adaptados a tus necesidades.</p>
        </div>

        <div class="card">
            <span class="card-number" aria-hidden="true">03</span>
            <h3>Clósets y Vestidores</h3>
            <p>Aprovechamos cada espacio con acabados de calidad.</p>
        </div>

        <div class="card">
            <span class="card-number" aria-hidden="true">04</span>
            <h3>Diseño Interior</h3>
            <p>Ideas creativas para transformar tus espacios.</p>
        </div>

    </div>
</section>

<section class="proceso" id="proceso">
    <p class="seccion-etiqueta">Simple y personal</p>
    <h2 class="titulo">Así comienza tu proyecto</h2>
    <p class="seccion-descripcion">Te acompañamos desde la primera idea hasta definir una propuesta que se ajuste a lo que buscas.</p>
    <div class="pasos">
        <article class="paso">
            <span class="paso-numero">01</span>
            <h3>Cuéntanos tu idea</h3>
            <p>Escríbenos por WhatsApp y platícanos qué espacio quieres transformar.</p>
        </article>
        <article class="paso">
            <span class="paso-numero">02</span>
            <h3>Definimos lo que necesitas</h3>
            <p>Conversamos sobre medidas, estilo, materiales y los detalles de tu proyecto.</p>
        </article>
        <article class="paso">
            <span class="paso-numero">03</span>
            <h3>Recibe tu cotización</h3>
            <p>Preparamos una propuesta personalizada para que puedas tomar una decisión.</p>
        </article>
    </div>
</section>

<section id="galeria">
    <p class="seccion-etiqueta">Nuestro trabajo</p>
    <h2 class="titulo">Proyectos realizados</h2>
    <p class="galeria-intro">Conoce algunos trabajos de carpintería a medida. Cada proyecto se adapta al espacio, al estilo y a las necesidades de cada cliente.</p>

    <div class="categorias">
        <button class="categoria-card" type="button" data-categoria="cocinas" aria-label="Ver proyectos de cocinas integrales">
            <img src="images/proyectos/cocinas/cocina-01.jpg" alt="" loading="lazy" decoding="async">
            <span class="categoria-info"><small>03 FOTOS</small><strong>Cocinas integrales</strong><span>Ver proyectos</span></span>
        </button>
        <button class="categoria-card" type="button" data-categoria="vestidores" aria-label="Ver proyectos de vestidores y clósets">
            <img src="images/proyectos/vestidores/vestidor-01.jpg" alt="" loading="lazy" decoding="async">
            <span class="categoria-info"><small>02 FOTOS</small><strong>Vestidores y clósets</strong><span>Ver proyectos</span></span>
        </button>
        <button class="categoria-card" type="button" data-categoria="sala" aria-label="Ver proyectos de muebles y paneles">
            <img src="images/proyectos/sala/panel-01.jpg" alt="" loading="lazy" decoding="async">
            <span class="categoria-info"><small>04 FOTOS</small><strong>Muebles y paneles</strong><span>Ver proyectos</span></span>
        </button>
        <button class="categoria-card" type="button" data-categoria="barras" aria-label="Ver proyectos de barras y espacios sociales">
            <img src="images/proyectos/barras/barra-01.jpg" alt="" loading="lazy" decoding="async">
            <span class="categoria-info"><small>02 FOTOS</small><strong>Barras y espacios sociales</strong><span>Ver proyectos</span></span>
        </button>
    </div>
</section>

<dialog class="visor-categoria" id="visor-categoria" aria-labelledby="visor-categoria-titulo" aria-describedby="visor-categoria-descripcion">
    <button class="visor-categoria-cerrar" type="button" aria-label="Cerrar galería">×</button>
    <div class="visor-categoria-header">
        <p>Proyectos de W. Carpintería &amp; Diseño</p>
        <h2 id="visor-categoria-titulo"></h2>
        <p id="visor-categoria-descripcion"></p>
        <a class="btn visor-categoria-cotizar" id="visor-categoria-cotizar" href="#" target="_blank" rel="noopener noreferrer">Cotizar un proyecto similar por WhatsApp</a>
    </div>
    <div class="visor-categoria-grid" id="visor-categoria-grid"></div>
</dialog>

<section id="nosotros">
    <p class="seccion-etiqueta">El valor de lo personalizado</p>
    <h2 class="titulo">¿Quiénes Somos?</h2>

    <div class="nosotros">
        <p>
            En W. Carpintería & Diseño transformamos ideas en espacios únicos.
            Nos especializamos en la fabricación de muebles personalizados,
            cocinas integrales, clósets, puertas y proyectos de carpintería
            con acabados profesionales.
        </p>

        <br>

        <p>
            Nuestro compromiso es ofrecer calidad, diseño y atención personalizada
            para que cada proyecto refleje el estilo y las necesidades de nuestros clientes.
        </p>
    </div>
</section>

<section class="contacto" id="contacto">
    <p class="seccion-etiqueta">Hablemos de tu proyecto</p>
    <h2>Contáctanos</h2>
    <p>Cuéntanos qué tienes en mente y te ayudamos a dar el primer paso. Solicita una cotización sin compromiso.</p>
    <form class="cotizacion-form" id="cotizacion-form">
        <div class="form-fields">
            <div class="form-group">
                <label for="nombre-cliente">Tu nombre (opcional)</label>
                <input id="nombre-cliente" name="nombre" type="text" autocomplete="name" maxlength="60" placeholder="¿Cómo te llamas?">
            </div>
            <div class="form-group">
                <label for="tipo-proyecto">¿Qué quieres cotizar?</label>
                <select id="tipo-proyecto" name="proyecto" required>
                    <option value="">Elige una opción</option>
                    <option>Cocina integral</option>
                    <option>Vestidor o clóset</option>
                    <option>Mueble a medida</option>
                    <option>Dormitorio</option>
                    <option>Comedor</option>
                    <option>Puertas o paneles</option>
                    <option>Otro proyecto</option>
                </select>
            </div>
        </div>
        <div class="form-group">
            <label for="detalles-proyecto">Cuéntanos qué necesitas</label>
            <textarea id="detalles-proyecto" name="detalles" maxlength="600" placeholder="Por ejemplo: medidas aproximadas, materiales o estilo que te gustaría." required></textarea>
        </div>
        <p class="form-note">WhatsApp se abrirá con tu mensaje listo para enviar. La página no guarda tus datos.</p>
        <button class="btn" type="submit">Preparar cotización por WhatsApp</button>
    </form>
    <div class="contacto-links">
        <a href="tel:+528126358909">📞 +52 81 2635 8909</a>
        <a href="https://mail.google.com/mail/?view=cm&amp;fs=1&amp;to=wcarpinteriaydiseno%40gmail.com" target="_blank" rel="noopener noreferrer">📧 Enviar correo</a>
    </div>
</section>

<footer>
    © 2026 W. Carpintería & Diseño | Todos los derechos reservados
</footer>

<a class="whatsapp"
href="https://wa.me/528126358909?text=Hola,%20quiero%20una%20cotización%20para%20un%20proyecto%20de%20carpintería"
target="_blank" rel="noopener noreferrer" aria-label="Solicitar una cotización por WhatsApp">
    <svg viewBox="0 0 24 24" aria-hidden="true" focusable="false">
        <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.198-.347.223-.644.074-.297-.149-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.297-.347.446-.52.149-.174.198-.298.297-.496.1-.198.05-.372-.025-.521-.074-.149-.669-1.611-.916-2.207-.242-.579-.487-.5-.669-.51l-.57-.01c-.198 0-.52.074-.792.372s-1.04 1.016-1.04 2.479 1.064 2.875 1.213 3.074c.149.198 2.095 3.2 5.076 4.487.709.306 1.262.489 1.693.626.711.226 1.358.194 1.87.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.999-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64.001 5.122 1.03 6.99 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.888 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 0 5.495 0 12.05c0 2.124.556 4.196 1.613 6.023L0 24l6.09-1.598a12.02 12.02 0 005.757 1.464h.005c6.554 0 12.05-5.495 12.053-12.05a11.97 11.97 0 00-3.54-8.328z"/>
    </svg>
</a>

<script>
const menuToggle = document.querySelector('.menu-toggle');
const menu = document.querySelector('#menu-principal');
const navigation = document.querySelector('nav');

function closeMenu(){
    menuToggle.setAttribute('aria-expanded', 'false');
    menuToggle.setAttribute('aria-label', 'Abrir menú');
    menu.classList.remove('is-open');
    navigation.classList.remove('menu-open');
}

menuToggle.addEventListener('click', function(){
    const isOpen = menuToggle.getAttribute('aria-expanded') === 'true';
    menuToggle.setAttribute('aria-expanded', String(!isOpen));
    menuToggle.setAttribute('aria-label', isOpen ? 'Abrir menú' : 'Cerrar menú');
    menu.classList.toggle('is-open', !isOpen);
    navigation.classList.toggle('menu-open', !isOpen);
});

menu.querySelectorAll('a').forEach(function(link){
    link.addEventListener('click', closeMenu);
});

document.addEventListener('keydown', function(event){
    if(event.key === 'Escape'){
        closeMenu();
    }
});

const projectGalleries = {
    cocinas:{
        title:'Cocinas integrales',
        description:'Cocinas hechas a medida con combinaciones de materiales, colores y acabados.',
        images:[
            {src:'images/proyectos/cocinas/cocina-01.jpg',alt:'Cocina integral con gabinetes de madera clara y cubierta clara',caption:'Madera clara y líneas limpias'},
            {src:'images/proyectos/cocinas/cocina-02.jpg',alt:'Cocina integral oscura con detalles de madera',caption:'Contraste de madera y tonos oscuros'},
            {src:'images/proyectos/cocinas/cocina-03.jpg',alt:'Detalle de gabinetes rojos con cubierta clara',caption:'Color y acabado brillante'}
        ]
    },
    vestidores:{
        title:'Vestidores y clósets',
        description:'Soluciones hechas a la medida para organizar y aprovechar mejor cada espacio.',
        images:[
            {src:'images/proyectos/vestidores/vestidor-01.jpg',alt:'Vestidor abierto con repisas, cajones y espacio para colgar ropa',caption:'Distribución abierta con repisas'},
            {src:'images/proyectos/vestidores/vestidor-02.jpg',alt:'Clóset de madera con cajones y compartimentos',caption:'Clóset con espacios de guardado'}
        ]
    },
    sala:{
        title:'Muebles y paneles',
        description:'Muebles para sala y detalles de madera diseñados para integrarse al espacio.',
        images:[
            {src:'images/proyectos/sala/panel-01.jpg',alt:'Panel de listones de madera junto a una barra integrada',caption:'Listones de madera en un área social'},
            {src:'images/proyectos/sala/centro-tv-01.jpg',alt:'Centro de TV a medida con mueble bajo y almacenamiento',caption:'Centro de entretenimiento'},
            {src:'images/proyectos/sala/panel-02.jpg',alt:'Muro decorativo revestido con listones de madera',caption:'Panel de listones decorativos'},
            {src:'images/proyectos/sala/librero-escalera-01.jpg',alt:'Mueble de madera a medida con nichos y almacenamiento integrado',caption:'Almacenamiento a medida con nichos'}
        ]
    },
    barras:{
        title:'Barras y espacios sociales',
        description:'Barras y espacios funcionales para compartir y convivir.',
        images:[
            {src:'images/proyectos/barras/barra-01.jpg',alt:'Barra con frente de listones de madera y bancos altos',caption:'Barra con acabado de listones'},
            {src:'images/proyectos/barras/barra-02.jpg',alt:'Barra de madera con bancos altos y detalles integrados',caption:'Barra integrada al espacio'}
        ]
    }
};

const categoryViewer = document.querySelector('#visor-categoria');
const categoryTitle = document.querySelector('#visor-categoria-titulo');
const categoryDescription = document.querySelector('#visor-categoria-descripcion');
const categoryImageGrid = document.querySelector('#visor-categoria-grid');
const categoryQuoteLink = document.querySelector('#visor-categoria-cotizar');

function openProjectGallery(categoryId){
    const gallery = projectGalleries[categoryId];
    if(!gallery){
        throw new Error(`No existe la galería "${categoryId}".`);
    }

    categoryTitle.textContent = gallery.title;
    categoryDescription.textContent = gallery.description;
    categoryQuoteLink.href = buildQuoteWhatsAppUrl('', gallery.title, 'Vi estos proyectos y me gustaría cotizar uno similar.');
    categoryImageGrid.replaceChildren();

    gallery.images.forEach(function(photo){
        const figure = document.createElement('figure');
        const image = document.createElement('img');
        const caption = document.createElement('figcaption');

        image.src = photo.src;
        image.alt = photo.alt;
        image.decoding = 'async';
        caption.textContent = photo.caption;
        figure.append(image, caption);
        categoryImageGrid.append(figure);
    });

    categoryViewer.showModal();
}

document.querySelectorAll('.categoria-card').forEach(function(button){
    button.addEventListener('click', function(){
        openProjectGallery(button.dataset.categoria);
    });
});

document.querySelector('.visor-categoria-cerrar').addEventListener('click', function(){
    categoryViewer.close();
});

categoryViewer.addEventListener('click', function(event){
    if(event.target === categoryViewer){
        categoryViewer.close();
    }
});

categoryViewer.addEventListener('keydown', function(event){
    if(event.key === 'Escape'){
        categoryViewer.close();
    }
});

const quoteForm = document.querySelector('#cotizacion-form');
const projectDetails = document.querySelector('#detalles-proyecto');

function buildQuoteWhatsAppUrl(name, project, details){
    const message = [
        'Hola, quiero cotizar un proyecto de carpintería.',
        name ? `Nombre: ${name}` : '',
        `Proyecto: ${project}`,
        `Detalles: ${details}`
    ].filter(Boolean).join('\n');

    return `https://wa.me/528126358909?text=${encodeURIComponent(message)}`;
}

projectDetails.addEventListener('input', function(){
    projectDetails.setCustomValidity('');
});

quoteForm.addEventListener('submit', function(event){
    event.preventDefault();
    const formData = new FormData(quoteForm);
    const name = String(formData.get('nombre') || '').trim();
    const project = String(formData.get('proyecto') || '').trim();
    const details = String(formData.get('detalles') || '').trim();

    if(!details){
        projectDetails.setCustomValidity('Escribe brevemente los detalles de tu proyecto.');
        projectDetails.reportValidity();
        return;
    }

    window.location.assign(buildQuoteWhatsAppUrl(name, project, details));
});
</script>

</body>
</html>
