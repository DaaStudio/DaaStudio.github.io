<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DAA Studio - Mobile App Developer</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@700;900&family=Poppins:wght@400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-glow-color: #00f7ff; /* Neon Cyan */
            --secondary-glow-color: #ff00c1; /* Neon Magenta */
            --background-color: #12121c; /* Koyu Uzay Mavisi */
            --surface-color: #1e1e2c; /* Kartlar için biraz daha açık */
            --text-color: #e0e0e0;
            --header-height: 80px;
        }

        /* General styles */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.7;
            color: var(--text-color);
            background-color: var(--background-color);
            /* Sadece masaüstü için padding-top */
            padding-top: var(--header-height);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        h1, h2 {
            font-family: 'Orbitron', sans-serif;
            text-transform: uppercase;
        }

        /* Header and Navigation */
        header {
            background: rgba(18, 18, 28, 0.95);
            backdrop-filter: blur(10px);
            position: fixed; /* Masaüstünde sabit */
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            border-bottom: 1px solid rgba(0, 247, 255, 0.2);
            height: var(--header-height);
            display: flex;
            align-items: center;
            transition: all 0.3s ease;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
        }

        .logo {
            font-family: 'Orbitron', sans-serif;
            font-size: 2.2rem;
            font-weight: 900;
            color: #fff;
            text-decoration: none;
            text-shadow: 
                0 0 5px var(--primary-glow-color),
                0 0 10px var(--primary-glow-color),
                0 0 20px var(--primary-glow-color);
            transition: text-shadow 0.3s ease;
        }
        .logo:hover {
            text-shadow: 
                0 0 10px var(--secondary-glow-color),
                0 0 20px var(--secondary-glow-color),
                0 0 40px var(--secondary-glow-color);
        }

        .nav-links {
            list-style: none;
            display: flex;
            gap: 40px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-color);
            font-weight: 600;
            font-size: 1.1rem;
            transition: color 0.3s ease, text-shadow 0.3s ease;
            text-transform: uppercase;
        }

        .nav-links a:hover {
            color: var(--primary-glow-color);
            text-shadow: 0 0 10px var(--primary-glow-color);
        }

        /* Hamburger menu */
        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 4px;
        }

        .hamburger span {
            width: 25px;
            height: 3px;
            background-color: var(--primary-glow-color);
            transition: all 0.3s ease;
        }

        /* Hero Section */
        .hero-section {
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            text-align: center;
            padding: 100px 0;
            background: radial-gradient(circle, var(--surface-color) 0%, var(--background-color) 70%);
            min-height: calc(100vh - var(--header-height));
            overflow: hidden;
        }

        .profile-image {
            width: 250px;
            height: 250px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--primary-glow-color);
            box-shadow: 
                0 0 15px var(--primary-glow-color),
                0 0 30px var(--primary-glow-color),
                inset 0 0 10px var(--primary-glow-color);
            margin-bottom: 30px;
            animation: pulse 3s infinite;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 15px var(--primary-glow-color), 0 0 30px var(--primary-glow-color), inset 0 0 10px var(--primary-glow-color); border-color: var(--primary-glow-color); }
            50% { box-shadow: 0 0 25px var(--secondary-glow-color), 0 0 50px var(--secondary-glow-color), inset 0 0 15px var(--secondary-glow-color); border-color: var(--secondary-glow-color); }
            100% { box-shadow: 0 0 15px var(--primary-glow-color), 0 0 30px var(--primary-glow-color), inset 0 0 10px var(--primary-glow-color); border-color: var(--primary-glow-color); }
        }

        .hero-content h1 {
            font-size: 4rem;
            font-weight: 700;
            margin-bottom: 20px;
            color: #fff;
            line-height: 1.2;
            text-shadow: 0 0 10px var(--secondary-glow-color);
        }

        .hero-content p {
            font-size: 1.5rem;
            margin-bottom: 40px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            color: var(--text-color);
        }

        .cta-button {
            display: inline-block;
            background-color: transparent;
            color: var(--primary-glow-color);
            border: 2px solid var(--primary-glow-color);
            padding: 15px 35px;
            font-size: 1.2rem;
            font-weight: 600;
            text-decoration: none;
            border-radius: 50px;
            transition: all 0.3s ease;
            box-shadow: 0 0 10px var(--primary-glow-color), inset 0 0 5px var(--primary-glow-color);
            text-transform: uppercase;
        }

        .cta-button:hover {
            background-color: var(--primary-glow-color);
            color: var(--background-color);
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 10px 25px rgba(0, 247, 255, 0.4);
        }

        /* About Section */
        .about-section {
            padding: 100px 0;
            background-color: var(--background-color);
            text-align: center;
            border-top: 1px solid rgba(0, 247, 255, 0.2);
        }
        
        .about-section .container {
            background-color: var(--surface-color);
            padding: 50px;
            border-radius: 20px;
            border: 1px solid rgba(0, 247, 255, 0.3);
            box-shadow: 0 0 30px rgba(255, 0, 193, 0.1);
        }

        .about-section h2 {
            font-size: 2.8rem;
            margin-bottom: 30px;
            color: var(--primary-glow-color);
            text-shadow: 0 0 10px var(--primary-glow-color);
        }

        .about-section p {
            max-width: 800px;
            margin: 0 auto 20px auto;
            font-size: 1.15rem;
            color: var(--text-color);
        }

        /* Footer */
        footer {
            background-color: var(--surface-color);
            color: var(--text-color);
            text-align: center;
            padding: 30px 0;
            font-size: 1rem;
            border-top: 1px solid rgba(0, 247, 255, 0.2);
        }

        footer a {
            color: var(--primary-glow-color);
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s ease, text-shadow 0.3s ease;
        }
        
        footer a:hover {
            color: var(--secondary-glow-color);
            text-shadow: 0 0 5px var(--secondary-glow-color);
        }

        /* Mobile responsive */
        @media (max-width: 768px) {
            /* Header düzeltmeleri */
            body {
                padding-top: 70px; /* Mobilde header sabit olduğu için padding gerekli */
            }
            
            header {
                position: fixed; /* Mobilde de sabit kalsın */
                height: 70px;
                padding: 0;
            }
            
            .navbar {
                padding: 0 20px;
            }
            
            .logo {
                font-size: 1.8rem;
            }
            
            .nav-links {
                position: fixed;
                top: 70px;
                left: 0;
                width: 100%;
                background: rgba(18, 18, 28, 0.95);
                backdrop-filter: blur(10px);
                flex-direction: column;
                align-items: center;
                padding: 20px 0;
                gap: 20px;
                transform: translateY(-100%);
                opacity: 0;
                visibility: hidden;
                transition: all 0.3s ease;
                border-bottom: 1px solid rgba(0, 247, 255, 0.2);
            }
            
            .nav-links.active {
                transform: translateY(0);
                opacity: 1;
                visibility: visible;
            }
            
            .hamburger {
                display: flex;
            }
            
            .hamburger.active span:nth-child(1) {
                transform: rotate(45deg) translate(5px, 5px);
            }
            
            .hamburger.active span:nth-child(2) {
                opacity: 0;
            }
            
            .hamburger.active span:nth-child(3) {
                transform: rotate(-45deg) translate(7px, -6px);
            }
            
            /* Hero section düzeltmeleri */
            .hero-section {
                padding: 60px 0;
                min-height: calc(100vh - 70px);
            }

            .hero-content h1 {
                font-size: 2.2rem;
                padding: 0 10px;
            }

            .hero-content p {
                font-size: 1.1rem;
                padding: 0 15px;
            }
            
            .profile-image {
                width: 180px;
                height: 180px;
            }
            
            .cta-button {
                padding: 12px 30px;
                font-size: 1.1rem;
            }
            
            /* About section düzeltmeleri */
            .about-section {
                padding: 60px 0;
            }

            .about-section .container {
                padding: 30px 20px;
                margin: 0 15px;
            }
            
            .about-section h2 {
                font-size: 2rem;
            }
            
            .about-section p {
                font-size: 1rem;
                text-align: left;
            }
        }
        
        /* Çok küçük ekranlar için ek düzenlemeler */
        @media (max-width: 480px) {
            .hero-content h1 {
                font-size: 1.8rem;
            }
            
            .hero-content p {
                font-size: 1rem;
            }
            
            .profile-image {
                width: 150px;
                height: 150px;
            }
            
            .about-section h2 {
                font-size: 1.8rem;
            }
            
            .logo {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="container navbar">
            <a href="https://daastudio.github.io/" class="logo">DAA Studio</a>
            <div class="hamburger" id="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </div>
            <nav>
                <ul class="nav-links" id="navLinks">
                    <li><a href="https://daastudio.github.io/">Home</a></li>
                    <li><a href="https://play.google.com/store/apps/dev?id=5180315254549954413" target="_blank">Apps</a></li>
                    <li><a href="#about">About</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <section class="hero-section">
            <div class="container hero-content">
                <img src="https://play-lh.googleusercontent.com/ARQlDcWULVh1J3fzM5XAAg2u9_DzN0Y6651lWqjF0d3H3rIptp60D6xgYHucnV54Xg=s94-rw" alt="DAA Studio Mobile Developer" class="profile-image">
                <h1>Hello, I'm DAA Studio!</h1>
                <p>I develop innovative, fun, and user-friendly mobile applications that simplify people's lives.</p>
                <a href="https://play.google.com/store/apps/dev?id=5180315254549954413" target="_blank" class="cta-button">Explore My Apps</a>
            </div>
        </section>

        <section id="about" class="about-section">
            <div class="container">
                <h2>About Me</h2>
                <p>
                    At DAA Studio, I focus on developing applications that push the boundaries of mobile technology.
                    Every project is designed with the user experience at its core, combining clean, intuitive interfaces
                    with powerful features. When you explore my developer page on Google Play, you'll witness how
                    a small studio can bring big ideas to life. My goal is to add value to your digital world
                    with apps that make a difference with every touch.
                </p>
                <p>
                    I develop a wide range of projects, from games to lifestyle applications.
                    Each app is a creation developed with passion and meticulous attention to detail.
                    I am constantly learning and improving myself to shape the mobile experiences of the future, together.
                </p>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>© 2025 DAA Studio. All rights reserved. | <a href="https://daastudio.github.io/">daastudio.github.io</a></p>
        </div>
    </footer>

    <script>
        // Hamburger menu functionality
        const hamburger = document.getElementById('hamburger');
        const navLinks = document.getElementById('navLinks');
        
        hamburger.addEventListener('click', () => {
            hamburger.classList.toggle('active');
            navLinks.classList.toggle('active');
        });
        
        // Menü dışına tıklandığında menüyü kapat
        document.addEventListener('click', (e) => {
            if (!hamburger.contains(e.target) && !navLinks.contains(e.target)) {
                hamburger.classList.remove('active');
                navLinks.classList.remove('active');
            }
        });
        
        // Linklere tıklandığında menüyü kapat
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                hamburger.classList.remove('active');
                navLinks.classList.remove('active');
            });
        });
    </script>

</body>
</html>
