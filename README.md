<!DOCTYPE html>
<html lang="ka">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clippers Barbershop - მამაკაცების პრემიუმ ბარბერშოპი</title>
    <style>
        /* Base Styles */
        :root {
            --primary-black: #0a0a0a;
            --dark-gray: #1a1a1a;
            --medium-gray: #2a2a2a;
            --light-gray: #e0e0e0;
            --white: #ffffff;
            --accent-gold: #d4af37;
            --accent-red: #c41e3a;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--primary-black);
            color: var(--white);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Navigation */
        .navbar {
            background: rgba(10, 10, 10, 0.95);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
        }

        .nav-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--accent-gold);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: var(--white);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--accent-gold);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), 
                        url('https://images.unsplash.com/photo-1585747860715-2ba37e788b70?ixlib=rb-4.0.3') center/cover;
            display: flex;
            align-items: center;
            text-align: center;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            color: var(--accent-gold);
        }

        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            color: var(--light-gray);
        }

        .cta-button {
            background: var(--accent-gold);
            color: var(--primary-black);
            padding: 12px 30px;
            border: none;
            border-radius: 5px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .cta-button:hover {
            background: #b8941f;
            transform: translateY(-2px);
        }

        /* Sections */
        .section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--accent-gold);
        }

        /* Services */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background: var(--dark-gray);
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
            transition: transform 0.3s ease;
            border: 1px solid var(--medium-gray);
        }

        .service-card:hover {
            transform: translateY(-5px);
            border-color: var(--accent-gold);
        }

        .service-price {
            color: var(--accent-gold);
            font-size: 1.5rem;
            font-weight: bold;
            margin-top: 1rem;
        }

        /* Gallery */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1rem;
        }

        .gallery-item {
            height: 300px;
            background: var(--dark-gray);
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        /* Locations */
        .locations-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .location-card {
            background: var(--dark-gray);
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
        }

        .map-container {
            height: 300px;
            margin-top: 1rem;
            border-radius: 10px;
            overflow: hidden;
        }

        .phone-number {
            display: block;
            margin-top: 1rem;
            font-size: 1.2rem;
            color: var(--accent-gold);
            font-weight: bold;
            text-decoration: none;
        }

        /* Reviews */
        .reviews-slider {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .review-card {
            background: var(--dark-gray);
            padding: 2rem;
            border-radius: 10px;
            border-left: 4px solid var(--accent-gold);
        }

        /* Footer */
        .footer {
            background: var(--dark-gray);
            padding: 3rem 0;
            text-align: center;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin: 2rem 0;
        }

        .social-links a {
            color: var(--white);
            font-size: 1.5rem;
            transition: color 0.3s ease;
        }

        .social-links a:hover {
            color: var(--accent-gold);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="container nav-content">
            <div class="logo">CLIPPERS</div>
            <ul class="nav-links">
                <li><a href="#home">მთავარი</a></li>
                <li><a href="#about">ჩვენს შესახებ</a></li>
                <li><a href="#services">სერვისები</a></li>
                <li><a href="#gallery">გალერეა</a></li>
                <li><a href="#reviews">რეცენზიები</a></li>
                <li><a href="#contact">კონტაქტი</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container hero-content">
            <h1>CLIPPERS BARBERSHOP</h1>
            <p>მამაკაცების პრემიუმ ბარბერშოპი თბილისში</p>
            <button class="cta-button" onclick="scrollToLocations()">ვიზიტზე ჩაწერა</button>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section">
        <div class="container">
            <h2 class="section-title">ჩვენს შესახებ</h2>
            <div style="text-align: center; max-width: 800px; margin: 0 auto;">
                <p style="font-size: 1.2rem; color: var(--light-gray);">
                    Clippers Barbershop უკვე 4 წელზე დიდიხანია მამაკაცების პრემიუმ სალონია, რომელიც გთავაზობთ მაღალი ხარისხის სერვისებს თბილისის ორ პრესტიჟულ ლოკაციაზე. ჩვენი პროფესიონალი ბარბერები მუდამ მზად არიან მოგემსახურონ უახლესი სტილებითა და ტექნიკით, ისევე, როგორც სუფთა და მყუდრო გარემოთი.
                </p>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="section" style="background: var(--dark-gray);">
        <div class="container">
            <h2 class="section-title">სერვისები და ფასები</h2>
            <div class="services-grid">
                <div class="service-card">
                    <h3>თმის შეჭრა</h3>
                    <div class="service-price">40 ₾</div>
                </div>
                <div class="service-card">
                    <h3>წვერი</h3>
                    <div class="service-price">25 ₾</div>
                </div>
                <div class="service-card">
                    <h3>თმის შეჭრა + წვერი</h3>
                    <div class="service-price">55 ₾</div>
                </div>
                <div class="service-card">
                    <h3>წარბები</h3>
                    <div class="service-price">15 ₾</div>
                </div>
                <div class="service-card">
                    <h3>ვაქსირების ზონა</h3>
                    <div class="service-price">10 ₾</div>
                </div>
                <div class="service-card">
                    <h3>სახის გაწმენდა</h3>
                    <div class="service-price">50 ₾</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="section">
        <div class="container">
            <h2 class="section-title">ჩვენი ნამუშევრები</h2>
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="/Users/revaztsomaia/Downloads/IMG_2256.JPG" alt="Barber Work">
                </div>
                <div class="gallery-item">
                    <img src="/Users/revaztsomaia/Downloads/IMG_2255.JPG" alt="Barber Work">
                </div>
                <div class="gallery-item">
                    <img src="/Users/revaztsomaia/Downloads/IMG_2254.JPG" alt="Barber Work">
                </div>
                <div class="gallery-item">
                    <img src="/Users/revaztsomaia/Downloads/IMG_2253.JPG" alt="Barber Work">
                </div>
            </div>
        </div>
    </section>

    <!-- Locations Section -->
    <section id="contact" class="section" style="background: var(--dark-gray);">
        <div class="container">
            <h2 class="section-title">ჩვენი ლოკაციები</h2>
            <div class="locations-grid">
                <div class="location-card">
                    <h3>საბურთალოს ფილიალი</h3>
                    <p>სულხან ცინცაძის ქუჩა #5, თბილისი 0160</p>
                    <a href="tel:558506888" class="phone-number">📞 558 506 888</a>
                    <div class="map-container">
                        <iframe 
                            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2978.123456789012!2d44.748809!3d41.732123!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNDHCsDQzJzU1LjciTiA0NMKwNDQnNTUuNyJF!5e0!3m2!1sen!2sge!4v1234567890" 
                            width="100%" 
                            height="100%" 
                            style="border:0;" 
                            allowfullscreen="" 
                            loading="lazy">
                        </iframe>
                    </div>
                </div>
                <div class="location-card">
                    <h3>დიდი დიღომის ფილიალი</h3>
                    <p>მირიან მეფის ქუჩა #47, თბილისი 0160</p>
                    <a href="tel:558596888" class="phone-number">📞 558 596 888</a>
                    <div class="map-container">
                        <iframe 
                            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2978.123456789013!2d44.758809!3d41.742123!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNDHCsDQ0JzM1LjciTiA0NMKwNDUnMzUuNyJF!5e0!3m2!1sen!2sge!4v1234567891" 
                            width="100%" 
                            height="100%" 
                            style="border:0;" 
                            allowfullscreen="" 
                            loading="lazy">
                        </iframe>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Reviews Section -->
    <section id="reviews" class="section">
        <div class="container">
            <h2 class="section-title">მომხმარებელთა შეფასებები</h2>
            <div class="reviews-slider">
                <div class="review-card">
                    <p>"საუკეთესო ბარბერშოპი თბილისში! პროფესიონალური მომსახურება და მაღალი ხარისხი."</p>
                    <strong>- გიორგი ლ.</strong>
                </div>
                <div class="review-card">
                    <p>"ყოველთვის დავტოვებ დადებით შეფასებას. გუნდი საოცარია და შედეგი ყოველთვის შესანიშნავი."</p>
                    <strong>- დავით კ.</strong>
                </div>
                <div class="review-card">
                    <p>"კომფორტული ატმოსფერო, სუფთა და მოწესრიგებული სივრცე. რეკომენდაციას ვუწევ ყველას!"</p>
                    <strong>- ნიკა მ.</strong>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="logo" style="margin-bottom: 1rem;">CLIPPERS</div>
            <p>მამაკაცების პრემიუმ ბარბერშოპი თბილისში</p>
            
            <div class="social-links">
                <a href="https://www.instagram.com/clippers.saburtalo?igsh=MXV3cDh2OGJxYXh6dQ==" target="_blank">
                    📷 Instagram
                </a>
                <a href="https://www.facebook.com/share/1BY9PrGC5g/?mibextid=wwXIfr" target="_blank">
                    📘 Facebook
                </a>
            </div>
            
            <p style="color: var(--light-gray); margin-top: 2rem;">
                © 2024 Clippers Barbershop. ყველა უფლება დაცულია.
            </p>
        </div>
    </footer>

    <script>
        function scrollToLocations() {
            document.getElementById('contact').scrollIntoView({ 
                behavior: 'smooth' 
            });
        }

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Navbar background on scroll
        window.addEventListener('scroll', function() {
            const navbar = document.querySelector('.navbar');
            if (window.scrollY > 100) {
                navbar.style.background = 'rgba(10, 10, 10, 0.98)';
            } else {
                navbar.style.background = 'rgba(10, 10, 10, 0.95)';
            }
        });
    </script>
</body>
</html>
