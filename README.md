<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ALQUDWAH I Home</title>

<style>
:root{
    --gold1:#f59e0b;
    --gold2:#fbbf24;
    --dark:#134e4a;
    --soft:#fff7ed;
}

*{
    box-sizing:border-box;
    font-family:"Segoe UI",Tahoma,sans-serif;
}

body{
    margin:0;
    background:var(--soft);
    color:#333;
    animation:fadeIn 1s ease;
}

/* ===== LOADING SCREEN ===== */
#loader{
    position:fixed;
    width:100%;
    height:100%;
    background:linear-gradient(135deg,#f59e0b,#fbbf24);
    display:flex;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    z-index:99999;
    color:#134e4a;
}

.loader-wrap{
    display:flex;
    align-items:center;
    gap:15px;
}

.loader-logo{
    width:50px;
    height:50px;
    border-radius:50%;
}

.loader-line{
    width:2px;
    height:40px;
    background:rgba(19,78,74,0.4);
}

.loader-text{
    font-size:26px;
    font-weight:bold;
    letter-spacing:2px;
}

.loader-text span{
    color:#134e4a;
}

.spinner{
    margin-top:25px;
    width:40px;
    height:40px;
    border:4px solid rgba(0,0,0,0.2);
    border-top:4px solid #134e4a;
    border-radius:50%;
    animation:spin 1s linear infinite;
}

@keyframes spin{
    to{transform:rotate(360deg);}
}

/* ===== ANIMATION ===== */
@keyframes fadeIn{
    from{opacity:0}
    to{opacity:1}
}

.fade-up{
    animation:fadeUp .9s ease both;
}

@keyframes fadeUp{
    from{
        opacity:0;
        transform:translateY(25px)
    }
    to{
        opacity:1;
        transform:none
    }
}

/* ===== NAVBAR ===== */
.navbar{
    background:rgba(255,255,255,0.45);
    backdrop-filter:blur(14px);
    -webkit-backdrop-filter:blur(14px);
    padding:14px 22px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    box-shadow:0 8px 25px rgba(0,0,0,.1);
    position:sticky;
    top:0;
    z-index:1000;
    border-bottom:1px solid rgba(255,255,255,0.4);
}

.navbar::after{
    content:"";
    position:absolute;
    bottom:0;
    left:0;
    width:100%;
    height:1px;
    background:linear-gradient(to right,transparent,rgba(255,255,255,0.8),transparent);
}

.logo{
    width:55px;
    border-radius:50%;
    margin-right:10px;
}

/* TEXT LOGO */
.brand-text{
    font-weight:800;
    font-size:18px;
    letter-spacing:1px;
}

.brand-text span{
    color:var(--gold1);
}

/* MENU TENGAH */
.nav-menu{
    position:absolute;
    left:50%;
    transform:translateX(-50%);
    display:flex;
    gap:20px;
}

.navbar a{
    text-decoration:none;
    color:var(--dark);
    font-weight:600;
    transition:.2s;
}

.navbar a:hover{
    color:var(--gold1);
    opacity:.8;
}

/* ===== HAMBURGER ===== */
.menu-icon{
    font-size:24px;
    cursor:pointer;
}

/* ===== DROPDOWN ===== */
.dropdown{
    position:fixed;
    right:20px;
    top:70px;
    background:#fff;
    padding:15px;
    border-radius:10px;
    box-shadow:0 10px 25px rgba(0,0,0,.15);
    display:none;
    z-index:9999;
}

.dropdown a{
    display:block;
    margin:10px 0;
    color:var(--dark);
}

/* ===== POPUP ===== */
.popup{
    position:fixed;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    background:#fff;
    padding:25px;
    border-radius:12px;
    box-shadow:0 20px 40px rgba(0,0,0,.2);
    display:none;
    text-align:center;
    z-index:9999;
}

.popup button{
    margin-top:10px;
    padding:8px 15px;
    border:none;
    background:var(--gold1);
    cursor:pointer;
}

/* ===== HERO ===== */
.welcome{
    min-height:420px;
    background:linear-gradient(135deg,var(--gold2),var(--soft));
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:40px 20px;
}

.welcome h1{
    color:var(--dark);
    font-size:clamp(28px,5vw,40px);
}

.welcome p{
    opacity:.85;
}

/* ===== SECTION ===== */
.section{
    max-width:1000px;
    margin:auto;
    padding:60px 20px;
}

.card{
    background:#fff;
    padding:30px;
    border-radius:14px;
    box-shadow:0 10px 30px rgba(0,0,0,.08);
    margin-bottom:25px;
}

.card h3{
    color:var(--dark);
}

/* ===== BUTTON ===== */
.btn{
    display:inline-block;
    background:linear-gradient(135deg,var(--gold1),var(--gold2));
    color:var(--dark);
    padding:12px 22px;
    border-radius:8px;
    font-weight:600;
    text-decoration:none;
    transition:.25s;
}

.btn:hover{
    transform:translateY(-2px);
    box-shadow:0 10px 20px rgba(0,0,0,.15);
}

/* ===== LOGO ===== */
.logo-tengah{
    display:flex;
    justify-content:center;
    margin:40px 0;
}

.logo-tengah img{
    width:160px;
}

/* ===== MARKET ===== */
.market{
    background:linear-gradient(135deg,var(--gold2),#fff);
    padding:50px 20px;
}

.market-wrap{
    max-width:1000px;
    margin:auto;
    display:flex;
    gap:30px;
    flex-wrap:wrap;
}

.market-text{
    flex:1;
}

.market-card{
    background:#fff;
    padding:20px;
    border-radius:14px;
    box-shadow:0 8px 25px rgba(0,0,0,.12);
    width:240px;
    text-align:center;
}

.market-card img{
    width:100%;
    border-radius:10px;
}

.price{
    color:var(--gold1);
    font-weight:bold;
}

/* ===== RESPONSIVE ===== */
@media(max-width:768px){
    .navbar{
        flex-wrap:wrap;
        justify-content:center;
    }

    .market-wrap{
        flex-direction:column;
        align-items:center;
    }
}
</style>
</head>

<body>

<!-- LOADING -->
<div id="loader">
    <div class="loader-wrap">
        <img src="logo2.png" class="loader-logo">
        <div class="loader-line"></div>
        <div class="loader-text">AL<span>QUDWAH</span></div>
    </div>
    <div class="spinner"></div>
</div>

<!-- NAVBAR -->
<div class="navbar fade-up">
    <div style="display:flex;align-items:center;">
        <img src="logo2.png" class="logo">
        <div class="brand-text">AL<span>QUDWAH</span></div>
    </div>

    <div class="nav-menu">
        <a href="#">Home</a>
        <a href="#">News</a>
        <a href="#">Members</a>
        <a href="#">Contact</a>
    </div>

    <div class="menu-icon" onclick="toggleMenu()">☰</div>
</div>

<!-- DROPDOWN -->
<div class="dropdown" id="dropdown">
    <a href="#" onclick="openLogin()">Login</a>
</div>

<!-- POPUP -->
<div class="popup" id="popup">
    <p><b>Kamu member? Ayo Login!</b></p>
    <button onclick="closeLogin()">Tutup</button>
</div>

<!-- HERO -->
<div class="welcome fade-up">
    <h1>Welcome To ALQUDWAH Official</h1>
    <p>Tempat dimana setiap cerita mengalun bagai melodi.</p>
</div>

<!-- ABOUT -->
<div class="market-card fade-up">
    <h3>Kenali kami melalui gebrakan baru kami!</h3>
</div>

<div class="section">
    <div class="card fade-up">
        <h3>Profile</h3>
        <p>
            ALQUDWAH Di ambil dari bahasa Arab yang artinya " Teladan",
            Adapun ALQUDWAH sendiri adalah akronim dari
            "Ahlul Qurra' Darullughah Wadda'wah" ialah sebuah Komunitas...
        </p>
    </div>

    <div class="card fade-up">
        <h3>Visi & Misi</h3>
        <p>
            • Mengembangkan potensi kreatif<br>
            • Menciptakan karya digital inovatif<br>
            • Menumbuhkan kerja tim profesional
        </p>
    </div>
</div>

<!-- LOGO -->
<div class="logo-tengah fade-up">
    <img src="fusionlogo.png">
</div>

<!-- MARKET -->
<section class="market">
    <div class="market-wrap">
        <div class="market-text fade-up">
            <h2>Don't Miss This</h2>
            <p>DLC eksklusif untuk member Creative Fusion.</p>
            <a href="#" class="btn">Sign In & Get It</a>
        </div>

        <div class="market-card fade-up">
            <img src="fusion1.png">
            <h3>Creative Pack</h3>
            <p>Skin Pack</p>
            <div class="price">FREE</div>
        </div>

        <div class="market-card fade-up">
            <img src="fusion1.png">
            <h3>Creative Pack</h3>
            <p>Skin Pack</p>
            <div class="price">FREE</div>
        </div>
    </div>
</section>

<script>
window.addEventListener("load", function(){
    setTimeout(()=>{
        document.getElementById("loader").style.display="none";
    }, 5000);
});

function toggleMenu(){
    let menu = document.getElementById("dropdown");
    menu.style.display = (menu.style.display === "block") ? "none" : "block";
}

function openLogin(){
    document.getElementById("popup").style.display = "block";
}

function closeLogin(){
    document.getElementById("popup").style.display = "none";
}
</script>

</body>
</html>
