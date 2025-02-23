<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Noble Edge - Agence de Marketing</title>
    <style>
        /* Styles de base */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Arimo', sans-serif;
            background-color: #000;
            color: #E5E4E2;
            line-height: 1.6;
            scroll-behavior: smooth;
        }
        /* Barre de navigation */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 8%;
            background-color: rgba(0, 0, 0, 0.9);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            animation: slideDown 1s ease-in-out;
        }
        .menu {
            display: flex;
            gap: 30px;
        }
        .menu a {
            color: #E5E4E2;
            font-weight: bold;
            transition: transform 0.3s, color 0.3s;
        }
        .menu a:hover {
            color: #C9B037;
            transform: scale(1.1);
        }
        .burger-menu {
            display: none;
            cursor: pointer;
            font-size: 30px;
            color: #E5E4E2;
        }
        .menu.active {
            display: block;
        }
        /* Animation du logo */
        #logo {
            transition: opacity 0.3s ease;
        }
        /* Animation du menu burger */
        @media screen and (max-width: 768px) {
            .menu {
                display: none;
                flex-direction: column;
                gap: 20px;
            }
            .burger-menu {
                display: block;
            }
        }
        /* Animation de l'Hero */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 20px;
            background: linear-gradient(135deg, rgba(0, 0, 0, 0.7), rgba(67, 23, 84, 0.8)), url('https://source.unsplash.com/1600x900/?business') center/cover no-repeat;
            animation: fadeIn 2s ease-in-out;
        }
        .hero h1 {
            font-size: 3rem;
            color: #FFFFFF;
            animation: fadeInUp 2s ease-in-out;
        }
        .cta {
            display: inline-block;
            padding: 12px 25px;
            margin-top: 20px;
            background-color: #EB0387;
            color: #E5E4E2;
            font-weight: bold;
            border-radius: 5px;
            transition: 0.3s;
            font-size: 18px;
            animation: bounce 2s infinite;
        }
        .cta:hover {
            background-color: #C9B037;
            transform: scale(1.1);
        }
        /* Section */
        .section {
            padding: 100px 8%;
            text-align: center;
            background: linear-gradient(135deg, rgba(67, 23, 84, 0.7), rgba(0, 0, 0, 0.7));
            animation: fadeInUp 1.5s ease-in-out;
        }
        .contact {
            background: linear-gradient(135deg, rgba(67, 23, 84, 0.7), rgba(0, 0, 0, 0.7)); 
            color: #E5E4E2;
            padding: 80px 8%;
            animation: fadeInUp 2s ease-in-out;
        }
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
        }
        .social-links img {
            width: 40px;
            transition: transform 0.3s ease;
        }
        .social-links img:hover {
            transform: scale(1.2);
        }
        /* Animation de la barre de chargement */
        #portfolio .loading-bar {
            position: relative;
            width: 100%;
            height: 4px;
            background-color: #C9B037;
            animation: loadBar 2s linear infinite;
            margin-top: 20px;
        }
        @keyframes loadBar {
            0% { width: 0; }
            50% { width: 50%; }
            100% { width: 0; }
        }
        /* Animation des éléments */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        @keyframes slideDown {
            from { opacity: 0; transform: translateY(-50px); }
            to { opacity: 1; transform: translateY(0); }
        }
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }
    </style>
</head>
<body>
    <div class="navbar">
        <img id="logo" src="https://via.placeholder.com/150" alt="Noble Edge Logo">
        <div class="menu">
            <a href="#about">À propos</a>
            <a href="#services">Services</a>
            <a href="#portfolio">Portfolio</a>
            <a href="#contact">Contact</a>
        </div>
        <div class="burger-menu" onclick="toggleMenu()">☰</div>
    </div>
    <div class="hero">
        <div>
            <h1>Bienvenue chez Noble Edge</h1>
            <a href="#contact" class="cta">Nous contacter</a>
        </div>
    </div>
    <div class="section" id="about">
        <h2>À propos</h2>
        <p>Votre agence marketing spécialisée dans la stratégie digitale et la communication créative.</p>
    </div>
    <div class="section" id="services">
        <h2>Nos Services</h2>
        <p>Découvrez nos services uniques pour booster votre marque.</p>
    </div>
    <div class="section" id="portfolio">
        <h2>Nos Réalisations</h2>
        <div class="loading-bar"></div>
        <p>Un aperçu de nos projets créatifs.</p>
    </div>
    <div class="section contact" id="contact">
        <h2>Contactez-nous</h2>
        <div class="social-links">
            <a href="https://www.instagram.com/nobleedge.agency/" target="_blank">
                <img src="https://cdn-icons-png.flaticon.com/512/2111/2111463.png" alt="Instagram">
            </a>
            <a href="https://www.linkedin.com/in/enzo-panuela-167ba6261/" target="_blank">
                <img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="LinkedIn">
            </a>
            <a href="https://wa.me/3364663370" target="_blank">
                <img src="https://cdn-icons-png.flaticon.com/512/124/124034.png" alt="WhatsApp">
            </a>
        </div>
        <p>Email : <a href="mailto:nobleedgeagency@gmail.com">nobleedgeagency@gmail.com</a></p>
    </div>
    <script>
        // Fonction pour afficher/cacher le menu burger
        function toggleMenu() {
            const menu = document.querySelector('.menu');
            menu.classList.toggle('active');
        }
        // Script pour cacher le logo au scroll
        window.onscroll = function() {
            const logo = document.getElementById('logo');
            if (window.scrollY > 50) {
                logo.style.opacity = "0"; // Le logo disparaît
            } else {
                logo.style.opacity = "1"; // Le logo réapparaît
            }
        };
    </script>
</body>
</html>
