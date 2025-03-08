 
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ME MOBILES</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        /* Global Styles */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to bottom right, #1e3a8a, #6d28d9);
            color: white;
        }

        /* Navbar */
        nav {
            background: rgba(0, 0, 0, 0.8);
            padding: 15px 20px;
            position: sticky;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav h1 {
            font-size: 24px;
            background: linear-gradient(to right, #ff4d4d, #7928ca);
            -webkit-background-clip: text;
            color: transparent;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .nav-links {
            display: flex;
            gap: 15px;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            padding: 10px 15px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 5px;
            transition: 0.3s;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .nav-links a:hover {
            background: rgba(255, 255, 255, 0.5);
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 50px 20px;
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://images.unsplash.com/photo-1616077168079-7e09a677fb2c?w=1600&q=80');
            background-size: cover;
            background-position: center;
        }

        .hero h1 {
            font-size: 48px;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        .hero p {
            font-size: 20px;
            opacity: 0.9;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
        }

        .hero a {
            display: inline-block;
            margin-top: 20px;
            padding: 12px 24px;
            background: linear-gradient(to right, #7928ca, #ff0080);
            color: white;
            text-decoration: none;
            border-radius: 25px;
            transition: 0.3s;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        .hero a:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
        }

        /* Products */
        .products {
            padding: 50px 20px;
            text-align: center;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            padding: 20px;
        }

        .product {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            transition: 0.3s;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .product:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .product img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 10px;
            margin-bottom: 15px;
        }

        .product h3 {
            margin: 15px 0;
            color: #fff;
            font-size: 1.5rem;
        }

        .product .price {
            font-size: 1.25rem;
            color: #ffd700;
            margin: 10px 0;
            font-weight: bold;
        }

        .product .features {
            margin: 15px 0;
            padding: 0;
            list-style: none;
            color: rgba(255, 255, 255, 0.9);
        }

        .product .features li {
            margin: 5px 0;
        }

        .buy-button {
            display: inline-block;
            padding: 12px 24px;
            background: linear-gradient(to right, #00b09b, #96c93d);
            color: white;
            text-decoration: none;
            border-radius: 25px;
            transition: 0.3s;
            margin-top: 15px;
            font-weight: bold;
        }

        .buy-button:hover {
            background: linear-gradient(to right, #96c93d, #00b09b);
            transform: scale(1.05);
            animation: glow 1.5s ease-out infinite;
        }

        @keyframes glow {
            0% {
                box-shadow: 0 0 5px #00b09b, 0 0 10px #00b09b;
            }
            50% {
                box-shadow: 0 0 20px #96c93d, 0 0 25px #96c93d;
            }
            100% {
                box-shadow: 0 0 5px #00b09b, 0 0 10px #00b09b;
            }
        }

        /* Contact Form */
        .contact {
            text-align: center;
            padding: 50px 20px;
            background: rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(10px);
            margin: 40px 20px;
            border-radius: 20px;
        }

        .contact form {
            max-width: 500px;
            margin: auto;
            padding: 30px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .contact label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #fff;
            text-align: left;
        }

        .contact input,
        .contact textarea {
            width: 100%;
            padding: 12px;
            margin: 8px 0 20px;
            border-radius: 8px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            background: rgba(255, 255, 255, 0.1);
            color: white;
            transition: 0.3s;
        }

        .contact input:focus,
        .contact textarea:focus {
            outline: none;
            border-color: #7928ca;
            box-shadow: 0 0 10px rgba(121, 40, 202, 0.3);
        }

        .contact button {
            background: linear-gradient(to right, #7928ca, #ff0080);
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 25px;
            font-size: 16px;
            cursor: pointer;
            transition: 0.3s;
            width: 100%;
            font-weight: bold;
        }

        .contact button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
        }

        /* Footer */
        footer {
            text-align: center;
            background: rgba(0, 0, 0, 0.8);
            padding: 20px;
            margin-top: 20px;
        }

        /* Media Queries */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 36px;
            }

            .hero p {
                font-size: 18px;
            }

            .products h2 {
                font-size: 24px;
            }

            .nav-links {
                gap: 8px;
            }

            .nav-links a {
                padding: 8px 12px;
                font-size: 14px;
            }
        }
    </style>
</head>
<body>

    <!-- Navbar -->
    <nav>
        <h1>ME MOBILES</h1>
        <div class="nav-links">
            <a href="tel:8489061134" aria-label="Call Now">
                <i class="fas fa-phone"></i> Call Now
            </a>
            <a href="https://maps.app.goo.gl/vb5tbLS44LTodcHE9?g_st=ic" target="_blank" aria-label="Our Location">
                <i class="fas fa-map-marker-alt"></i> Location
            </a>
            <a href="https://www.instagram.com/me_mobiles_krishnagiri" target="_blank" aria-label="Follow Us on Instagram">
                <i class="fab fa-instagram"></i> Follow Us
            </a>
        </div>
    </nav>

    <!-- Hero Section -->
    <div class="hero">
        <h1>Welcome to ME MOBILES</h1>
        <p>Discover the latest in mobile technology</p>
        <a href="#products">Shop Now <i class="fas fa-arrow-right"></i></a>
    </div>

    <!-- Products Section -->
    <section id="products" class="products">
        <h2>Featured Products</h2>
        <div class="product-grid">
            <div class="product">
                <img src="https://images.unsplash.com/photo-1510557880182-3d4d3cba35a5?w=800&q=80" alt="ME Ultra Pro 13" loading="lazy">
                <h3>ME Ultra Pro 13</h3>
                <p class="price">₹74,999</p>
                <ul class="features">
                    <li><i class="fas fa-microchip"></i> Snapdragon 8 Gen 2</li>
                    <li><i class="fas fa-camera"></i> 108MP Camera</li>
                    <li><i class="fas fa-battery-full"></i> 5000mAh Battery</li>
                </ul>
                <a href="https://wa.me/918489061134?text=I'm interested in ME Ultra Pro 13" class="buy-button">
                    <i class="fas fa-shopping-cart"></i> Buy Now
                </a>
            </div>
            <div class="product">
                <img src="https://images.unsplash.com/photo-1592899677977-9c10ca588bbd?w=800&q=80" alt="ME Lite 8" loading="lazy">
                <h3>ME Lite 8</h3>
                <p class="price">₹42,999</p>
                <ul class="features">
                    <li><i class="fas fa-microchip"></i> MediaTek Dimensity 8200</li>
                    <li><i class="fas fa-camera"></i> 64MP Camera</li>
                    <li><i class="fas fa-battery-full"></i> 4500mAh Battery</li>
                </ul>
                <a href="https://wa.me/918489061134?text=I'm interested in ME Lite 8" class="buy-button">
                    <i class="fas fa-shopping-cart"></i> Buy Now
                </a>
            </div>
            <div class="product">
                <img src="https://images.unsplash.com/photo-1578345218746-50a229b3d0f8?w=800&q=80" alt="ME Fold X" loading="lazy">
                <h3>ME Fold X</h3>
                <p class="price">₹1,09,999</p>
                <ul class="features">
                    <li><i class="fas fa-microchip"></i> Snapdragon 8 Gen 2</li>
                    <li><i class="fas fa-camera"></i> 50MP Triple Camera</li>
                    <li><i class="fas fa-battery-full"></i> 4800mAh Battery</li>
                </ul>
                <a href="https://wa.me/918489061134?text=I'm interested in ME Fold X" class="buy-button">
                    <i class="fas fa-shopping-cart"></i> Buy Now
                </a>
            </div>
            <div class="product">
                <img src="https://images.unsplash.com/photo-1533228100845-08145b01de14?w=800&q=80" alt="ME Essential" loading="lazy">
                <h3>ME Essential</h3>
                <p class="price">₹24,999</p>
                <ul class="features">
                    <li><i class="fas fa-microchip"></i> MediaTek Helio G99</li>
                    <li><i class="fas fa-camera"></i> 48MP Camera</li>
                    <li><i class="fas fa-battery-full"></i> 5000mAh Battery</li>
                </ul>
                <a href="https://wa.me/918489061134?text=I'm interested in ME Essential" class="buy-button">
                    <i class="fas fa-shopping-cart"></i> Buy Now
                </a>
            </div>
            <div class="product">
                <img src="https://images.unsplash.com/photo-1616348436168-de43ad0db179?w=800&q=80" alt="ME Pro Max" loading="lazy">
                <h3>ME Pro Max</h3>
                <p class="price">₹89,999</p>
                <ul class="features">
                    <li><i class="fas fa-microchip"></i> Snapdragon 8+ Gen 1</li>
                    <li><i class="fas fa-camera"></i> 200MP Camera</li>
                    <li><i class="fas fa-battery-full"></i> 5500mAh Battery</li>
                </ul>
                <a href="https://wa.me/918489061134?text=I'm interested in ME Pro Max" class="buy-button">
                    <i class="fas fa-shopping-cart"></i> Buy Now
                </a>
            </div>
            <div class="product">
                <img src="https://images.unsplash.com/photo-1585060544812-6b45742d762f?w=800&q=80" alt="ME Lite Pro" loading="lazy">
                <h3>ME Lite Pro</h3>
                <p class="price">₹35,999</p>
                <ul class="features">
                    <li><i class="fas fa-microchip"></i> MediaTek Dimensity 7200</li>
                    <li><i class="fas fa-camera"></i> 50MP Camera</li>
                    <li><i class="fas fa-battery-full"></i> 4500mAh Battery</li>
                </ul>
                <a href="https://wa.me/918489061134?text=I'm interested in ME Lite Pro" class="buy-button">
                    <i class="fas fa-shopping-cart"></i> Buy Now
                </a>
            </div>
        </div>
    </section>

    <!-- Contact Form -->
    <section class="contact">
        <h2>Contact Us</h2>
        <form id="contactForm">
            <label for="name">Your Name</label>
            <input type="text" id="name" name="name" placeholder="Enter your name" required>
            
            <label for="phone">Your Phone</label>
            <input type="tel" id="phone" name="phone" placeholder="Enter your phone number" required>
            
            <label for="message">Your Message</label>
            <textarea id="message" name="message" placeholder="Enter your message" rows="4" required></textarea>
            
            <button type="submit">
                <i class="fab fa-whatsapp"></i> Send Message on WhatsApp
            </button>
        </form>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2025 ME MOBILES. All rights reserved.</p>
    </footer>

    <script>
        // Form Submission Handler (Send to WhatsApp)
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();

            const name = document.getElementById('name').value;
            const phone = document.getElementById('phone').value;
            const message = document.getElementById('message').value;

            const whatsappMessage = `Name: ${name}%0APhone: ${phone}%0AMessage: ${message}`;
            const whatsappURL = `https://wa.me/918489061134?text=${whatsappMessage}`;
            
            // Open WhatsApp with pre-filled message
            window.open(whatsappURL, '_blank');
            
            // Reset form
            this.reset();
        });
    </script>
</body>
</html>
