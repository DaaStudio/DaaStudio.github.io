<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DAA Studio - Mobil Uygulama Geliştiricisi</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #007bff;
            --secondary-color: #f8f9fa;
            --text-color: #343a40;
            --link-color: #0056b3;
            --background-color: #ffffff;
            --header-height: 80px;
        }

        /* Genel stiller */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--background-color);
            padding-top: var(--header-height);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Başlık (Header) ve Menü */
        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
            height: var(--header-height);
            display: flex;
            align-items: center;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
        }

        .logo {
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
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
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--primary-color);
        }

        /* Ana Bölüm (Hero) */
        .hero-section {
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            text-align: center;
            padding: 100px 0;
            background: linear-gradient(135deg, var(--secondary-color), #e9ecef);
            min-height: calc(100vh - var(--header-height));
        }

        .hero-content {
            max-width: 800px;
        }

        .profile-image {
            width: 250px;
            height: 250px;
            border-radius: 50%;
            object-fit: cover;
            border: 8px solid #fff;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            margin-bottom: 30px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 20px;
            color: var(--primary-color);
            line-height: 1.2;
        }

        .hero-content p {
            font-size: 1.5rem;
            margin-bottom: 40px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            color: #555;
        }

        .cta-button {
            display: inline-block;
            background-color: var(--primary-color);
            color: #fff;
            padding: 15px 35px;
            font-size: 1.2rem;
            font-weight: 600;
            text-decoration: none;
            border-radius: 50px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .cta-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 123, 255, 0.3);
        }

        /* Hakkında Bölümü */
        .about-section {
            padding: 80px 0;
            background-color: #fff;
            text-align: center;
        }

        .about-section h2 {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 20px;
            color: var(--text-color);
        }

        .about-section p {
            max-width: 900px;
            margin: 0 auto;
            font-size: 1.15rem;
            line-height: 1.8;
            color: #666;
        }

        /* Alt kısım (Footer) */
        footer {
            background-color: var(--text-color);
            color: var(--secondary-color);
            text-align: center;
            padding: 30px 0;
            font-size: 1rem;
        }

        footer a {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 600;
        }

        /* Mobil uyumluluk */
        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                gap: 20px;
            }

            .nav-links {
                gap: 20px;
                flex-wrap: wrap;
                justify-content: center;
            }

            .logo {
                margin-bottom: 10px;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .hero-content p {
                font-size: 1.2rem;
            }

            .cta-button {
                padding: 12px 30px;
                font-size: 1rem;
            }

            .profile-image {
                width: 180px;
                height: 180px;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="container navbar">
            <a href="https://daastudio.github.io/" class="logo">DAA Studio</a>
            <nav>
                <ul class="nav-links">
                    <li><a href="https://daastudio.github.io/">Anasayfa</a></li>
                    <li><a href="https://play.google.com/store/apps/dev?id=5180315254549954413" target="_blank">Uygulamalar</a></li>
                    <li><a href="#hakkinda">Hakkında</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <section class="hero-section">
            <div class="container hero-content">
                <img src="https://i.hizliresim.com/k6x352i.png" alt="DAA Studio Mobil Geliştiricisi" class="profile-image">
                <h1>Merhaba, Ben DAA Studio!</h1>
                <p>Kullanıcıların hayatını kolaylaştıran, eğlenceli ve yenilikçi mobil uygulamalar geliştiriyorum.</p>
                <a href="https://play.google.com/store/apps/dev?id=5180315254549954413" target="_blank" class="cta-button">Uygulamalarımı Keşfet</a>
            </div>
        </section>

        <section id="hakkinda" class="about-section">
            <div class="container">
                <h2>Hakkımda</h2>
                <p>
                    DAA Studio olarak, mobil teknolojinin sınırlarını zorlayan uygulamalar geliştirmeye odaklanıyorum.
                    Her proje, kullanıcı deneyimini merkeze alarak tasarlanıyor ve sade, kullanışlı arayüzlerle
                    güçlü özellikleri bir araya getiriyor. Google Play'deki geliştirici sayfamı incelediğinizde,
                    küçük bir stüdyonun büyük fikirleri nasıl hayata geçirebileceğine şahit olacaksınız.
                    Amacım, her dokunuşta fark yaratan uygulamalarla dijital dünyanıza değer katmak.
                </p>
                <p>
                    Oyunlardan yaşam tarzı uygulamalarına kadar geniş bir yelpazede projeler üretiyorum.
                    Her bir uygulama, tutku ve titizlikle geliştirilmiş birer eserdir.
                    Geleceğin mobil deneyimlerini birlikte şekillendirmek için sürekli öğreniyor ve
                    kendimi geliştiriyorum.
                </p>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2025 DAA Studio. Tüm hakları saklıdır. | <a href="https://daastudio.github.io/">daastudio.github.io</a></p>
        </div>
    </footer>

</body>
</html>
