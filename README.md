# Expresspost-gh
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ExpressPost Ghana - Fast & Reliable Delivery Services</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #e31e25;
            --secondary: #f9a825;
            --dark: #333;
            --light: #f8f9fa;
            --gray: #6c757d;
        }
        
        body {
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        section {
            padding: 80px 0;
        }
        
        h1, h2, h3, h4 {
            margin-bottom: 1rem;
            line-height: 1.2;
        }
        
        h1 {
            font-size: 2.8rem;
        }
        
        h2 {
            font-size: 2.2rem;
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
        }
        
        h2:after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: var(--primary);
        }
        
        p {
            margin-bottom: 1.5rem;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: var(--primary);
            color: white;
            border: none;
            border-radius: 4px;
            font-weight: 600;
            text-decoration: none;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background: #c11a20;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .btn-secondary {
            background: var(--secondary);
        }
        
        .btn-secondary:hover {
            background: #e59400;
        }
        
        /* Header & Navigation */
        header {
            background: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo img {
            height: 50px;
            margin-right: 10px;
        }
        
        .logo h1 {
            font-size: 1.8rem;
            margin: 0;
            color: var(--primary);
        }
        
        .logo span {
            color: var(--secondary);
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
        }
        
        nav ul li a:hover {
            color: var(--primary);
        }
        
        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1586528116311-ad8dd3c8310d?ixlib=rb-4.0.3&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 180px 0 100px;
            margin-top: 80px;
        }
        
        .hero h1 {
            font-size: 3.2rem;
            margin-bottom: 1.5rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        .hero-btns {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 2rem;
        }
        
        /* Services Section */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .service-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
        }
        
        .service-icon {
            background: var(--primary);
            color: white;
            font-size: 2.5rem;
            padding: 25px;
            text-align: center;
        }
        
        .service-content {
            padding: 25px;
        }
        
        .service-content h3 {
            color: var(--primary);
        }
        
        /* Tracking Section */
        .tracking {
            background: #f1f1f1;
            text-align: center;
        }
        
        .tracking-form {
            max-width: 600px;
            margin: 0 auto;
            display: flex;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            border-radius: 4px;
            overflow: hidden;
        }
        
        .tracking-form input {
            flex: 1;
            padding: 15px 20px;
            border: none;
            font-size: 1rem;
        }
        
        .tracking-form button {
            background: var(--primary);
            color: white;
            border: none;
            padding: 0 25px;
            cursor: pointer;
            transition: background 0.3s;
        }
        
        .tracking-form button:hover {
            background: #c11a20;
        }
        
        /* Pricing Section */
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .pricing-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .pricing-card:hover {
            transform: translateY(-5px);
        }
        
        .pricing-header {
            background: var(--primary);
            color: white;
            padding: 20px;
        }
        
        .pricing-header h3 {
            margin: 0;
            font-size: 1.5rem;
        }
        
        .pricing-body {
            padding: 30px 20px;
        }
        
        .price {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--primary);
            margin: 20px 0;
        }
        
        .price span {
            font-size: 1rem;
            color: var(--gray);
        }
        
        .pricing-features {
            list-style: none;
            margin: 20px 0;
        }
        
        .pricing-features li {
            padding: 8px 0;
            border-bottom: 1px solid #eee;
        }
        
        .pricing-features li:last-child {
            border-bottom: none;
        }
        
        /* Contact Section */
        .contact {
            background: #f1f1f1;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }
        
        .contact-info h3 {
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .contact-details {
            margin-bottom: 30px;
        }
        
        .contact-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 20px;
        }
        
        .contact-icon {
            background: var(--primary);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            flex-shrink: 0;
        }
        
        .contact-form {
            background: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }
        
        .form-group textarea {
            height: 150px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 60px 0 30px;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-col h3 {
            color: var(--secondary);
            margin-bottom: 20px;
            font-size: 1.3rem;
        }
        
        .footer-col ul {
            list-style: none;
        }
        
        .footer-col ul li {
            margin-bottom: 10px;
        }
        
        .footer-col ul li a {
            color: #bbb;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-col ul li a:hover {
            color: white;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #bbb;
            font-size: 0.9rem;
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            h1 {
                font-size: 2.4rem;
            }
            
            h2 {
                font-size: 2rem;
            }
            
            .hero h1 {
                font-size: 2.8rem;
            }
        }
        
        @media (max-width: 768px) {
            .mobile-menu {
                display: block;
            }
            
            nav ul {
                display: none;
                position: absolute;
                top: 80px;
                left: 0;
                width: 100%;
                background: white;
                flex-direction: column;
                box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
                padding: 20px 0;
            }
            
            nav ul.show {
                display: flex;
            }
            
            nav ul li {
                margin: 0;
                text-align: center;
                padding: 10px 0;
            }
            
            .hero-btns {
                flex-direction: column;
                align-items: center;
            }
            
            .hero-btns .btn {
                width: 80%;
                margin-bottom: 10px;
            }
            
            .tracking-form {
                flex-direction: column;
            }
            
            .tracking-form input {
                width: 100%;
            }
            
            .tracking-form button {
                padding: 15px;
            }
        }
        
        @media (max-width: 576px) {
            section {
                padding: 60px 0;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .hero {
                padding: 150px 0 80px;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .logo h1 {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNTAiIGhlaWdodD0iNTAiIHZpZXdCb3g9IjAgMCA1MCA1MCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTI1IDBDMTEuMTkyOSAwIDAgMTEuMTkyOSAwIDI1QzAgMzguODA3MSAxMS4xOTI5IDUwIDI1IDUwQzM4LjgwNzEgNTAgNTAgMzguODA3MSA1MCAyNUM1MCAxMS4xOTI5IDM4LjgwNzEgMCAyNSAwWk0zNi4yNSA5LjM3NUw0MC42MjUgMTMuNzVMMzEuODc1IDIyLjVMNDAuNjI1IDMxLjI1TDM2LjI1IDM1LjYyNUwyNSAyNi44NzVMMTMuNzUgMzUuNjI1TDkuMzc1IDMxLjI1TDE4LjEyNSAyMi41TDkuMzc1IDEzLjc1TDEzLjc1IDkuMzc1TDI1IDE4LjEyNUwzNi4yNSA5LjM3NVoiIGZpbGw9IiNFMzFFMjUiLz4KPC9zdmc+Cg==" alt="ExpressPost Ghana Logo">
                <h1>Express<span>Post</span></h1>
            </div>
            <div class="mobile-menu">
                <i class="fas fa-bars"></i>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#tracking">Tracking</a></li>
                    <li><a href="#pricing">Pricing</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>Fast & Reliable Delivery Across Ghana</h1>
            <p>We deliver your packages with speed, security, and efficiency. From Accra to Tamale and everywhere in between, trust ExpressPost Ghana for all your delivery needs.</p>
            <div class="hero-btns">
                <a href="#tracking" class="btn">Track Your Package</a>
                <a href="#contact" class="btn btn-secondary">Schedule a Pickup</a>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services">
        <div class="container">
            <h2>Our Services</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-shipping-fast"></i>
                    </div>
                    <div class="service-content">
                        <h3>Express Delivery</h3>
                        <p>Same-day and next-day delivery services across major cities in Ghana. We guarantee timely delivery of your important packages.</p>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-box"></i>
                    </div>
                    <div class="service-content">
                        <h3>Parcel Delivery</h3>
                        <p>Secure and reliable parcel delivery services for businesses and individuals. Various size options available.</p>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-file-contract"></i>
                    </div>
                    <div class="service-content">
                        <h3>Document Delivery</h3>
                        <p>Specialized handling for important documents, contracts, and legal papers with guaranteed security and confidentiality.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Tracking Section -->
    <section class="tracking" id="tracking">
        <div class="container">
            <h2>Track Your Package</h2>
            <p>Enter your tracking number to check the status of your delivery</p>
            <div class="tracking-form">
                <input type="text" placeholder="Enter tracking number">
                <button type="submit">Track</button>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section id="pricing">
        <div class="container">
            <h2>Delivery Pricing</h2>
            <div class="pricing-grid">
                <div class="pricing-card">
                    <div class="pricing-header">
                        <h3>Standard</h3>
                    </div>
                    <div class="pricing-body">
                        <div class="price">₵15<span>/package</span></div>
                        <ul class="pricing-features">
                            <li>3-5 Business Days</li>
                            <li>Up to 5kg</li>
                            <li>Tracking Included</li>
                            <li>Email Notifications</li>
                        </ul>
                        <a href="#contact" class="btn">Select Plan</a>
                    </div>
                </div>
                <div class="pricing-card">
                    <div class="pricing-header">
                        <h3>Express</h3>
                    </div>
                    <div class="pricing-body">
                        <div class="price">₵25<span>/package</span></div>
                        <ul class="pricing-features">
                            <li>1-2 Business Days</li>
                            <li>Up to 10kg</li>
                            <li>Priority Handling</li>
                            <li>SMS & Email Updates</li>
                        </ul>
                        <a href="#contact" class="btn">Select Plan</a>
                    </div>
                </div>
                <div class="pricing-card">
                    <div class="pricing-header">
                        <h3>Same-Day</h3>
                    </div>
                    <div class="pricing-body">
                        <div class="price">₵40<span>/package</span></div>
                        <ul class="pricing-features">
                            <li>Same Day Delivery</li>
                            <li>Up to 15kg</li>
                            <li>Real-time Tracking</li>
                            <li>Phone & SMS Updates</li>
                        </ul>
                        <a href="#contact" class="btn">Select Plan</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <h2>Contact Us</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Get In Touch</h3>
                    <p>Have questions or need assistance with your delivery? Our team is here to help.</p>
                    
                    <div class="contact-details">
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>
                                <h4>Our Location</h4>
                                <p>123 Liberation Road, Accra, Ghana</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div>
                                <h4>Phone Number</h4>
                                <p>+233 24 123 4567</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>
                                <h4>Email Address</h4>
                                <p>info@expresspostghana.com</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Full Name</label>
                            <input type="text" id="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email Address</label>
                            <input type="email" id="email" required>
                        </div>
                        <div class="form-group">
                            <label for="phone">Phone Number</label>
                            <input type="tel" id="phone">
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" required></textarea>
                        </div>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-col">
                    <h3>ExpressPost Ghana</h3>
                    <p>Your trusted partner for fast and reliable delivery services across Ghana.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div class="footer-col">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#tracking">Tracking</a></li>
                        <li><a href="#pricing">Pricing</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>Services</h3>
                    <ul>
                        <li><a href="#">Express Delivery</a></li>
                        <li><a href="#">Parcel Delivery</a></li>
                        <li><a href="#">Document Delivery</a></li>
                        <li><a href="#">International Shipping</a></li>
                        <li><a href="#">Corporate Solutions</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>Contact Info</h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> 123 Liberation Road, Accra</li>
                        <li><i class="fas fa-phone"></i> +233 24 123 4567</li>
                        <li><i class="fas fa-envelope"></i> info@expresspostghana.com</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 ExpressPost Ghana. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            document.querySelector('nav ul').classList.toggle('show');
        });
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetSection = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetSection.offsetTop - 80,
                    behavior: 'smooth'
                });
                
                // Close mobile menu after clicking a link
                document.querySelector('nav ul').classList.remove('show');
            });
        });
        
        // Form submission
        document.querySelector('.contact-form form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! We will get back to you soon.');
            this.reset();
        });
        
        // Tracking form submission
        document.querySelector('.tracking-form button').addEventListener('click', function() {
            const trackingNumber = document.querySelector('.tracking-form input').value;
            if(trackingNumber.trim() === '') {
                alert('Please enter a tracking number');
            } else {
                alert(`Tracking information for ${trackingNumber} would be displayed here.`);
            }
        });
    </script>
</body>
</html>