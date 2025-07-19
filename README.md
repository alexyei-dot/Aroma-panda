# Aroma-panda<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Panda Aroma - Ароматические украшения</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Pacifico&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --primary: #8bc34a;
            --secondary: #4caf50;
            --accent: #ff9800;
            --light: #f9f9f9;
            --dark: #333;
            --text: #555;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            color: var(--text);
            background-color: #fff;
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        header {
            background-color: white;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            padding: 15px 5%;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo img {
            height: 50px;
            margin-right: 15px;
        }
        
        .logo h1 {
            font-family: 'Pacifico', cursive;
            color: var(--secondary);
            font-size: 24px;
            font-weight: 400;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }
        
        nav ul li a:hover {
            color: var(--accent);
        }
        
        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent);
            transition: width 0.3s;
        }
        
        nav ul li a:hover::after {
            width: 100%;
        }
        
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0.9)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%23f0f0f0"/><path d="M20,20 Q40,5 60,20 T100,20 Q85,40 100,60 T100,100 Q60,85 20,100 T0,100 Q5,60 0,20 T20,20 Z" fill="%238bc34a" opacity="0.1"/></svg>');
            background-size: cover;
            display: flex;
            align-items: center;
            padding: 0 5%;
            margin-top: 80px;
        }
        
        .hero-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            align-items: center;
            justify-content: space-between;
            width: 100%;
        }
        
        .hero-text {
            flex: 1;
            padding-right: 50px;
        }
        
        .hero-text h2 {
            font-size: 2.8rem;
            color: var(--dark);
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        .hero-text p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            max-width: 600px;
        }
        
        .highlight {
            color: var(--secondary);
            font-weight: 700;
        }
        
        .cta-button {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            padding: 15px 35px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(255, 152, 0, 0.3);
        }
        
        .cta-button:hover {
            background-color: #e68a00;
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(255, 152, 0, 0.4);
        }
        
        .hero-image {
            flex: 1;
            position: relative;
            display: flex;
            justify-content: center;
        }
        
        .panda-circle {
            width: 400px;
            height: 400px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
            position: relative;
        }
        
        .panda-face {
            position: relative;
            width: 300px;
            height: 300px;
        }
        
        .panda-ears {
            position: absolute;
            top: -30px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 150px;
        }
        
        .ear {
            width: 70px;
            height: 70px;
            background-color: #333;
            border-radius: 50%;
        }
        
        .panda-eyes {
            position: absolute;
            top: 70px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 100px;
        }
        
        .eye {
            width: 50px;
            height: 50px;
            background-color: #333;
            border-radius: 50%;
            position: relative;
        }
        
        .eye::before {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: white;
            border-radius: 50%;
            top: 10px;
            left: 10px;
        }
        
        .panda-nose {
            position: absolute;
            top: 130px;
            left: 50%;
            transform: translateX(-50%);
            width: 40px;
            height: 30px;
            background-color: #333;
            border-radius: 50%;
        }
        
        .panda-mouth {
            position: absolute;
            top: 160px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 50px;
            border-bottom: 8px solid #333;
            border-radius: 0 0 50px 50px;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: var(--dark);
            margin-bottom: 60px;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--accent);
            border-radius: 2px;
        }
        
        .products {
            padding: 100px 5%;
            background-color: var(--light);
        }
        
        .products-container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }
        
        .product-card {
            background-color: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
        }
        
        .product-image {
            height: 200px;
            background-color: #f0f0f0;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
        }
        
        .bracelet-img {
            width: 180px;
            height: 180px;
            background: linear-gradient(45deg, #a5d6a7, #81c784);
            border-radius: 50%;
            position: relative;
        }
        
        .bracelet-img::before {
            content: '';
            position: absolute;
            width: 160px;
            height: 30px;
            background: linear-gradient(45deg, #d7ccc8, #bcaaa4);
            border-radius: 15px;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
        
        .pendant-img {
            width: 150px;
            height: 150px;
            background: linear-gradient(45deg, #ffcc80, #ffb74d);
            border-radius: 50%;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .pendant-img::before {
            content: '☯';
            font-size: 50px;
            color: white;
        }
        
        .product-info {
            padding: 25px;
        }
        
        .product-title {
            font-size: 1.5rem;
            color: var(--dark);
            margin-bottom: 10px;
        }
        
        .product-price {
            font-size: 1.8rem;
            color: var(--secondary);
            font-weight: 700;
            margin-bottom: 15px;
        }
        
        .product-description {
            margin-bottom: 20px;
        }
        
        .aromas {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }
        
        .aroma {
            background-color: #e8f5e9;
            color: var(--secondary);
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
        }
        
        .buy-button {
            display: block;
            width: 100%;
            background-color: var(--accent);
            color: white;
            border: none;
            padding: 12px;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .buy-button:hover {
            background-color: #e68a00;
        }
        
        .promo-section {
            padding: 100px 5%;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            text-align: center;
        }
        
        .promo-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .promo-title {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        
        .promo-text {
            font-size: 1.3rem;
            margin-bottom: 40px;
            line-height: 1.8;
        }
        
        .promo-highlight {
            background-color: white;
            color: var(--secondary);
            padding: 5px 15px;
            border-radius: 30px;
            font-weight: 700;
            display: inline-block;
            margin: 0 5px;
        }
        
        .values {
            padding: 100px 5%;
            background-color: white;
        }
        
        .values-container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .values-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }
        
        .value-card {
            text-align: center;
            padding: 30px;
        }
        
        .value-icon {
            font-size: 3rem;
            color: var(--accent);
            margin-bottom: 20px;
        }
        
        .value-title {
            font-size: 1.5rem;
            color: var(--dark);
            margin-bottom: 15px;
        }
        
        footer {
            background-color: var(--dark);
            color: white;
            padding: 60px 5% 30px;
        }
        
        .footer-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
        }
        
        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 2px;
            background-color: var(--accent);
        }
        
        .footer-column p {
            margin-bottom: 10px;
            opacity: 0.8;
        }
        
        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            transition: background-color 0.3s;
        }
        
        .social-icons a:hover {
            background-color: var(--accent);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            margin-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            opacity: 0.7;
        }
        
        @media (max-width: 900px) {
            .hero-content {
                flex-direction: column;
                text-align: center;
            }
            
            .hero-text {
                padding-right: 0;
                margin-bottom: 50px;
            }
            
            .panda-circle {
                width: 300px;
                height: 300px;
            }
            
            .panda-face {
                width: 220px;
                height: 220px;
            }
            
            .panda-ears {
                gap: 110px;
            }
            
            .panda-eyes {
                gap: 70px;
            }
        }
        
        @media (max-width: 600px) {
            .header-container {
                flex-direction: column;
            }
            
            nav ul {
                margin-top: 20px;
            }
            
            .hero-text h2 {
                font-size: 2.2rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Шапка сайта -->
    <header>
        <div class="header-container">
            <div class="logo">
                <div class="panda-icon">
                    <svg width="50" height="50" viewBox="0 0 100 100">
                        <circle cx="50" cy="50" r="45" fill="#333"/>
                        <circle cx="35" cy="40" r="8" fill="white"/>
                        <circle cx="65" cy="40" r="8" fill="white"/>
                        <circle cx="35" cy="40" r="3" fill="#333"/>
                        <circle cx="65" cy="40" r="3" fill="#333"/>
                        <ellipse cx="50" cy="60" rx="10" ry="6" fill="#333"/>
                        <circle cx="30" cy="30" r="5" fill="#333"/>
                        <circle cx="70" cy="30" r="5" fill="#333"/>
                    </svg>
                </div>
                <h1>Panda Aroma</h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#products">Товары</a></li>
                    <li><a href="#promo">Акции</a></li>
                    <li><a href="#values">О нас</a></li>
                    <li><a href="#footer">Контакты</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Основной баннер -->
    <section class="hero">
        <div class="hero-content">
            <div class="hero-text">
                <h2>Ароматические украшения <span class="highlight">Panda</span></h2>
                <p>Мы создаем неповторимую ауру вокруг тебя. Наши украшения дарят свежесть и гармонию на весь день.</p>
                <p><em>Важен каждый момент жизни</em> — наполни его приятными ароматами!</p>
                <a href="#products" class="cta-button">Выбрать аромат</a>
            </div>
            <div class="hero-image">
                <div class="panda-circle">
                    <div class="panda-face">
                        <div class="panda-ears">
                            <div class="ear"></div>
                            <div class="ear"></div>
                        </div>
                        <div class="panda-eyes">
                            <div class="eye"></div>
                            <div class="eye"></div>
                        </div>
                        <div class="panda-nose"></div>
                        <div class="panda-mouth"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Раздел с товарами -->
    <section id="products" class="products">
        <div class="products-container">
            <h2 class="section-title">Наши Ароматические Украшения</h2>
            <div class="product-grid">
                <!-- Браслет -->
                <div class="product-card">
                    <div class="product-image">
                        <div class="bracelet-img"></div>
                    </div>
                    <div class="product-info">
                        <h3 class="product-title">Ароматический браслет</h3>
                        <div class="product-price">150₽</div>
                        <p class="product-description">Элегантный браслет с аромакапсулой. Легкий и стильный аксессуар, который наполнит ваш день приятными ароматами.</p>
                        <div class="aromas">
                            <span class="aroma">Свежесть утра</span>
                            <span class="aroma">Весенний дождь</span>
                            <span class="aroma">Зеленый чай</span>
                        </div>
                        <button class="buy-button">Добавить в корзину</button>
                    </div>
                </div>
                
                <!-- Подвеска -->
                <div class="product-card">
                    <div class="product-image">
                        <div class="pendant-img"></div>
                    </div>
                    <div class="product-info">
                        <h3 class="product-title">Ароматическая подвеска</h3>
                        <div class="product-price">300₽</div>
                        <p class="product-description">Изящная подвеска на шею со сменными аромакапсулами. Идеальный аксессуар для тех, кто ценит стиль и свежесть.</p>
                        <div class="aromas">
                            <span class="aroma">Свежесть утра</span>
                            <span class="aroma">Весенний дождь</span>
                            <span class="aroma">Зеленый чай</span>
                        </div>
                        <button class="buy-button">Добавить в корзину</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Раздел с акцией -->
    <section id="promo" class="promo-section">
        <div class="promo-content">
            <h2 class="promo-title">Специальное предложение!</h2>
            <p class="promo-text">
                Купи <span class="promo-highlight">2 ароматические подвески</span> и получи
                <span class="promo-highlight">3-ю в подарок</span>!
            </p>
            <p class="promo-text">
                Успейте воспользоваться выгодным предложением. Акция действует до конца месяца.
            </p>
            <a href="#products" class="cta-button">Воспользоваться акцией</a>
        </div>
    </section>

    <!-- Раздел "Наши ценности" -->
    <section id="values" class="values">
        <div class="values-container">
            <h2 class="section-title">Почему выбирают нас</h2>
            <div class="values-grid">
                <div class="value-card">
                    <div class="value-icon">
                        <i class="fas fa-leaf"></i>
                    </div>
                    <h3 class="value-title">Натуральные ароматы</h3>
                    <p>Мы используем только натуральные эфирные масла, которые дарят свежесть и бодрость без химии.</p>
                </div>
                <div class="value-card">
                    <div class="value-icon">
                        <i class="fas fa-heart"></i>
                    </div>
                    <h3 class="value-title">Ручная работа</h3>
                    <p>Каждое украшение создается с любовью и вниманием к деталям нашими мастерами.</p>
                </div>
                <div class="value-card">
                    <div class="value-icon">
                        <i class="fas fa-recycle"></i>
                    </div>
                    <h3 class="value-title">Экологичность</h3>
                    <p>Наши изделия созданы из экологичных материалов, безопасных для вас и природы.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Подвал сайта -->
    <footer id="footer">
        <div class="footer-container">
            <div class="footer-column">
                <h3>Panda Aroma</h3>
                <p>Мы создаем неповторимую ауру с помощью ароматических украшений, которые дарят свежесть и гармонию на весь день.</p>
                <div class="social-icons">
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-vk"></i></a>
                    <a href="#"><i class="fab fa-telegram"></i></a>
                    <a href="#"><i class="fab fa-whatsapp"></i></a>
                </div>
            </div>
            <div class="footer-column">
                <h3>Контакты</h3>
                <p><i class="fas fa-map-marker-alt"></i> г. Москва, ул. Ароматная, 15</p>
                <p><i class="fas fa-phone"></i> +7 (999) 123-45-67</p>
                <p><i class="fas fa-envelope"></i> info@panda-aroma.ru</p>
            </div>
            <div class="footer-column">
                <h3>Часы работы</h3>
                <p>Пн-Пт: 10:00 - 20:00</p>
                <p>Сб-Вс: 11:00 - 18:00</p>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2023 Panda Aroma. Все права защищены.</p>
        </div>
    </footer>

    <script>
        // Плавная прокрутка для навигации
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Анимация при скролле
        const animateOnScroll = () => {
            const elements = document.querySelectorAll('.product-card, .value-card');
            elements.forEach(element => {
                const elementPosition = element.getBoundingClientRect().top;
                const screenPosition = window.innerHeight / 1.3;
                
                if(elementPosition < screenPosition) {
                    element.style.opacity = "1";
                    element.style.transform = "translateY(0)";
                }
            });
        };

        // Инициализация анимации
        window.addEventListener('scroll', animateOnScroll);
        document.querySelectorAll('.product-card, .value-card').forEach(card => {
            card.style.opacity = "0";
            card.style.transform = "translateY(20px)";
            card.style.transition = "opacity 0.5s ease, transform 0.5s ease";
        });
        
        // Вызов при загрузке для элементов в видимой области
        window.addEventListener('load', animateOnScroll);
    </script>
</body>
</html>
