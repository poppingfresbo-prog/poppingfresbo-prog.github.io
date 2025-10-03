# poppingfresbo-prog.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BEST CREATORS AGENCY - Multimedia Production</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #0a0a0a;
            color: #fff;
            overflow-x: hidden;
        }

        .nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 20px 50px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(10, 10, 10, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .logo {
            font-size: 24px;
            font-weight: 800;
            letter-spacing: 2px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            gap: 40px;
        }

        .nav-links a {
            color: #fff;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
            position: relative;
        }

        .nav-links a:hover {
            color: #667eea;
        }

        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }

        .hero-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
            opacity: 0.15;
            animation: gradientShift 15s ease infinite;
        }

        @keyframes gradientShift {
            0%, 100% { transform: scale(1) rotate(0deg); }
            50% { transform: scale(1.2) rotate(5deg); }
        }

        .hero-content {
            text-align: center;
            z-index: 1;
            padding: 20px;
        }

        .hero h1 {
            font-size: 80px;
            font-weight: 900;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: fadeInUp 1s ease;
        }

        .hero p {
            font-size: 24px;
            margin-bottom: 40px;
            color: #ccc;
            animation: fadeInUp 1s ease 0.2s backwards;
        }

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

        .cta-button {
            display: inline-block;
            padding: 18px 50px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #fff;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 700;
            font-size: 18px;
            transition: all 0.3s;
            animation: fadeInUp 1s ease 0.4s backwards;
            box-shadow: 0 10px 40px rgba(102, 126, 234, 0.4);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 50px rgba(102, 126, 234, 0.6);
        }

        .services {
            padding: 100px 50px;
            background: #0f0f0f;
        }

        .section-title {
            text-align: center;
            font-size: 48px;
            font-weight: 800;
            margin-bottom: 60px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .service-card {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.1) 0%, rgba(118, 75, 162, 0.1) 100%);
            padding: 50px;
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.4s;
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transition: left 0.5s;
        }

        .service-card:hover::before {
            left: 100%;
        }

        .service-card:hover {
            transform: translateY(-10px);
            border-color: rgba(102, 126, 234, 0.5);
            box-shadow: 0 20px 60px rgba(102, 126, 234, 0.3);
        }

        .service-icon {
            font-size: 50px;
            margin-bottom: 20px;
        }

        .service-card h3 {
            font-size: 28px;
            margin-bottom: 15px;
            color: #667eea;
        }

        .service-card p {
            color: #aaa;
            line-height: 1.6;
            font-size: 16px;
        }

        .about {
            padding: 100px 50px;
            background: #0a0a0a;
        }

        .about-content {
            max-width: 900px;
            margin: 0 auto;
            text-align: center;
        }

        .about-content p {
            font-size: 20px;
            line-height: 1.8;
            color: #ccc;
            margin-bottom: 20px;
        }

        .team {
            padding: 100px 50px;
            background: #0f0f0f;
        }

        .team-grid {
            display: flex;
            justify-content: center;
            gap: 40px;
            max-width: 1200px;
            margin: 0 auto;
            flex-wrap: wrap;
        }

        .team-card {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.1) 0%, rgba(118, 75, 162, 0.1) 100%);
            padding: 40px;
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
            max-width: 350px;
            transition: all 0.4s;
        }

        .team-card:hover {
            transform: translateY(-10px);
            border-color: rgba(102, 126, 234, 0.5);
            box-shadow: 0 20px 60px rgba(102, 126, 234, 0.3);
        }

        .team-image-container {
            width: 200px;
            height: 200px;
            margin: 0 auto 25px;
            border-radius: 50%;
            overflow: hidden;
            border: 4px solid #667eea;
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.4);
        }

        .team-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .team-card h3 {
            font-size: 28px;
            margin-bottom: 10px;
            color: #fff;
        }

        .team-role {
            color: #667eea;
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 15px;
        }

        .team-bio {
            color: #aaa;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .twitter-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: #667eea;
            text-decoration: none;
            font-weight: 600;
            padding: 10px 20px;
            border: 2px solid #667eea;
            border-radius: 25px;
            transition: all 0.3s;
        }

        .twitter-link:hover {
            background: #667eea;
            color: #fff;
            transform: translateY(-2px);
        }

        .contact {
            padding: 100px 50px;
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.05) 0%, rgba(118, 75, 162, 0.05) 100%);
            text-align: center;
        }

        .contact-button {
            display: inline-block;
            padding: 18px 50px;
            background: transparent;
            color: #667eea;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 700;
            font-size: 18px;
            border: 2px solid #667eea;
            transition: all 0.3s;
            margin-top: 20px;
        }

        .contact-button:hover {
            background: #667eea;
            color: #fff;
            transform: translateY(-3px);
        }

        footer {
            padding: 40px;
            text-align: center;
            background: #050505;
            color: #666;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 48px;
            }
            .hero p {
                font-size: 18px;
            }
            .nav {
                padding: 20px;
            }
            .nav-links {
                gap: 20px;
            }
            .services-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <nav class="nav">
        <div class="logo">BEST CREATORS</div>
        <div class="nav-links">
            <a href="#services">Services</a>
            <a href="#about">About</a>
            <a href="#team">Team</a>
            <a href="#contact">Contact</a>
        </div>
    </nav>

    <section class="hero">
        <div class="hero-bg"></div>
        <div class="hero-content">
            <h1>BEST CREATORS AGENCY</h1>
            <p>Elevating Stories Through Film & Podcast Production</p>
            <a href="#contact" class="cta-button">Start Your Project</a>
        </div>
    </section>

    <section class="services" id="services">
        <h2 class="section-title">Our Services</h2>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">🎬</div>
                <h3>Film Production</h3>
                <p>From concept to screen, we bring your vision to life with cinematic excellence. Our team handles everything from pre-production planning to post-production magic, creating compelling visual stories that resonate.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">🎙️</div>
                <h3>Podcast Production</h3>
                <p>Professional podcast creation from recording to distribution. We provide studio-quality audio production, editing, and strategic content development to help your voice reach and engage your audience.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">✨</div>
                <h3>Content Strategy</h3>
                <p>We craft comprehensive multimedia strategies that amplify your brand across all platforms. Our creative approach ensures your content cuts through the noise and connects with your target audience.</p>
            </div>
        </div>
    </section>

    <section class="about" id="about">
        <h2 class="section-title">About Us</h2>
        <div class="about-content">
            <p>BEST CREATORS AGENCY is a premier multimedia production house dedicated to crafting exceptional content that captivates and inspires. With expertise spanning film and podcast production, we're passionate about bringing stories to life.</p>
            <p>Our team of creative professionals combines technical excellence with artistic vision, delivering content that doesn't just meet expectations—it exceeds them. Whether you're launching a new podcast series or producing your next film project, we're here to make it extraordinary.</p>
        </div>
    </section>

    <section class="team" id="team">
        <h2 class="section-title">Meet The Team</h2>
        <div class="team-grid">
            <div class="team-card">
                <div class="team-image-container">
                    <img src="https://i.postimg.cc/zvHxLxqg/theophilus.jpg" alt="Theophilus Asare" class="team-image">
                </div>
                <h3>Theophilus Asare</h3>
                <p class="team-role">Creative Director & CEO</p>
                <p class="team-bio">Visionary leader driving creative excellence and strategic innovation in multimedia production.</p>
                <a href="https://x.com/timecommuter" target="_blank" class="twitter-link">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/>
                    </svg>
                    @timecommuter
                </a>
            </div>
        </div>
    </section>

    <section class="contact" id="contact">
        <h2 class="section-title">Let's Create Together</h2>
        <p style="color: #ccc; font-size: 20px; max-width: 700px; margin: 0 auto;">Ready to bring your multimedia project to life? Get in touch with our team and let's discuss how we can help you create something amazing.</p>
        <a href="mailto:info@bestcreatorsagency.com" class="contact-button">Get In Touch</a>
    </section>

    <footer>
        <p>&copy; 2025 BEST CREATORS AGENCY. All rights reserved.</p>
    </footer>
</body>
</html>
