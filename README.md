```html
<!DOCTYPE html>
<html lang="tr">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>AHM Mobilya — Samsun | Modern Living</title>

<meta name="description"
content="AHM Mobilya Samsun — Yaşam alanları için modern mobilya koleksiyonları.">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://images.unsplash.com">

<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700&family=Manrope:wght@300;400;500;600&family=Playfair+Display:wght@400;500;600&display=swap" rel="stylesheet">


<style>

/* =========================================================
   ROOT
========================================================= */

:root{

    --bg:#f4f1eb;
    --paper:#faf8f3;
    --dark:#151412;
    --dark2:#211f1b;

    --text:#171613;
    --muted:#77736b;

    --accent:#9b7650;
    --accent2:#c29b6b;

    --line:rgba(23,22,19,.12);

    --ease:cubic-bezier(.2,.8,.2,1);

}

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{

    background:var(--bg);

    color:var(--text);

    font-family:"DM Sans",sans-serif;

    overflow-x:hidden;

}

body::-webkit-scrollbar{
    width:7px;
}

body::-webkit-scrollbar-track{
    background:var(--bg);
}

body::-webkit-scrollbar-thumb{
    background:#9c846b;
}

img{
    width:100%;
    display:block;
}

a{
    color:inherit;
    text-decoration:none;
}

button,
input,
select{
    font:inherit;
}


/* =========================================================
   PRELOADER
========================================================= */

.loader{

    position:fixed;

    inset:0;

    z-index:99999;

    background:#161512;

    display:flex;

    align-items:center;

    justify-content:center;

    flex-direction:column;

    color:white;

    transition:1s ease;

}

.loader.hide{

    opacity:0;

    visibility:hidden;

}

.loader-logo{

    font-family:"Playfair Display",serif;

    font-size:42px;

    letter-spacing:8px;

}

.loader-sub{

    margin-top:10px;

    font-size:8px;

    letter-spacing:5px;

    color:#aaa;

}

.loader-line{

    width:180px;

    height:1px;

    background:#333;

    margin-top:35px;

    overflow:hidden;

}

.loader-line span{

    display:block;

    width:100%;

    height:100%;

    background:#c29b6b;

    transform:translateX(-100%);

    animation:load 1.5s forwards;

}

@keyframes load{

    to{
        transform:translateX(0);
    }

}


/* =========================================================
   CURSOR
========================================================= */

.cursor{

    position:fixed;

    width:8px;

    height:8px;

    border-radius:50%;

    background:var(--accent);

    pointer-events:none;

    z-index:9998;

    transform:translate(-50%,-50%);

}

.cursor-ring{

    position:fixed;

    width:40px;

    height:40px;

    border:1px solid rgba(155,118,80,.45);

    border-radius:50%;

    pointer-events:none;

    z-index:9997;

    transform:translate(-50%,-50%);

    transition:.2s;

}

@media(max-width:800px){

    .cursor,
    .cursor-ring{
        display:none;
    }

}


/* =========================================================
   TOP BAR
========================================================= */

.topbar{

    background:#171613;

    color:#ddd;

    height:35px;

    display:flex;

    align-items:center;

    justify-content:center;

    font-size:9px;

    letter-spacing:2px;

    text-transform:uppercase;

}

.topbar span{

    color:#cba676;

}


/* =========================================================
   NAV
========================================================= */

.nav{

    position:fixed;

    top:35px;

    left:0;

    width:100%;

    z-index:1000;

    transition:.45s var(--ease);

}

.nav.scrolled{

    top:0;

    background:rgba(250,248,243,.92);

    backdrop-filter:blur(18px);

    border-bottom:1px solid var(--line);

}

.nav-inner{

    width:min(1380px,94%);

    margin:auto;

    height:82px;

    display:flex;

    align-items:center;

    justify-content:space-between;

}

.logo{

    display:flex;

    align-items:center;

    gap:13px;

}

.logo-symbol{

    width:42px;

    height:42px;

    border:1px solid var(--text);

    display:flex;

    align-items:center;

    justify-content:center;

    font-family:"Playfair Display",serif;

    font-size:18px;

}

.logo-text{

    display:flex;

    flex-direction:column;

}

.logo-text strong{

    font-family:"Playfair Display",serif;

    font-size:20px;

    letter-spacing:3px;

}

.logo-text span{

    font-size:7px;

    letter-spacing:4px;

    color:#8b7054;

    margin-top:5px;

}

.nav-links{

    display:flex;

    gap:32px;

}

.nav-links a{

    font-size:9px;

    letter-spacing:1.8px;

    text-transform:uppercase;

    color:#5e5a53;

    transition:.3s;

}

.nav-links a:hover{

    color:#9b7650;

}

.nav-cta{

    border:1px solid #76634f;

    padding:12px 20px;

    font-size:9px;

    letter-spacing:2px;

    text-transform:uppercase;

    transition:.3s;

}

.nav-cta:hover{

    background:#171613;

    color:white;

}

.menu{

    display:none;

    font-size:25px;

}


/* =========================================================
   HERO
========================================================= */

.hero{

    min-height:100vh;

    padding-top:117px;

    display:grid;

    grid-template-columns:44% 56%;

    position:relative;

}

.hero-copy{

    display:flex;

    flex-direction:column;

    justify-content:center;

    padding:80px 7vw 80px 8vw;

    position:relative;

    z-index:2;

}

.hero-kicker{

    display:flex;

    align-items:center;

    gap:13px;

    font-size:9px;

    letter-spacing:4px;

    text-transform:uppercase;

    color:#8e6e4e;

    margin-bottom:30px;

}

.hero-kicker:before{

    content:"";

    width:45px;

    height:1px;

    background:#9b7650;

}

.hero h1{

    font-family:"Playfair Display",serif;

    font-size:clamp(60px,7vw,110px);

    font-weight:400;

    line-height:.88;

    letter-spacing:-4px;

}

.hero h1 em{

    display:block;

    font-style:italic;

    color:#9b7650;

}

.hero-description{

    max-width:440px;

    color:#706c65;

    font-size:14px;

    line-height:1.9;

    margin:35px 0;

}

.hero-actions{

    display:flex;

    gap:12px;

}

.btn{

    min-height:53px;

    padding:0 25px;

    display:inline-flex;

    align-items:center;

    justify-content:center;

    gap:10px;

    font-size:9px;

    letter-spacing:2px;

    text-transform:uppercase;

    transition:.4s var(--ease);

}

.btn-dark{

    background:#171613;

    color:white;

}

.btn-dark:hover{

    transform:translateY(-4px);

    background:#302c26;

}

.btn-light{

    border:1px solid var(--line);

}

.btn-light:hover{

    border-color:#9b7650;

    color:#9b7650;

}

.hero-image{

    position:relative;

    overflow:hidden;

}

.hero-image img{

    height:100%;

    object-fit:cover;

    animation:heroZoom 12s ease-out forwards;

}

@keyframes heroZoom{

    from{
        transform:scale(1.08);
    }

    to{
        transform:scale(1);
    }

}

.hero-image:after{

    content:"";

    position:absolute;

    inset:0;

    background:
        linear-gradient(
            90deg,
            rgba(0,0,0,.12),
            transparent 35%
        );

}

.hero-label{

    position:absolute;

    z-index:4;

    right:35px;

    bottom:35px;

    color:white;

    border:1px solid rgba(255,255,255,.4);

    backdrop-filter:blur(10px);

    padding:15px 20px;

    font-size:8px;

    letter-spacing:3px;

    text-transform:uppercase;

}


/* =========================================================
   TRUST
========================================================= */

.trust{

    background:#1a1916;

    color:white;

}

.trust-grid{

    width:min(1200px,92%);

    margin:auto;

    display:grid;

    grid-template-columns:repeat(4,1fr);

}

.trust-item{

    padding:30px;

    border-right:1px solid rgba(255,255,255,.1);

}

.trust-item:last-child{

    border:0;

}

.trust-number{

    font-family:"Playfair Display",serif;

    font-size:31px;

    color:#c29b6b;

}

.trust-item p{

    color:#aaa59c;

    font-size:9px;

    letter-spacing:1px;

    margin-top:5px;

}


/* =========================================================
   GENERAL
========================================================= */

.container{

    width:min(1200px,92%);

    margin:auto;

}

section{

    padding:130px 0;

}

.kicker{

    color:#94704e;

    font-size:9px;

    letter-spacing:4px;

    text-transform:uppercase;

    margin-bottom:16px;

}

.title{

    font-family:"Playfair Display",serif;

    font-size:clamp(44px,5vw,70px);

    line-height:.98;

    font-weight:400;

}

.title em{

    color:#9b7650;

    font-style:italic;

}

.muted{

    color:#77736b;

    font-size:13px;

    line-height:1.9;

}


/* =========================================================
   COLLECTIONS
========================================================= */

.collections{

    background:var(--paper);

}

.collection-head{

    display:flex;

    justify-content:space-between;

    align-items:end;

    margin-bottom:55px;

}

.collection-head .muted{

    max-width:390px;

}

.collection-grid{

    display:grid;

    grid-template-columns:1.25fr .75fr .75fr;

    grid-template-rows:300px 300px;

    gap:12px;

}

.collection{

    position:relative;

    overflow:hidden;

    cursor:pointer;

}

.collection:first-child{

    grid-row:span 2;

}

.collection img{

    width:100%;

    height:100%;

    object-fit:cover;

    transition:1s var(--ease);

}

.collection:hover img{

    transform:scale(1.07);

}

.collection-overlay{

    position:absolute;

    inset:0;

    background:
        linear-gradient(
            transparent 45%,
            rgba(0,0,0,.8)
        );

}

.collection-content{

    position:absolute;

    z-index:3;

    left:25px;

    bottom:25px;

    color:white;

}

.collection-content span{

    font-size:8px;

    letter-spacing:3px;

    text-transform:uppercase;

    opacity:.7;

}

.collection-content h3{

    font-family:"Playfair Display",serif;

    font-size:27px;

    font-weight:400;

    margin-top:6px;

}

.collection-arrow{

    position:absolute;

    right:20px;

    bottom:22px;

    width:42px;

    height:42px;

    border:1px solid rgba(255,255,255,.4);

    border-radius:50%;

    display:flex;

    align-items:center;

    justify-content:center;

    color:white;

}


/* =========================================================
   SHOWCASE
========================================================= */

.showcase{

    background:#e9e4dc;

}

.showcase-grid{

    display:grid;

    grid-template-columns:.75fr 1.25fr;

    gap:90px;

    align-items:center;

}

.showcase-copy{

    padding-left:20px;

}

.showcase-copy .title{

    margin-bottom:30px;

}

.showcase-image{

    height:650px;

    position:relative;

}

.showcase-image img{

    width:100%;

    height:100%;

    object-fit:cover;

}

.showcase-tag{

    position:absolute;

    left:-25px;

    bottom:30px;

    background:#171613;

    color:white;

    padding:25px 30px;

}

.showcase-tag strong{

    font-family:"Playfair Display",serif;

    font-size:30px;

    color:#d0ab78;

}

.showcase-tag span{

    display:block;

    font-size:8px;

    letter-spacing:2px;

    margin-top:5px;

    color:#aaa;

}


/* =========================================================
   PRODUCTS
========================================================= */

.products{

    background:#f8f6f1;

}

.product-header{

    display:flex;

    justify-content:space-between;

    align-items:end;

    margin-bottom:55px;

}

.filters{

    display:flex;

    gap:8px;

    flex-wrap:wrap;

}

.filter{

    border:1px solid var(--line);

    background:transparent;

    padding:10px 15px;

    font-size:8px;

    letter-spacing:1.5px;

    text-transform:uppercase;

    cursor:pointer;

    transition:.3s;

}

.filter.active,
.filter:hover{

    background:#171613;

    color:white;

    border-color:#171613;

}

.product-grid{

    display:grid;

    grid-template-columns:repeat(4,1fr);

    gap:15px;

}

.product{

    background:white;

    position:relative;

    overflow:hidden;

    transition:.4s var(--ease);

}

.product:hover{

    transform:translateY(-7px);

    box-shadow:0 25px 60px rgba(0,0,0,.09);

}

.product-image{

    height:350px;

    position:relative;

    overflow:hidden;

}

.product-image img{

    height:100%;

    object-fit:cover;

    transition:.7s var(--ease);

}

.product:hover .product-image img{

    transform:scale(1.05);

}

.product-badge{

    position:absolute;

    left:14px;

    top:14px;

    background:#171613;

    color:white;

    padding:7px 10px;

    font-size:7px;

    letter-spacing:1.5px;

}

.product-info{

    padding:20px;

}

.product-category{

    color:#a27e59;

    font-size:7px;

    letter-spacing:2px;

    text-transform:uppercase;

}

.product-name{

    font-family:"Playfair Display",serif;

    font-size:19px;

    margin-top:7px;

}

.product-bottom{

    margin-top:18px;

    display:flex;

    align-items:center;

    justify-content:space-between;

}

.product-price{

    font-size:13px;

}

.product-btn{

    width:36px;

    height:36px;

    border:1px solid var(--line);

    display:flex;

    align-items:center;

    justify-content:center;

    font-size:12px;

}


/* =========================================================
   FULL WIDTH CAMPAIGN
========================================================= */

.campaign{

    min-height:680px;

    position:relative;

    display:flex;

    align-items:center;

    overflow:hidden;

}

.campaign-bg{

    position:absolute;

    inset:0;

    background:
        linear-gradient(
            90deg,
            rgba(15,14,12,.97),
            rgba(15,14,12,.6),
            rgba(15,14,12,.2)
        ),
        url("https://images.unsplash.com/photo-1618220179428-22790b461013?auto=format&fit=crop&w=2200&q=95")
        center/cover;

}

.campaign-content{

    position:relative;

    z-index:3;

    color:white;

    max-width:650px;

}

.campaign-content .kicker{

    color:#d0ab78;

}

.campaign-content h2{

    font-family:"Playfair Display",serif;

    font-size:clamp(55px,7vw,100px);

    font-weight:400;

    line-height:.88;

}

.campaign-content h2 em{

    color:#d0ab78;

}

.campaign-content p{

    max-width:450px;

    color:#aaa59d;

    font-size:13px;

    line-height:1.9;

    margin:30px 0;

}

.campaign-note{

    display:flex;

    align-items:center;

    gap:15px;

    color:#aaa;

    font-size:8px;

    letter-spacing:2px;

    text-transform:uppercase;

}

.campaign-note:before{

    content:"";

    width:35px;

    height:1px;

    background:#c29b6b;

}


/* =========================================================
   BENEFITS
========================================================= */

.benefits{

    background:#171613;

    color:white;

}

.benefits-grid{

    display:grid;

    grid-template-columns:repeat(4,1fr);

}

.benefit{

    padding:35px;

    border-right:1px solid rgba(255,255,255,.1);

}

.benefit:last-child{

    border:0;

}

.benefit-icon{

    font-size:25px;

    color:#c29b6b;

    margin-bottom:25px;

}

.benefit h3{

    font-family:"Playfair Display",serif;

    font-size:22px;

    font-weight:400;

}

.benefit p{

    color:#8e8981;

    font-size:10px;

    line-height:1.8;

    margin-top:10px;

}


/* =========================================================
   INSTAGRAM
========================================================= */

.instagram{

    background:var(--paper);

}

.instagram-head{

    display:flex;

    justify-content:space-between;

    align-items:end;

    margin-bottom:45px;

}

.instagram-link{

    border-bottom:1px solid #9b7650;

    padding-bottom:6px;

    font-size:9px;

    letter-spacing:2px;

    text-transform:uppercase;

}

.instagram-grid{

    display:grid;

    grid-template-columns:repeat(5,1fr);

    gap:7px;

}

.instagram-item{

    aspect-ratio:1;

    overflow:hidden;

}

.instagram-item img{

    width:100%;

    height:100%;

    object-fit:cover;

    transition:.6s var(--ease);

}

.instagram-item:hover img{

    transform:scale(1.08);

}


/* =========================================================
   TESTIMONIAL
========================================================= */

.testimonials{

    background:#e7e1d8;

}

.testimonial-grid{

    display:grid;

    grid-template-columns:.8fr 1.2fr;

    gap:100px;

    align-items:center;

}

.testimonial-rating{

    font-family:"Playfair Display",serif;

    font-size:70px;

}

.stars{

    color:#a47d55;

    letter-spacing:4px;

    font-size:14px;

}

.review{

    border-top:1px solid rgba(0,0,0,.15);

    padding-top:30px;

}

.review-quote{

    font-family:"Playfair Display",serif;

    font-size:32px;

    color:#9b7650;

}

.review p{

    font-family:"Playfair Display",serif;

    font-size:24px;

    line-height:1.5;

    max-width:700px;

    margin:10px 0 25px;

}

.review-author{

    font-size:9px;

    letter-spacing:2px;

    text-transform:uppercase;

}


/* =========================================================
   APPOINTMENT / CONTACT
========================================================= */

.contact{

    background:#f7f4ee;

}

.contact-grid{

    display:grid;

    grid-template-columns:.75fr 1.25fr;

    gap:100px;

    align-items:start;

}

.contact-copy h2{

    font-family:"Playfair Display",serif;

    font-size:70px;

    line-height:.9;

    font-weight:400;

}

.contact-copy h2 em{

    color:#9b7650;

}

.contact-copy p{

    color:#777;

    max-width:400px;

    line-height:1.9;

    font-size:13px;

    margin:30px 0;

}

.contact-info{

    margin-top:40px;

}

.contact-info div{

    padding:15px 0;

    border-bottom:1px solid var(--line);

    font-size:11px;

}

.contact-info span{

    display:block;

    color:#777;

    font-size:8px;

    letter-spacing:2px;

    text-transform:uppercase;

    margin-bottom:5px;

}

.form{

    display:grid;

    grid-template-columns:1fr 1fr;

    gap:12px;

}

.input{

    background:white;

    border:1px solid var(--line);

    padding:17px;

    outline:none;

    color:#222;

}

.input:focus{

    border-color:#9b7650;

}

.form .full{

    grid-column:1/-1;

}

.form button{

    border:0;

    cursor:pointer;

}


/* =========================================================
   FOOTER
========================================================= */

footer{

    background:#11100e;

    color:white;

    padding:55px 0 30px;

}

.footer-top{

    display:flex;

    justify-content:space-between;

    align-items:start;

    padding-bottom:45px;

    border-bottom:1px solid rgba(255,255,255,.1);

}

.footer-logo{

    font-family:"Playfair Display",serif;

    font-size:32px;

    letter-spacing:4px;

}

.footer-logo span{

    display:block;

    font-family:"DM Sans",sans-serif;

    font-size:7px;

    color:#8c7b67;

    letter-spacing:4px;

    margin-top:8px;

}

.footer-links{

    display:flex;

    gap:45px;

}

.footer-links a{

    color:#8d8981;

    font-size:9px;

    letter-spacing:1.5px;

    text-transform:uppercase;

}

.footer-links a:hover{

    color:#d0ab78;

}

.footer-bottom{

    padding-top:25px;

    display:flex;

    justify-content:space-between;

    color:#55514c;

    font-size:8px;

}


/* =========================================================
   FLOATING WHATSAPP
========================================================= */

.whatsapp{

    position:fixed;

    z-index:500;

    right:24px;

    bottom:24px;

    width:58px;

    height:58px;

    border-radius:50%;

    background:#171613;

    color:#d0ab78;

    display:flex;

    align-items:center;

    justify-content:center;

    font-size:20px;

    box-shadow:0 15px 40px rgba(0,0,0,.18);

    transition:.35s;

}

.whatsapp:hover{

    transform:scale(1.1);

    background:#c29b6b;

    color:#171613;

}


/* =========================================================
   REVEAL
========================================================= */

.reveal{

    opacity:0;

    transform:translateY(35px);

    transition:1s var(--ease);

}

.reveal.show{

    opacity:1;

    transform:none;

}


/* =========================================================
   MOBILE
========================================================= */

@media(max-width:1000px){

    .nav-links,
    .nav-cta{

        display:none;

    }

    .menu{

        display:block;

    }

    .hero{

        grid-template-columns:1fr;

    }

    .hero-copy{

        min-height:620px;

        padding:110px 7% 70px;

    }

    .hero-image{

        height:550px;

    }

    .trust-grid{

        grid-template-columns:1fr 1fr;

    }

    .collection-grid{

        grid-template-columns:1fr 1fr;

        grid-template-rows:350px 250px 250px;

    }

    .collection:first-child{

        grid-column:span 2;

        grid-row:auto;

    }

    .showcase-grid,
    .testimonial-grid,
    .contact-grid{

        grid-template-columns:1fr;

        gap:60px;

    }

    .product-grid{

        grid-template-columns:1fr 1fr;

    }

    .benefits-grid{

        grid-template-columns:1fr 1fr;

    }

}

@media(max-width:650px){

    section{

        padding:90px 0;

    }

    .topbar{

        font-size:7px;

    }

    .hero-copy{

        min-height:650px;

    }

    .hero h1{

        font-size:67px;

        letter-spacing:-2px;

    }

    .hero-description{

        font-size:12px;

    }

    .hero-actions{

        flex-direction:column;

    }

    .btn{

        width:100%;

    }

    .hero-image{

        height:450px;

    }

    .hero-label{

        right:15px;

        bottom:15px;

    }

    .trust-grid{

        grid-template-columns:1fr;

    }

    .trust-item{

        border-right:0;

        border-bottom:1px solid rgba(255,255,255,.1);

    }

    .collection-head,
    .product-header,
    .instagram-head{

        display:block;

    }

    .collection-head .muted{

        margin-top:25px;

    }

    .filters{

        margin-top:25px;

    }

    .collection-grid{

        grid-template-columns:1fr;

        grid-template-rows:350px 240px 240px 240px;

    }

    .collection:first-child{

        grid-column:auto;

    }

    .product-grid{

        grid-template-columns:1fr;

    }

    .product-image{

        height:400px;

    }

    .showcase-image{

        height:450px;

    }

    .campaign{

        min-height:650px;

    }

    .benefits-grid{

        grid-template-columns:1fr;

    }

    .benefit{

        border-right:0;

        border-bottom:1px solid rgba(255,255,255,.1);

    }

    .instagram-grid{

        grid-template-columns:1fr 1fr;

    }

    .instagram-item:last-child{

        display:none;

    }

    .review p{

        font-size:19px;

    }

    .contact-copy h2{

        font-size:60px;

    }

    .form{

        grid-template-columns:1fr;

    }

    .form .full{

        grid-column:auto;

    }

    .footer-top,
    .footer-bottom{

        flex-direction:column;

        gap:25px;

    }

    .footer-links{

        flex-wrap:wrap;

        gap:20px;

    }

}

</style>

</head>


<body>


<!-- =========================================================
     LOADER
========================================================= -->

<div class="loader" id="loader">

    <div class="loader-logo">
        AHM
    </div>

    <div class="loader-sub">
        MOBİLYA · SAMSUN
    </div>

    <div class="loader-line">
        <span></span>
    </div>

</div>


<div class="cursor" id="cursor"></div>
<div class="cursor-ring" id="cursorRing"></div>


<!-- =========================================================
     TOPBAR
========================================================= -->

<div class="topbar">

    <span>Ücretsiz Gönderim & Kurulum</span>
    &nbsp; · &nbsp;
    Samsun & Bölge Teslimat

</div>


<!-- =========================================================
     NAV
========================================================= -->

<header class="nav" id="nav">

<div class="nav-inner">

<a href="#" class="logo">

<div class="logo-symbol">
A
</div>

<div class="logo-text">

<strong>AHM</strong>

<span>MOBİLYA</span>

</div>

</a>


<nav class="nav-links">

<a href="#koleksiyonlar">
Koleksiyonlar
</a>

<a href="#urunler">
Ürünler
</a>

<a href="#hikaye">
AHM
</a>

<a href="#instagram">
Instagram
</a>

<a href="#iletisim">
İletişim
</a>

</nav>


<a href="#iletisim" class="nav-cta">
Showroom'a Gel
</a>


<div class="menu">
☰
</div>

</div>

</header>


<!-- =========================================================
     HERO
========================================================= -->

<section class="hero">


<div class="hero-copy reveal">

<div class="hero-kicker">
MODERN LIVING · SAMSUN
</div>


<h1>

Yaşam
<span>alanınız.</span>

</h1>


<p class="hero-description">

Evinizin karakterini tamamlayan
mobilyaları keşfedin. Modern tasarım,
güçlü detaylar ve yaşamınıza göre
şekillenen koleksiyonlar.

</p>


<div class="hero-actions">

<a href="#koleksiyonlar"
class="btn btn-dark">

Koleksiyonları Keşfet →

</a>

<a href="#urunler"
class="btn btn-light">

Ürünlere Göz At

</a>

</div>

</div>


<div class="hero-image">

<img
src="https://images.unsplash.com/photo-1616486338812-3dadae4b4ace?auto=format&fit=crop&w=2200&q=95"
alt="Modern AHM Mobilya yaşam alanı">

<div class="hero-label">

AHM · NEW SEASON

</div>

</div>


</section>


<!-- =========================================================
     TRUST
========================================================= -->

<section class="trust" style="padding:0;">

<div class="trust-grid">

<div class="trust-item">

<div class="trust-number">
2 Yıl
</div>

<p>
Garanti
</p>

</div>


<div class="trust-item">

<div class="trust-number">
Tüm Türkiye
</div>

<p>
Gönderim & Kurulum
</p>

</div>


<div class="trust-item">

<div class="trust-number">
Güvenli
</div>

<p>
Ödeme
</p>

</div>


<div class="trust-item">

<div class="trust-number">
AHM
</div>

<p>
Samsun Showroom
</p>

</div>

</div>

</section>


<!-- =========================================================
     COLLECTIONS
========================================================= -->

<section class="collections" id="koleksiyonlar">

<div class="container">


<div class="collection-head reveal">

<div>

<div class="kicker">
Koleksiyonlar
</div>

<h2 class="title">
Eviniz için <em>seçtik.</em>
</h2>

</div>

<p class="muted">

Bir evin tüm hikâyesini tamamlayan
koleksiyonları tek bir yerde keşfedin.

</p>

</div>


<div class="collection-grid">


<div class="collection reveal">

<img
src="https://images.unsplash.com/photo-1555041469-a586c61ea9bc?auto=format&fit=crop&w=1400&q=95"
alt="Koltuk takımları">

<div class="collection-overlay"></div>

<div class="collection-content">

<span>
01 · LIVING
</span>

<h3>
Koltuk Takımları
</h3>

</div>

<div class="collection-arrow">
↗
</div>

</div>


<div class="collection reveal">

<img
src="https://images.unsplash.com/photo-1616627561950-9f746e330187?auto=format&fit=crop&w=1000&q=95"
alt="Yatak odası">

<div class="collection-overlay"></div>

<div class="collection-content">

<span>
02 · BEDROOM
</span>

<h3>
Yatak Odaları
</h3>

</div>

<div class="collection-arrow">
↗
</div>

</div>


<div class="collection reveal">

<img
src="https://images.unsplash.com/photo-1618220179428-22790b461013?auto=format&fit=crop&w=1000&q=95"
alt="Yemek odası">

<div class="collection-overlay"></div>

<div class="collection-content">

<span>
03 · DINING
</span>

<h3>
Yemek Odaları
</h3>

</div>

<div class="collection-arrow">
↗
</div>

</div>


<div class="collection reveal">

<img
src="https://images.unsplash.com/photo-1616486338812-3dadae4b4ace?auto=format&fit=crop&w=1000&q=95"
alt="TV ünitesi">

<div class="collection-overlay"></div>

<div class="collection-content">

<span>
04 · LIVING
</span>

<h3>
TV Üniteleri
</h3>

</div>

<div class="collection-arrow">
↗
</div>

</div>


<div class="collection reveal">

<img
src="https://images.unsplash.com/photo-1600210492486-724fe5c67fb0?auto=format&fit=crop&w=1000&q=95"
alt="Köşe takımları">

<div class="collection-overlay"></div>

<div class="collection-content">

<span>
05 · COLLECTION
</span>

<h3>
Köşe Takımları
</h3>

</div>

<div class="collection-arrow">
↗
</div>

</div>


</div>

</div>

</section>


<!-- =========================================================
     SHOWCASE
========================================================= -->

<section class="showcase" id="hikaye">

<div class="container showcase-grid">


<div class="showcase-copy reveal">

<div class="kicker">
AHM MOBİLYA
</div>

<h2 class="title">

Evinizi
<em>yeniden</em>
hayal edin.

</h2>

<p class="muted">

Mobilya yalnızca bir eşya değildir.
Yaşadığınız alanın atmosferini,
konforunu ve karakterini belirler.

AHM koleksiyonlarını bu anlayışla
seçiyor ve yaşam alanlarınıza
uyum sağlayacak seçenekleri
bir araya getiriyoruz.

</p>

<br>

<a href="#urunler" class="btn btn-dark">

Koleksiyonu Gör →

</a>

</div>


<div class="showcase-image reveal">

<img
src="https://images.unsplash.com/photo-1600607687920-4e2a09cf159d?auto=format&fit=crop&w=1600&q=95"
alt="AHM premium showroom">

<div class="showcase-tag">

<strong>AHM</strong>

<span>
DESIGN FOR LIVING
</span>

</div>

</div>


</div>

</section>


<!-- =========================================================
     PRODUCTS
========================================================= -->

<section class="products" id="urunler">

<div class="container">


<div class="product-header reveal">

<div>

<div class="kicker">
Seçili Ürünler
</div>

<h2 class="title">
Sezonun <em>favorileri.</em>
</h2>

</div>


<div class="filters">

<button class="filter active"
data-filter="all">
Tümü
</button>

<button class="filter"
data-filter="living">
Koltuk
</button>

<button class="filter"
data-filter="bedroom">
Yatak Odası
</button>

<button class="filter"
data-filter="dining">
Yemek Odası
</button>

</div>

</div>


<div class="product-grid">


<article class="product reveal"
data-category="living">

<div class="product-image">

<div class="product-badge">
ÖNE ÇIKAN
</div>

<img
src="https://images.unsplash.com/photo-1555041469-a586c61ea9bc?auto=format&fit=crop&w=1000&q=90"
alt="Premium koltuk">

</div>

<div class="product-info">

<div class="product-category">
Koltuk Takımı
</div>

<div class="product-name">
Modern Living
</div>

<div class="product-bottom">

<div class="product-price">
Fiyat için iletişime geç
</div>

<a
href="https://wa.me/903622669796"
class="product-btn"
target="_blank">

↗

</a>

</div>

</div>

</article>


<article class="product reveal"
data-category="bedroom">

<div class="product-image">

<div class="product-badge">
YENİ
</div>

<img
src="https://images.unsplash.com/photo-1616627561950-9f746e330187?auto=format&fit=crop&w=1000&q=90"
alt="Yatak odası">

</div>

<div class="product-info">

<div class="product-category">
Yatak Odası
</div>

<div class="product-name">
Signature Bedroom
</div>

<div class="product-bottom">

<div class="product-price">
Fiyat için iletişime geç
</div>

<a
href="https://wa.me/903622669796"
class="product-btn"
target="_blank">

↗

</a>

</div>

</div>

</article>


<article class="product reveal"
data-category="dining">

<div class="product-image">

<img
src="https://images.unsplash.com/photo-1618220179428-22790b461013?auto=format&fit=crop&w=1000&q=90"
alt="Yemek odası">

</div>

<div class="product-info">

<div class="product-category">
Yemek Odası
</div>

<div class="product-name">
Atelier Dining
</div>

<div class="product-bottom">

<div class="product-price">
Fiyat için iletişime geç
</div>

<a
href="https://wa.me/903622669796"
class="product-btn"
target="_blank">

↗

</a>

</div>

</div>

</article>


<article class="product reveal"
data-category="living">

<div class="product-image">

<img
src="https://images.unsplash.com/photo-1616486338812-3dadae4b4ace?auto=format&fit=crop&w=1000&q=90"
alt="TV ünitesi">

</div>

<div class="product-info">

<div class="product-category">
TV Ünitesi
</div>

<div class="product-name">
Minimal TV
</div>

<div class="product-bottom">

<div class="product-price">
Fiyat için iletişime geç
</div>

<a
href="https://wa.me/903622669796"
class="product-btn"
target="_blank">

↗

</a>

</div>

</div>

</article>


</div>

</div>

</section>


<!-- =========================================================
     CAMPAIGN
========================================================= -->

<section class="campaign">

<div class="campaign-bg"></div>

<div class="container">

<div class="campaign-content reveal">

<div class="kicker">
AHM SEASON
</div>

<h2>

Yeni bir ev.<br>
Yeni bir <em>hikâye.</em>

</h2>

<p>

Yaşam alanınızı baştan tasarlamak
istiyorsanız showroom koleksiyonlarımızı
yakından keşfedin.

</p>

<div class="campaign-note">

Showroom · Samsun

</div>

<br>

<a href="#iletisim"
class="btn btn-light"
style="color:white;border-color:rgba(255,255,255,.4);">

Showroom'a Gel →

</a>

</div>

</div>

</section>


<!-- =========================================================
     BENEFITS
========================================================= -->

<section class="benefits" style="padding:0;">

<div class="container" style="width:100%;">

<div class="benefits-grid">


<div class="benefit reveal">

<div class="benefit-icon">
◇
</div>

<h3>
2 Yıl Garanti
</h3>

<p>
Ürünlerde güven veren garanti
ve satış sonrası destek.
</p>

</div>


<div class="benefit reveal">

<div class="benefit-icon">
↗
</div>

<h3>
Gönderim & Kurulum
</h3>

<p>
Belirli bölgelerde ücretsiz
gönderim ve kurulum seçenekleri.
</p>

</div>


<div class="benefit reveal">

<div class="benefit-icon">
₺
</div>

<h3>
Esnek Ödeme
</h3>

<p>
İhtiyacınıza göre farklı
ödeme seçenekleri.
</p>

</div>


<div class="benefit reveal">

<div class="benefit-icon">
✦
</div>

<h3>
Showroom Deneyimi
</h3>

<p>
Ürünleri yakından görün,
dokunun ve yaşam alanınızı planlayın.
</p>

</div>


</div>

</div>

</section>


<!-- =========================================================
     INSTAGRAM
========================================================= -->

<section class="instagram" id="instagram">

<div class="container">


<div class="instagram-head reveal">

<div>

<div class="kicker">
Sosyal
</div>

<h2 class="title">
AHM <em>Instagram.</em>
</h2>

</div>


<a
href="https://www.instagram.com/ahmmobilyasamsun/"
target="_blank"
class="instagram-link">

@ahmmobilyasamsun →

</a>

</div>


<div class="instagram-grid">


<div class="instagram-item reveal">

<img
src="https://images.unsplash.com/photo-1555041469-a586c61ea9bc?auto=format&fit=crop&w=700&q=90">

</div>


<div class="instagram-item reveal">

<img
src="https://images.unsplash.com/photo-1600607687920-4e2a09cf159d?auto=format&fit=crop&w=700&q=90">

</div>


<div class="instagram-item reveal">

<img
src="https://images.unsplash.com/photo-1618220179428-22790b461013?auto=format&fit=crop&w=700&q=90">

</div>


<div class="instagram-item reveal">

<img
src="https://images.unsplash.com/photo-1616486338812-3dadae4b4ace?auto=format&fit=crop&w=700&q=90">

</div>


<div class="instagram-item reveal">

<img
src="https://images.unsplash.com/photo-1616627561950-9f746e330187?auto=format&fit=crop&w=700&q=90">

</div>


</div>

</div>

</section>


<!-- =========================================================
     TESTIMONIAL
========================================================= -->

<section class="testimonials">

<div class="container testimonial-grid">


<div class="reveal">

<div class="kicker">
Müşteri Deneyimi
</div>

<div class="testimonial-rating">
4.4
</div>

<div class="stars">
★★★★★
</div>

<p class="muted" style="margin-top:10px;">
Showroom deneyiminizi daha güçlü
bir sosyal kanıt alanıyla destekleyin.
</p>

</div>


<div class="review reveal">

<div class="review-quote">
“ 
</div>

<p>
“Evinizin havasını değiştiren
detaylar bazen tek bir mobilyayla
başlar.”
</p>

<div class="review-author">
AHM MOBİLYA · SAMSUN
</div>

</div>


</div>

</section>


<!-- =========================================================
     CONTACT
========================================================= -->

<section class="contact" id="iletisim">

<div class="container contact-grid">


<div class="contact-copy reveal">

<div class="kicker">
Showroom
</div>

<h2>

Gelip
<em>görün.</em>

</h2>

<p>

Beğendiğiniz ürünleri yakından görmek,
ölçü ve seçenekler hakkında bilgi almak
için showroomumuzu ziyaret edin.

</p>


<div class="contact-info">

<div>

<span>
Adres
</span>

Şabanoğlu Mahallesi
Karadeniz Bulvarı No:14
Tekkeköy / Samsun

</div>


<div>

<span>
Telefon
</span>

<a href="tel:+903622669796">
0362 266 97 96
</a>

</div>


<div>

<span>
WhatsApp
</span>

<a href="https://wa.me/903622669796"
target="_blank">

WhatsApp'tan Yaz

</a>

</div>

</div>

</div>


<form class="form reveal"
id="contactForm">


<input
class="input"
id="cname"
placeholder="Ad Soyad"
required>


<input
class="input"
id="cphone"
placeholder="Telefon"
required>


<select
class="input full"
id="cservice">

<option>
Ne hakkında bilgi almak istiyorsunuz?
</option>

<option>
Koltuk Takımları
</option>

<option>
Yatak Odaları
</option>

<option>
Yemek Odaları
</option>

<option>
TV Üniteleri
</option>

<option>
Köşe Takımları
</option>

<option>
Diğer
</option>

</select>


<textarea
class="input full"
id="cmessage"
rows="6"
placeholder="Mesajınız">
</textarea>


<button
class="btn btn-dark"
type="submit">

WhatsApp'tan Bilgi Al →

</button>


</form>

</div>

</section>


<!-- =========================================================
     FOOTER
========================================================= -->

<footer>

<div class="container">

<div class="footer-top">

<div class="footer-logo">

AHM

<span>
MOBİLYA · SAMSUN
</span>

</div>


<div class="footer-links">

<a href="#koleksiyonlar">
Koleksiyonlar
</a>

<a href="#urunler">
Ürünler
</a>

<a href="#instagram">
Instagram
</a>

<a href="#iletisim">
İletişim
</a>

</div>

</div>


<div class="footer-bottom">

<div>
© 2026 AHM MOBİLYA
</div>

<div>
@ahmmobilyasamsun
</div>

</div>

</div>

</footer>


<!-- =========================================================
     WHATSAPP
========================================================= -->

<a
href="https://wa.me/903622669796"
target="_blank"
class="whatsapp">

◉

</a>


<script>

/* =========================================================
   LOADER
========================================================= */

window.addEventListener("load",()=>{

setTimeout(()=>{

document
.getElementById("loader")
.classList.add("hide");

},900);

});


/* =========================================================
   NAV
========================================================= */

const nav=
document.getElementById("nav");

window.addEventListener("scroll",()=>{

if(window.scrollY>70){

nav.classList.add("scrolled");

}else{

nav.classList.remove("scrolled");

}

});


/* =========================================================
   CURSOR
========================================================= */

const cursor=
document.getElementById("cursor");

const ring=
document.getElementById("cursorRing");

document.addEventListener("mousemove",(e)=>{

cursor.style.left=e.clientX+"px";
cursor.style.top=e.clientY+"px";

ring.style.left=e.clientX+"px";
ring.style.top=e.clientY+"px";

});


document
.querySelectorAll("a,button,.collection,.product")
.forEach(el=>{

el.addEventListener("mouseenter",()=>{

ring.style.width="65px";
ring.style.height="65px";

});

el.addEventListener("mouseleave",()=>{

ring.style.width="40px";
ring.style.height="40px";

});

});


/* =========================================================
   REVEAL
========================================================= */

const observer=
new IntersectionObserver(

entries=>{

entries.forEach(entry=>{

if(entry.isIntersecting){

entry.target.classList.add("show");

observer.unobserve(entry.target);

}

});

},
{
threshold:.12
}

);


document
.querySelectorAll(".reveal")
.forEach(el=>{

observer.observe(el);

});


/* =========================================================
   PRODUCT FILTER
========================================================= */

const filters=
document.querySelectorAll(".filter");

const products=
document.querySelectorAll(".product");


filters.forEach(filter=>{

filter.addEventListener("click",()=>{

filters.forEach(f=>
f.classList.remove("active")
);

filter.classList.add("active");

const category=
filter.dataset.filter;

products.forEach(product=>{

if(
category==="all" ||
product.dataset.category===category
){

product.style.display="block";

}else{

product.style.display="none";

}

});

});

});


/* =========================================================
   CONTACT → WHATSAPP
========================================================= */

document
.getElementById("contactForm")
.addEventListener("submit",(e)=>{

e.preventDefault();

const name=
document.getElementById("cname").value;

const phone=
document.getElementById("cphone").value;

const service=
document.getElementById("cservice").value;

const message=
document.getElementById("cmessage").value;

const text=

`Merhaba AHM Mobilya,

Bilgi almak istiyorum.

Ad Soyad: ${name}
Telefon: ${phone}
İlgilendiğim kategori: ${service}

Mesaj:
${message}`;

const url=
"https://wa.me/903622669796?text="
+
encodeURIComponent(text);

window.open(url,"_blank");

});


/* =========================================================
   SMOOTH LINKS
========================================================= */

document
.querySelectorAll('a[href^="#"]')
.forEach(link=>{

link.addEventListener("click",function(e){

const target=
document.querySelector(
this.getAttribute("href")
);

if(target){

e.preventDefault();

target.scrollIntoView({
behavior:"smooth"
});

}

});

});

</script>

</body>

</html>
```
