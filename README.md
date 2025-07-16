M_in_X.Tech
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>M_in_X.Tech | Enterprise Technology Solutions</title>
    <style>
        :root {
            --primary: #2563EB; /* Microsoft blue */
            --secondary: #34A853; /* Google green */
            --dark: #202124; /* Google dark */
            --light: #F8F9FA;
            --accent: #FBBC05; /* Google yellow */
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Roboto, -apple-system, sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1440px;
            margin: 0 auto;
        }
        
        /* Microsoft-inspired header */
        header {
            position: fixed;
            width: 100%;
            background: rgba(255,255,255,0.98);
            backdrop-filter: blur(10px);
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
            z-index: 1000;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            font-size: 1.8rem;
            font-weight: 600;
        }
        
        .logo-icon {
            width: 32px;
            height: 32px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }
        
        .nav-links {
            display: flex;
            gap: 2rem;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            position: relative;
            padding: 0.5rem 0;
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        /* Google-inspired hero */
        .hero {
            padding: 12rem 0 6rem;
            text-align: center;
            background: linear-gradient(rgba(255,255,255,0.9), rgba(255,255,255,0.9)), 
                        url('https://source.unsplash.com/random/1600x900/?technology') center/cover no-repeat;
        }
        
        h1 {
            font-size: 3.5rem;
            font-weight: 300;
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }
        
        h1 strong {
            font-weight: 600;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .hero p {
            max-width: 700px;
            margin: 0 auto 2rem;
            font-size: 1.2rem;
            color: #5F6368; /* Google text gray */
        }
        
        .btn {
            display: inline-block;
            padding: 0.8rem 2rem;
            border-radius: 4px;
            font-weight: 500;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .btn-primary {
            background: var(--primary);
            color: white;
            margin-right: 1rem;
        }
        
        .btn-outline {
            border: 1px solid var(--primary);
            color: var(--primary);
        }
        
        /* Microsoft Fluent UI cards */
        .features {
            padding: 6rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 4rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            font-weight: 300;
            margin-bottom: 1rem;
        }
        
        .section-title p {
            max-width: 700px;
            margin: 0 auto;
            color: #5F6368;
        }
        
        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 1px 2px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .card-icon {
            width: 48px;
            height: 48px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 2rem auto 1rem;
            color: white;
            font-size: 1.5rem;
        }
        
        .card-content {
            padding: 1.5rem;
            text-align: center;
        }
        
        /* Google Material footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 4rem 0 2rem;
        }
        
        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }
        
        .footer-col h3 {
            margin-bottom: 1.5rem;
            font-weight: 500;
        }
        
        .footer-col ul {
            list-style: none;
        }
        
        .footer-col li {
            margin-bottom: 0.8rem;
        }
        
        .footer-col a {
            color: #9AA0A6;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-col a:hover {
            color: white;
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid #3C4043;
            color: #9AA0A6;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .hero {
                padding: 8rem 0 4rem;
            }
            
            .nav-links {
                display: none; /* Replace with hamburger menu in production */
            }
        }
    </style>
</head>
<body>
    <!-- Microsoft-inspired header -->
    <header>
        <div class="container">
            <nav>
                <a href="#" class="logo">
                    <div class="logo-icon">MX</div>
                    <span>M_in_X.Tech</span>
                </a>
                <div class="nav-links">
                    <a href="#solutions">Solutions</a>
                    <a href="#products">Products</a>
                    <a href="#industries">Industries</a>
                    <a href="#resources">Resources</a>
                    <a href="#about">About</a>
                    <a href="#contact">Contact</a>
                </div>
            </nav>
        </div>
    </header>

    <!-- Google-inspired hero -->
    <section class="hero">
        <div class="container">
            <h1>Innovative <strong>Technology Solutions</strong> for the Modern Enterprise</h1>
            <p>We deliver cutting-edge software and services that transform businesses and drive digital innovation at scale.</p>
            <div>
                <a href="#contact" class="btn btn-primary">Get Started</a>
                <a href="#solutions" class="btn btn-outline">Learn More</a>
            </div>
        </div>
    </section>

    <!-- Microsoft Fluent UI cards -->
    <section class="features" id="solutions">
        <div class="container">
            <div class="section-title">
                <h2>Our Enterprise Solutions</h2>
                <p>Comprehensive technology services designed for global businesses</p>
            </div>
            <div class="card-grid">
                <div class="card">
                    <div class="card-icon">
                        <i>☁️</i>
                    </div>
                    <div class="card-content">
                        <h3>Cloud Transformation</h3>
                        <p>Modernize your infrastructure with our cloud-native solutions and migration services.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="card-icon">
                        <i>🤖</i>
                    </div>
                    <div class="card-content">
                        <h3>AI & Automation</h3>
                        <p>Implement intelligent systems that learn, adapt, and automate complex processes.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="card-icon">
                        <i>🔒</i>
                    </div>
                    <div class="card-content">
                        <h3>Cybersecurity</h3>
                        <p>Protect your assets with our enterprise-grade security frameworks and monitoring.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Additional sections would go here -->
    <!-- Products, Industries, Case Studies, etc. -->

    <!-- Google Material footer -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <h3>Solutions</h3>
                    <ul>
                        <li><a href="#">Cloud Services</a></li>
                        <li><a href="#">Data Analytics</a></li>
                        <li><a href="#">AI/ML</a></li>
                        <li><a href="#">IoT</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>Industries</h3>
                    <ul>
                        <li><a href="#">Financial Services</a></li>
                        <li><a href="#">Healthcare</a></li>
                        <li><a href="#">Manufacturing</a></li>
                        <li><a href="#">Retail</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>Company</h3>
                    <ul>
                        <li><a href="#">About Us</a></li>
                        <li><a href="#">Leadership</a></li>
                        <li><a href="#">Careers</a></li>
                        <li><a href="#">Newsroom</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>Contact</h3>
                    <ul>
                        <li><a href="#">Sales</a></li>
                        <li><a href="#">Support</a></li>
                        <li><a href="#">Locations</a></li>
                        <li><a href="#">Partners</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>© 2023 M_in_X.Tech. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- Modern features to add in production:
         1. Lazy loading images
         2. Service worker for PWA
         3. Dynamic content loading
         4. Accessibility enhancements -->
</body>
</html>
