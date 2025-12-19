<!DOCTYPE html>
<html lang="pt-AO">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AptiMail | Impulso Profissional e Branding</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        /* --- VARIÁVEIS --- */
        :root {
            --primary-blue: #0f172a; 
            --accent-blue: #3b82f6;  
            --light-gray: #f8f9fa;   
            --white: #ffffff;
            --text-dark: #333333;
            --text-light: #d1d5db;
            --transition: all 0.3s ease;
        }

        /* --- RESET --- */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; }
        body {
            font-family: 'Poppins', sans-serif;
            color: var(--text-dark);
            background-color: var(--light-gray);
            line-height: 1.6;
            overflow-x: hidden;
        }
        a { text-decoration: none; color: inherit; }
        ul { list-style: none; }

        /* --- HEADER --- */
        header {
            background-color: var(--primary-blue);
            color: var(--white);
            padding: 1rem 5%;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .logo { font-size: 1.5rem; font-weight: 700; letter-spacing: 1px; }
        .logo span { color: var(--accent-blue); }

        .nav-links { display: flex; gap: 2rem; }
        .nav-links a { font-size: 0.95rem; font-weight: 500; transition: var(--transition); }
        .nav-links a:hover { color: var(--accent-blue); }

        .hamburger { display: none; cursor: pointer; font-size: 1.5rem; }

        /* --- HERO SECTION --- */
        #home {
            height: 100vh;
            background: linear-gradient(rgba(15, 23, 42, 0.85), rgba(15, 23, 42, 0.7)), 
                        url('https://images.unsplash.com/photo-1497366216548-37526070297c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: var(--white);
            padding: 0 20px;
        }

        #home h1 { font-size: 3rem; margin-bottom: 1rem; animation: fadeInDown 1s ease; }
        #home p {
            font-size: 1.2rem; margin-bottom: 2rem; color: var(--text-light);
            max-width: 600px; animation: fadeInUp 1s ease 0.3s forwards; opacity: 0;
        }

        .cta-button {
            padding: 12px 30px;
            background-color: var(--accent-blue);
            color: var(--white);
            font-weight: 600;
            border-radius: 5px;
            transition: var(--transition);
            border: 2px solid var(--accent-blue);
            animation: fadeInUp 1s ease 0.6s forwards; opacity: 0;
        }
        .cta-button:hover { background-color: transparent; color: var(--accent-blue); }

        /* --- SEÇÕES GERAIS --- */
        section { padding: 5rem 10%; }
        .section-title {
            text-align: center; font-size: 2.2rem; margin-bottom: 3rem;
            color: var(--primary-blue); position: relative;
        }
        .section-title::after {
            content: ''; width: 60px; height: 3px; background-color: var(--accent-blue);
            position: absolute; bottom: -10px; left: 50%; transform: translateX(-50%);
        }

        /* --- HISTÓRIA --- */
        #historia { background-color: var(--white); }
        .history-content { display: grid; grid-template-columns: 1fr 1fr; gap: 3rem; align-items: center; }
        .values-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1rem; margin-top: 2rem; }
        .value-box {
            background: var(--light-gray); padding: 1rem; border-radius: 8px;
            text-align: center; box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        .value-box i { color: var(--accent-blue); font-size: 1.5rem; margin-bottom: 0.5rem; }
        .founder-card {
            background: var(--primary-blue); color: var(--white); padding: 2rem;
            border-radius: 10px; text-align: center; box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        /* --- SERVIÇOS --- */
        #servicos { background-color: var(--light-gray); }
        .services-grid {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 2rem;
        }
        .service-card {
            background: var(--white); padding: 2rem; border-radius: 10px; text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05); transition: var(--transition);
            border-bottom: 3px solid transparent;
        }
        .service-card:hover { transform: translateY(-10px); border-bottom: 3px solid var(--accent-blue); }
        .service-icon { font-size: 2.5rem; color: var(--primary-blue); margin-bottom: 1.5rem; }
        .price-tag {
            display: inline-block; margin-top: 1rem; padding: 5px 15px;
            background-color: rgba(59, 130, 246, 0.1); color: var(--accent-blue);
            font-weight: 700; border-radius: 20px;
        }

        /* --- NOVO DESIGN DE CONTATO (SIMPLIFICADO) --- */
        #contato { background-color: var(--white); text-align: center; }
        
        .contact-minimalist {
            max-width: 800px;
            margin: 0 auto;
        }

        .contact-minimalist p {
            margin-bottom: 2.5rem;
            color: #555;
            font-size: 1.1rem;
        }

        .action-buttons {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            flex-wrap: wrap;
        }

        .btn-contact {
            padding: 15px 35px;
            border-radius: 50px;
            font-size: 1rem;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: var(--transition);
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .btn-whatsapp {
            background-color: #25D366;
            color: #fff;
            border: 2px solid #25D366;
        }
        
        .btn-whatsapp:hover {
            background-color: #fff;
            color: #25D366;
            transform: translateY(-3px);
        }

        .btn-email {
            background-color: var(--primary-blue);
            color: #fff;
            border: 2px solid var(--primary-blue);
        }

        .btn-email:hover {
            background-color: #fff;
            color: var(--primary-blue);
            transform: translateY(-3px);
        }

        /* --- FOOTER --- */
        footer { background-color: var(--primary-blue); color: var(--white); padding: 2rem 5%; text-align: center; }
        .social-icons { margin: 1.5rem 0; }
        .social-icons a { color: var(--white); font-size: 1.2rem; margin: 0 10px; transition: var(--transition); }
        .social-icons a:hover { color: var(--accent-blue); }
        .footer-bottom { border-top: 1px solid rgba(255,255,255,0.1); padding-top: 1rem; font-size: 0.8rem; color: var(--text-light); }

        /* --- ANIMAÇÕES --- */
        .reveal { opacity: 0; transform: translateY(30px); transition: all 0.8s ease-out; }
        .reveal.active { opacity: 1; transform: translateY(0); }
        @keyframes fadeInDown { from { opacity: 0; transform: translateY(-30px); } to { opacity: 1; transform: translateY(0); } }
        @keyframes fadeInUp { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }

        /* --- RESPONSIVIDADE --- */
        @media (max-width: 768px) {
            .hamburger { display: block; }
            .nav-links {
                position: absolute; top: 70px; right: 0; width: 100%;
                background-color: var(--primary-blue); flex-direction: column;
                align-items: center; padding: 2rem 0; transform: translateY(-150%);
                transition: var(--transition);
            }
            .nav-links.nav-active { transform: translateY(0); box-shadow: 0 5px 10px rgba(0,0,0,0.1); }
            #home h1 { font-size: 2rem; }
            .history-content, .values-grid { grid-template-columns: 1fr; }
            .founder-card { margin-top: 2rem; }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">Apti<span>Mail</span></div>
        <nav>
            <ul class="nav-links">
                <li><a href="#home">Início</a></li>
                <li><a href="#historia">Nossa História</a></li>
                <li><a href="#servicos">Serviços</a></li>
                <li><a href="#contato">Contato</a></li>
            </ul>
        </nav>
        <div class="hamburger">
            <i class="fas fa-bars"></i>
        </div>
    </header>

    <section id="home">
        <h1>Impulsione a sua imagem profissional</h1>
        <p>A AptiMail é a sua parceira estratégica na construção de uma marca pessoal forte e competitiva no mercado.</p>
        <a href="#servicos" class="cta-button">Ver Preços</a>
    </section>

    <section id="historia">
        <h2 class="section-title reveal">Quem Somos</h2>
        <div class="history-content reveal">
            <div class="history-text">
                <h3>Origem e Propósito</h3>
                <p>A AptiMail nasceu da necessidade de destacar talentos num mercado de trabalho cada vez mais competitivo. Fundada para transformar carreiras através de um branding pessoal de excelência.</p>
                <div class="values-grid">
                    <div class="value-box">
                        <i class="fas fa-bullseye"></i>
                        <h4>Missão</h4>
                    </div>
                    <div class="value-box">
                        <i class="fas fa-eye"></i>
                        <h4>Visão</h4>
                    </div>
                    <div class="value-box">
                        <i class="fas fa-gem"></i>
                        <h4>Valores</h4>
                    </div>
                </div>
            </div>
            <div class="founder-card reveal">
                <i class="fas fa-user-tie" style="font-size: 3rem; margin-bottom: 1rem;"></i>
                <h3>Ednário Teixeira Nhenga</h3>
                <p>Cofundador</p>
                <hr style="margin: 1rem 0; opacity: 0.3;">
                <p style="font-size: 0.9rem;">"A nossa marca é o seu sucesso."</p>
            </div>
        </div>
    </section>

    <section id="servicos">
        <h2 class="section-title reveal">Nossos Serviços</h2>
        <div class="services-grid">
            
            <div class="service-card reveal">
                <div class="service-icon"><i class="fas fa-file-alt"></i></div>
                <h3>Currículo Profissional</h3>
                <p>Estruturação e design moderno para destacar as suas competências.</p>
                <span class="price-tag">A partir de 500 Kz</span>
            </div>

            <div class="service-card reveal">
                <div class="service-icon"><i class="fas fa-pen-fancy"></i></div>
                <h3>Cartas Profissionais</h3>
                <p>Apresentação, Pedidos de Estágio e Cartas de Motivação.</p>
                <span class="price-tag">Desde 1.000 Kz</span>
            </div>

            <div class="service-card reveal">
                <div class="service-icon"><i class="fas fa-bezier-curve"></i></div>
                <h3>Logótipos Profissionais</h3>
                <p>Identidade visual única e impactante para a sua marca.</p>
                <span class="price-tag">Sob Consulta</span>
            </div>

            <div class="service-card reveal">
                <div class="service-icon"><i class="fas fa-chalkboard-teacher"></i></div>
                <h3>Consultoria</h3>
                <p>Análise de carreira e orientação personalizada.</p>
                <span class="price-tag">Sob Consulta</span>
            </div>

            <div class="service-card reveal">
                <div class="service-icon"><i class="fas fa-briefcase"></i></div>
                <h3>Portfólios</h3>
                <p>Apresentação visual dos seus melhores trabalhos.</p>
                <span class="price-tag">Sob Consulta</span>
            </div>

            <div class="service-card reveal">
                <div class="service-icon"><i class="fas fa-share-alt"></i></div>
                <h3>Gestão de Marca</h3>
                <p>Estratégia para posicionamento online.</p>
                <span class="price-tag">Sob Consulta</span>
            </div>

        </div>
    </section>

    <section id="contato">
        <h2 class="section-title reveal">Entre em Contacto</h2>
        <div class="contact-minimalist reveal">
            <p>Pronto para impulsionar a sua carreira? Fale diretamente com a nossa equipa através dos canais abaixo.</p>
            
            <div class="action-buttons">
                <a href="https://wa.me/244950622197" target="_blank" class="btn-contact btn-whatsapp">
                    <i class="fab fa-whatsapp"></i> Conversar no WhatsApp
                </a>
                <a href="mailto:aptimailprofissional@gmail.com" class="btn-contact btn-email">
                    <i class="far fa-envelope"></i> Enviar Email
                </a>
            </div>
        </div>
    </section>

    <footer>
        <div class="logo">Apti<span>Mail</span></div>
        <div class="social-icons">
            <a href="#"><i class="fab fa-facebook-f"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="https://wa.me/244950622197"><i class="fab fa-whatsapp"></i></a>
        </div>
        <div class="footer-bottom">
            &copy; 2025 AptiMail. Todos os direitos reservados.
        </div>
    </footer>

    <script>
        // Menu Hamburger
        const hamburger = document.querySelector('.hamburger');
        const navLinks = document.querySelector('.nav-links');
        const links = document.querySelectorAll('.nav-links li');

        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('nav-active');
            const icon = hamburger.querySelector('i');
            if (navLinks.classList.contains('nav-active')) {
                icon.classList.remove('fa-bars');
                icon.classList.add('fa-times');
            } else {
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
            }
        });

        links.forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('nav-active');
                hamburger.querySelector('i').classList.remove('fa-times');
                hamburger.querySelector('i').classList.add('fa-bars');
            });
        });

        // Scroll Reveal
        const revealElements = document.querySelectorAll('.reveal');
        const revealOnScroll = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                }
            });
        }, { threshold: 0.1 });

        revealElements.forEach(el => revealOnScroll.observe(el));
    </script>
</body>
</html>
