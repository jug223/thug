<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AstroLab 88 - 88-Key Keyboard & Creative Hub | Arturia</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Основные стили */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        a {
            text-decoration: none;
            color: inherit;
            transition: all 0.3s ease;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .section-title {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
            color: #000;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: #ff5500;
            margin: 10px auto;
            border-radius: 2px;
        }
        
        .btn {
            display: inline-block;
            background-color: #ff5500;
            color: #fff;
            padding: 12px 30px;
            border-radius: 30px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 0.9rem;
        }
        
        .btn:hover {
            background-color: #e64a00;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(255, 85, 0, 0.3);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid #ff5500;
            color: #ff5500;
        }
        
        .btn-outline:hover {
            background: #ff5500;
            color: #fff;
        }
        
        /* Шапка сайта */
        header {
            background-color: #000;
            color: #fff;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 28px;
            font-weight: bold;
            color: #ff5500;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 10px;
            font-size: 24px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 25px;
            position: relative;
        }
        
        nav ul li a {
            font-size: 14px;
            text-transform: uppercase;
            font-weight: 500;
            padding: 5px 0;
        }
        
        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: #ff5500;
            transition: width 0.3s ease;
        }
        
        nav ul li a:hover::after {
            width: 100%;
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: #fff;
            font-size: 24px;
            cursor: pointer;
        }
        
        /* Герой-секция */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1511379938547-c1f69419868d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: #fff;
            text-align: center;
            padding: 150px 0;
            position: relative;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            animation: fadeIn 1s ease;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 2px;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.5);
        }
        
        .hero p {
            font-size: 1.3rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }
        
        /* Секция описания */
        .description {
            padding: 100px 0;
            background-color: #fff;
        }
        
        .description-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .description-text {
            flex: 1;
        }
        
        .description-text h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: #000;
        }
        
        .description-text p {
            margin-bottom: 20px;
            font-size: 1.1rem;
            line-height: 1.8;
        }
        
        .description-image {
            flex: 1;
            text-align: center;
            position: relative;
        }
        
        .description-image img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
            transition: transform 0.5s ease;
        }
        
        .description-image:hover img {
            transform: scale(1.03);
        }
        
        /* Секция характеристик */
        .features {
            padding: 100px 0;
            background-color: #f9f9f9;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }
        
        .feature-item {
            background-color: #fff;
            padding: 40px 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .feature-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: #ff5500;
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }
        
        .feature-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }
        
        .feature-item:hover::before {
            transform: scaleX(1);
        }
        
        .feature-icon {
            font-size: 50px;
            margin-bottom: 20px;
            color: #ff5500;
        }
        
        .feature-item h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }
        
        /* Секция галереи */
        .gallery {
            padding: 100px 0;
            background-color: #fff;
        }
        
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }
        
        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            height: 300px;
            cursor: pointer;
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .gallery-item:hover img {
            transform: scale(1.1);
        }
        
        .gallery-item::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.3);
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .gallery-item:hover::after {
            opacity: 1;
        }
        
        /* Секция отзывов */
        .testimonials {
            padding: 100px 0;
            background-color: #f9f9f9;
        }
        
        .testimonials-container {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .testimonial {
            background: #fff;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            margin-bottom: 30px;
            position: relative;
        }
        
        .testimonial::before {
            content: '"';
            font-size: 80px;
            color: #ff5500;
            position: absolute;
            top: -20px;
            left: 20px;
            opacity: 0.2;
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
            font-size: 1.1rem;
            line-height: 1.8;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 15px;
        }
        
        .author-avatar img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .author-info h4 {
            font-size: 1.1rem;
            margin-bottom: 5px;
        }
        
        .author-info p {
            font-size: 0.9rem;
            color: #777;
        }
        
        /* Секция покупки */
        .purchase {
            padding: 100px 0;
            background-color: #000;
            color: #fff;
            text-align: center;
        }
        
        .purchase h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        
        .purchase p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
            opacity: 0.9;
        }
        
        .price {
            font-size: 3.5rem;
            font-weight: bold;
            color: #ff5500;
            margin-bottom: 30px;
        }
        
        .purchase-features {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin: 40px 0;
        }
        
        .purchase-feature {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .purchase-feature i {
            color: #ff5500;
            font-size: 1.2rem;
        }
        
        /* Подвал */
        footer {
            background-color: #111;
            color: #fff;
            padding: 70px 0 20px;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }
        
        .footer-section {
            flex: 1;
            padding: 0 20px;
            min-width: 250px;
            margin-bottom: 30px;
        }
        
        .footer-section h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            color: #ff5500;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-section h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 2px;
            background: #ff5500;
        }
        
        .footer-section ul {
            list-style: none;
        }
        
        .footer-section ul li {
            margin-bottom: 10px;
        }
        
        .footer-section ul li a:hover {
            color: #ff5500;
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: #222;
            border-radius: 50%;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background: #ff5500;
            transform: translateY(-3px);
        }
        
        .newsletter-form {
            display: flex;
            margin-top: 20px;
        }
        
        .newsletter-form input {
            flex: 1;
            padding: 12px 15px;
            border: none;
            border-radius: 30px 0 0 30px;
            outline: none;
        }
        
        .newsletter-form button {
            background: #ff5500;
            color: #fff;
            border: none;
            padding: 0 20px;
            border-radius: 0 30px 30px 0;
            cursor: pointer;
            transition: background 0.3s ease;
        }
        
        .newsletter-form button:hover {
            background: #e64a00;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #333;
            font-size: 0.9rem;
            color: #777;
        }
        
        /* Анимации */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease;
        }
        
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Адаптивность */
        @media (max-width: 992px) {
            .features-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .gallery-grid {
                grid-template-columns: 1fr;
            }
            
            .hero h1 {
                font-size: 2.8rem;
            }
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-wrap: wrap;
            }
            
            nav {
                width: 100%;
                margin-top: 15px;
                display: none;
            }
            
            nav.active {
                display: block;
            }
            
            nav ul {
                flex-direction: column;
            }
            
            nav ul li {
                margin: 10px 0;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .description-content {
                flex-direction: column;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
            
            .footer-content {
                flex-direction: column;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .purchase-features {
                flex-direction: column;
                gap: 20px;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
        
        @media (max-width: 576px) {
            .hero {
                padding: 100px 0;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .description, .features, .gallery, .testimonials, .purchase {
                padding: 70px 0;
            }
        }
    </style>
</head>
<body>
    <!-- Шапка сайта -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-music"></i> ARTURIA
                </div>
                <button class="mobile-menu-btn">
                    <i class="fas fa-bars"></i>
                </button>
                <nav id="main-nav">
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#description">Overview</a></li>
                        <li><a href="#features">Features</a></li>
                        <li><a href="#gallery">Gallery</a></li>
                        <li><a href="#testimonials">Reviews</a></li>
                        <li><a href="#purchase">Buy Now</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Герой-секция -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>AstroLab 88</h1>
                <p>88-Key Keyboard & Creative Hub</p>
                <div class="hero-buttons">
                    <a href="#purchase" class="btn">Buy Now</a>
                    <a href="#features" class="btn btn-outline">Explore Features</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Секция описания -->
    <section class="description" id="description">
        <div class="container">
            <h2 class="section-title">Your All-in-One Creative Studio</h2>
            <div class="description-content">
                <div class="description-text">
                    <p>The AstroLab is a premium 88-key keyboard and creative hub that brings together Arturia's award-winning software instruments and effects with a professional-grade Fatar keybed.</p>
                    <p>With its intuitive interface and powerful sound engine, AstroLab gives you instant access to thousands of pristine sounds, from classic keyboards to modern synths, all in one portable instrument.</p>
                    <p>Whether you're performing on stage or producing in the studio, AstroLab delivers the ultimate creative experience with unparalleled sound quality and expressive playability.</p>
                    <a href="#features" class="btn">Explore Features</a>
                </div>
                <div class="description-image">
                    <img src="https://images.unsplash.com/photo-1571974599782-87624638275f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1031&q=80" alt="AstroLab 88 Keyboard">
                </div>
            </div>
        </div>
    </section>

    <!-- Секция характеристик -->
    <section class="features" id="features">
        <div class="container">
            <h2 class="section-title">Key Features</h2>
            <div class="features-grid">
                <div class="feature-item fade-in">
                    <div class="feature-icon"><i class="fas fa-keyboard"></i></div>
                    <h3>Premium 88-Key Keybed</h3>
                    <p>Fatar TP/100LR weighted hammer action keyboard for expressive playing with aftertouch</p>
                </div>
                <div class="feature-item fade-in">
                    <div class="feature-icon"><i class="fas fa-volume-up"></i></div>
                    <h3>Powerful Sound Engine</h3>
                    <p>Access to 10,000+ sounds from Arturia's acclaimed software collection</p>
                </div>
                <div class="feature-item fade-in">
                    <div class="feature-icon"><i class="fas fa-sliders-h"></i></div>
                    <h3>Intuitive Control</h3>
                    <p>Dedicated controls for filters, envelopes, effects, and more</p>
                </div>
                <div class="feature-item fade-in">
                    <div class="feature-icon"><i class="fas fa-laptop"></i></div>
                    <h3>Seamless Integration</h3>
                    <p>Connect to your DAW or use standalone with built-in audio interface</p>
                </div>
                <div class="feature-item fade-in">
                    <div class="feature-icon"><i class="fas fa-wave-square"></i></div>
                    <h3>Professional Effects</h3>
                    <p>Studio-quality reverb, delay, chorus, and more built-in</p>
                </div>
                <div class="feature-item fade-in">
                    <div class="feature-icon"><i class="fas fa-mobile-alt"></i></div>
                    <h3>Mobile Companion</h3>
                    <p>Use the AstroLab Connect app for additional sound management</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Секция галереи -->
    <section class="gallery" id="gallery">
        <div class="container">
            <h2 class="section-title">Gallery</h2>
            <div class="gallery-grid">
                <div class="gallery-item fade-in">
                    <img src="https://images.unsplash.com/photo-1520523839897-bd0b52f945a0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="AstroLab Front View">
                </div>
                <div class="gallery-item fade-in">
                    <img src="https://images.unsplash.com/photo-1518709268805-4e9042af2176?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1028&q=80" alt="AstroLab Controls">
                </div>
                <div class="gallery-item fade-in">
                    <img src="https://images.unsplash.com/photo-1571974599782-87624638275f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1031&q=80" alt="AstroLab Back Panel">
                </div>
                <div class="gallery-item fade-in">
                    <img src="https://images.unsplash.com/photo-1511379938547-c1f69419868d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="AstroLab in Performance">
                </div>
            </div>
        </div>
    </section>

    <!-- Секция отзывов -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <h2 class="section-title">What Musicians Say</h2>
            <div class="testimonials-container">
                <div class="testimonial fade-in">
                    <p class="testimonial-text">The AstroLab 88 has completely transformed my workflow. The keybed feels incredible, and having access to all those amazing Arturia sounds in one instrument is a game-changer for live performance.</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">
                            <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="User Avatar">
                        </div>
                        <div class="author-info">
                            <h4>Michael Johnson</h4>
                            <p>Professional Keyboardist</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial fade-in">
                    <p class="testimonial-text">As a producer, I appreciate how seamlessly the AstroLab integrates with my DAW. The sound quality is exceptional, and the built-in effects are studio-grade. This is the all-in-one solution I've been waiting for.</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">
                            <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="User Avatar">
                        </div>
                        <div class="author-info">
                            <h4>Sarah Williams</h4>
                            <p>Music Producer</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Секция покупки -->
    <section class="purchase" id="purchase">
        <div class="container">
            <h2>Ready to Create?</h2>
            <p>Experience the ultimate all-in-one keyboard workstation</p>
            <div class="price">$2,499.00</div>
            
            <div class="purchase-features">
                <div class="purchase-feature">
                    <i class="fas fa-shipping-fast"></i>
                    <span>Free Shipping</span>
                </div>
                <div class="purchase-feature">
                    <i class="fas fa-shield-alt"></i>
                    <span>2-Year Warranty</span>
                </div>
                <div class="purchase-feature">
                    <i class="fas fa-headphones"></i>
                    <span>Premium Support</span>
                </div>
            </div>
            
            <a href="#" class="btn">Buy Now</a>
            <p style="margin-top: 20px; font-size: 0.9rem;">30-day money-back guarantee</p>
        </div>
    </section>

    <!-- Подвал -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Products</h3>
                    <ul>
                        <li><a href="#">Software Instruments</a></li>
                        <li><a href="#">Hardware Synths</a></li>
                        <li><a href="#">Keyboards</a></li>
                        <li><a href="#">Controllers</a></li>
                        <li><a href="#">Bundles</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Support</h3>
                    <ul>
                        <li><a href="#">Downloads</a></li>
                        <li><a href="#">Documentation</a></li>
                        <li><a href="#">Knowledge Base</a></li>
                        <li><a href="#">Contact Support</a></li>
                        <li><a href="#">Community</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Company</h3>
                    <ul>
                        <li><a href="#">About Arturia</a></li>
                        <li><a href="#">News</a></li>
                        <li><a href="#">Careers</a></li>
                        <li><a href="#">Contact Us</a></li>
                        <li><a href="#">Press</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Stay Connected</h3>
                    <p>Subscribe to our newsletter for the latest updates and offers.</p>
                    <form class="newsletter-form">
                        <input type="email" placeholder="Your email address" required>
                        <button type="submit"><i class="fas fa-paper-plane"></i></button>
                    </form>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Arturia. All rights reserved. | Designed with <i class="fas fa-heart" style="color: #ff5500;"></i> for musicians</p>
            </div>
        </div>
    </footer>

    <script>
        // Мобильное меню
        document.querySelector('.mobile-menu-btn').addEventListener('click', function() {
            document.getElementById('main-nav').classList.toggle('active');
        });
        
        // Плавная прокрутка для якорных ссылок
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Закрыть мобильное меню после клика
                    document.getElementById('main-nav').classList.remove('active');
                }
            });
        });
        
        // Анимация появления элементов при прокрутке
        const fadeElements = document.querySelectorAll('.fade-in');
        
        const fadeInOnScroll = () => {
            fadeElements.forEach(element => {
                const elementTop = element.getBoundingClientRect().top;
                const elementVisible = 150;
                
                if (elementTop < window.innerHeight - elementVisible) {
                    element.classList.add('visible');
                }
            });
        };
        
        window.addEventListener('scroll', fadeInOnScroll);
        window.addEventListener('load', fadeInOnScroll);
        
        // Фиксированная шапка при прокрутке
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.backgroundColor = 'rgba(0, 0, 0, 0.95)';
                header.style.padding = '10px 0';
            } else {
                header.style.backgroundColor = '#000';
                header.style.padding = '15px 0';
            }
        });
    </script>
</body>
</html>
```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>THUG STORE</title>
    <script src="https://js.stripe.com/v3/"></script>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: Arial; }
        body { background: #1a1a1a; color: white; }
        .container { max-width: 500px; margin: 50px auto; padding: 20px; }
        .logo { color: #ff4444; font-size: 2em; text-align: center; margin-bottom: 30px; }
        .product { background: #2d2d2d; padding: 20px; border-radius: 10px; text-align: center; }
        .price { color: #ff4444; font-size: 1.5em; margin: 15px 0; }
        .buy-btn { background: #ff4444; color: white; border: none; padding: 15px 30px; font-size: 1.2em; border-radius: 5px; cursor: pointer; width: 100%; }
        .test-info { background: #333; padding: 10px; border-radius: 5px; margin: 15px 0; font-size: 0.9em; }
        .card-element { background: white; padding: 10px; border-radius: 5px; margin: 10px 0; }
        #card-errors { color: #ff4444; margin: 10px 0; }
    </style>
</head>
<body>
    <div class="container">
        <div class="logo">THUG STORE</div>
        
        <div class="product">
            <h2>THUG Product</h2>
            <div class="price">$99.99</div>
            
            <div class="test-info">
                <strong>Тест карта:</strong> 4242 4242 4242 4242<br>
                <strong>Дата:</strong> 12/34 <strong>CVC:</strong> 123
            </div>

            <form id="payment-form">
                <input type="email" id="email" placeholder="Email" required style="width: 100%; padding: 10px; margin: 10px 0;">
                
                <div class="card-element" id="card-element"></div>
                <div id="card-errors"></div>
                
                <button type="submit" class="buy-btn" id="submit-btn">
                    ОПЛАТИТЬ $99.99
                </button>
            </form>
        </div>
    </div>

    <script>
        const stripe = Stripe('pk_test_51P8gL02Jd8v8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8w8
