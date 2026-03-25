# 🌐 **Al Mizan Center – Complete Website**

Here's your **fully functional, responsive website** based on the Word document content. Copy-paste into an HTML file and open in browser!

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Al Mizan Center - Digital Marketing & Design Qatar</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* Glass Effect */
        .glass {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000"><defs><radialGradient id="a" cx="50%" cy="50%"><stop offset="0%" stop-color="%23ffffff" stop-opacity="0.1"/><stop offset="100%" stop-color="%23ffffff" stop-opacity="0"/></radialGradient></defs><circle cx="300" cy="200" r="200" fill="url(%23a)"><animate attributeName="r" values="200;250;200" dur="3s" repeatCount="indefinite"/></circle><circle cx="700" cy="600" r="150" fill="url(%23a)"><animate attributeName="r" values="150;200;150" dur="4s" repeatCount="indefinite"/></circle></svg>');
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .hero-content h1 {
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 700;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease-out;
        }

        .hero-content p {
            font-size: clamp(1rem, 2.5vw, 1.25rem);
            margin-bottom: 2rem;
            max-width: 600px;
            animation: fadeInUp 1s ease-out 0.2s both;
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(45deg, #ff6b6b, #feca57);
            color: white;
            padding: 1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            animation: fadeInUp 1s ease-out 0.4s both;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        .cta-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
        }

        /* Fade In Animation */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Sections */
        section {
            padding: 100px 5%;
            max-width: 1400px;
            margin: 0 auto;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Quick Quote */
        .quick-quote {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            text-align: center;
            color: white;
        }

        .quote-form {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            max-width: 800px;
            margin: 2rem auto;
        }

        .form-group {
            position: relative;
        }

        .form-group input, .form-group select {
            width: 100%;
            padding: 1rem;
            border: none;
            border-radius: 15px;
            background: rgba(255,255,255,0.9);
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-group input:focus, .form-group select:focus {
            outline: none;
            background: white;
            transform: scale(1.02);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .quote-btn {
            background: linear-gradient(45deg, #4facfe 0%, #00f2fe 100%);
            color: white;
            border: none;
            padding: 1.2rem 3rem;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            grid-column: 1 / -1;
        }

        .quote-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 35px rgba(0,0,0,0.2);
        }

        /* About Us */
        .about {
            background: #f8f9fa;
            text-align: center;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
            margin-top: 3rem;
        }

        .about-text h2 {
            font-size: 2.5rem;
            color: #333;
            margin-bottom: 1.5rem;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
            margin-top: 2rem;
        }

        .stat {
            text-align: center;
            padding: 2rem;
            background: white;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .stat:hover {
            transform: translateY(-10px);
        }

        .stat-number {
            font-size: 3rem;
            font-weight: 700;
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Services */
        .services {
            background: white;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .service-card {
            background: white;
            padding: 2.5rem;
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            text-align: center;
            transition: all 0.3s ease;
            border-top: 4px solid transparent;
        }

        .service-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 25px 50px rgba(0,0,0,0.15);
        }

        .service-card.digital { border-top-color: #667eea; }
        .service-card.printing { border-top-color: #f093fb; }
        .service-card.web { border-top-color: #4facfe; }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 1.5rem;
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #333;
        }

        /* Portfolio */
        .portfolio {
            background: #f8f9fa;
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .portfolio-item {
            height: 250px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
            font-weight: 600;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .portfolio-item:hover {
            transform: scale(1.05);
        }

        /* Testimonials */
        .testimonials {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-align: center;
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .testimonial {
            background: rgba(255,255,255,0.1);
            padding: 2rem;
            border-radius: 20px;
            backdrop-filter: blur(10px);
        }

        /* Contact */
        .contact {
            background: white;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .contact-info h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: #333;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
            padding: 1rem;
            background: #f8f9fa;
            border-radius: 15px;
            transition: all 0.3s ease;
        }

        .contact-item:hover {
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            transform: translateX(10px);
        }

        .contact-item i {
            font-size: 1.5rem;
            margin-right: 1rem;
            width: 40px;
        }

        .quick-actions {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
        }

        .action-btn {
            flex: 1;
            padding: 1rem 2rem;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .whatsapp { background: #25D366; color: white; }
        .call { background: #ff6b6b; color: white; }

        .action-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 35px rgba(0,0,0,0.2);
        }

        /* Footer */
        .footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        /* Logo Section */
        .logo-section {
            background: linear-gradient(135deg, #ff6b6b, #feca57);
            color: white;
            text-align: center;
            padding: 3rem 5%;
        }

        .logo-designer {
            font-size: 1.5rem;
            font-weight: 600;
            margin-top: 1rem;
        }

        .wing-icon {
            font-size: 4rem;
            margin-bottom: 1rem;
            display: block;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }
            
            section {
                padding: 60px 5%;
            }
            
            .quick-actions {
                flex-direction: column;
            }
        }

        /* Smooth Scroll */
        html {
            scroll-behavior: smooth;
        }

        /* Navbar */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255,255,255,0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 5%;
            transition: all 0.3s ease;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #667eea;
        }

        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
        }

        .hamburger span {
            width: 25px;
            height: 3px;
            background: #333;
            margin: 3px 0;
            transition: 0.3s;
        }
    </style>
</head>
<body>
    <!-- Navbar -->
    <nav class="navbar">
        <div class="nav-container">
            <div class="logo">Al Mizan Center</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>GROW YOUR BUSINESS WITH CONFIDENCE</h1>
            <p>Digital marketing, branding & web design solutions in Qatar. Helping businesses stand out with creative design, strong branding, and powerful online presence since 2017.</p>
            <a href="#quote" class="cta-button">Explore Now</a>
        </div>
    </section>

    <!-- Quick Quote -->
    <section id="quote" class="quick-quote">
        <div class="container">
            <h2 style="font-size: 2.5rem; margin-bottom: 1rem;">Get Your Free Quote</h2>
            <p style="font-size: 1.2rem; margin-bottom: 2rem;">Tell us about your project</p>
            <form class="quote-form">
                <div class="form-group">
                    <select>
                        <option>Service Type</option>
                        <option>Digital Marketing</option>
                        <option>Branding & Logo</option>
                        <option>Web Design</option>
                        <option>Printing</option>
                    </select>
                </div>
                <div class="form-group">
                    <select>
                        <option>Project Type</option>
                        <option>New Project</option>
                        <option>Redesign</option>
                        <option>Maintenance</option>
                    </select>
                </div>
                <div class="form-group">
                    <select>
                        <option>Budget</option>
                        <option>Under 5000 QAR</option>
                        <option>5000-15000 QAR</option>
                        <option>15000+ QAR</option>
                    </select>
                </div>
                <button type="submit" class="quote-btn">Get Quote</button>
            </form>
        </div>
    </section>

    <!-- About Us -->
    <section id="about" class="about">
        <div class="container">
            <h2 style="font-size: 2.5rem; text-align: center; margin-bottom: 1rem;">About Al Mizan Center</h2>
            <p style="text-align: center; font-size: 1.2rem; max-width: 800px; margin: 0 auto 3rem;">
                Qatar-based creative agency established in 2017. We specialize in delivering high-quality digital marketing, branding, and web solutions for businesses of all sizes.
            </p>
            <div class="about-content">
                <div>
                    <p style="font-size: 1.1rem; line-height: 1.8; color: #666;">
                        With over <strong>10,000 successful projects</strong>, we have built a strong reputation for quality, affordability, and customer satisfaction.
                    </p>
                </div>
                <div class="stats">
                    <div class="stat">
                        <div class="stat-number">10,000
