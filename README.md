        }

        /* Reset et styles de base */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--light-color);
            background-color: var(--dark-color);
            overflow-x: hidden;
        }

        a {
            text-decoration: none;
            color: var(--secondary-color);
            transition: var(--transition);
        }

        a:hover {
            color: var(--accent-color);
        }

        ul {
            list-style: none;
        }

        img {
            max-width: 100%;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        .section {
            padding: 100px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }

        .section-title h2 {
            font-size: 2.8rem;
            margin-bottom: 20px;
            color: var(--light-color);
            background: linear-gradient(to right, var(--secondary-color), var(--accent-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .section-title p {
            color: var(--gray-color);
            max-width: 700px;
            margin: 0 auto;
            font-size: 1.1rem;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            border-radius: 2px;
        }

        .btn {
            display: inline-block;
            padding: 14px 32px;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            border: none;
            border-radius: var(--border-radius);
            cursor: pointer;
            font-weight: 600;
            transition: var(--transition);
            text-align: center;
            font-size: 1rem;
            box-shadow: 0 4px 15px rgba(0, 159, 253, 0.3);
        }

        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 159, 253, 0.4);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--secondary-color);
            color: var(--secondary-color);
            box-shadow: none;
        }

        .btn-outline:hover {
            background: var(--secondary-color);
            color: white;
        }

        .btn-success {
            background: linear-gradient(135deg, var(--success-color), #00aa66);
        }

        .btn-warning {
            background: linear-gradient(135deg, var(--warning-color), #ff8800);
        }

        .glass-effect {
            background: rgba(42, 42, 114, 0.15);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: var(--border-radius);
        }

        /* Header */
        header {
            background-color: rgba(18, 18, 18, 0.95);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            display: flex;
            align-items: center;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--light-color);
        }

        .logo span {
            background: linear-gradient(to right, var(--secondary-color), var(--accent-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .nav-links {
            display: flex;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            color: var(--light-color);
            font-weight: 500;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--secondary-color);
            transition: var(--transition);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .auth-buttons {
            display: flex;
            gap: 15px;
        }

        .hamburger {
            display: none;
            cursor: pointer;
            font-size: 1.5rem;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, rgba(18, 18, 18, 0.9), rgba(42, 42, 114, 0.7)), 
                        url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%232a2a72"/><path d="M0 0L100 100M100 0L0 100" stroke="%23009ffd" stroke-width="1"/></svg>');
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            align-items: center;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(0, 159, 253, 0.1) 0%, rgba(18, 18, 18, 0) 70%);
            animation: pulse 8s infinite alternate;
        }

        @keyframes pulse {
            0% { transform: scale(0.8); opacity: 0.5; }
            100% { transform: scale(1.2); opacity: 0.8; }
        }

        .hero-content {
            max-width: 900px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }

        .hero h1 {
            font-size: 3.8rem;
            margin-bottom: 25px;
            line-height: 1.2;
            background: linear-gradient(to right, var(--light-color), var(--accent-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 40px;
            color: var(--gray-color);
        }

        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
        }

        /* Features Section */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }

        .feature-card {
            background: rgba(42, 42, 114, 0.15);
            border-radius: var(--border-radius);
            padding: 35px 30px;
            text-align: center;
            transition: var(--transition);
            border: 1px solid rgba(0, 159, 253, 0.1);
            position: relative;
            overflow: hidden;
        }

        .feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
            border-color: var(--secondary-color);
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 25px;
            display: inline-block;
            width: 80px;
            height: 80px;
            line-height: 80px;
            border-radius: 50%;
            background: rgba(0, 159, 253, 0.1);
        }

        .feature-card h3 {
            margin-bottom: 15px;
            font-size: 1.6rem;
        }

        .feature-card p {
            color: var(--gray-color);
        }

        /* Live Streaming Section */
        .live-streaming {
            background-color: var(--darker-color);
            position: relative;
        }

        .stream-container {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 30px;
            align-items: start;
        }

        .stream-main {
            background: rgba(42, 42, 114, 0.2);
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: var(--box-shadow);
        }

        .stream-video {
            width: 100%;
            height: 400px;
            background: linear-gradient(135deg, var(--primary-color), var(--darker-color));
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
        }

        .live-indicator {
            position: absolute;
            top: 20px;
            left: 20px;
            background: var(--danger-color);
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .live-indicator::before {
            content: '';
            width: 10px;
            height: 10px;
            background: white;
            border-radius: 50%;
            animation: pulse-live 1.5s infinite;
        }

        @keyframes pulse-live {
            0% { opacity: 1; }
            50% { opacity: 0.5; }
            100% { opacity: 1; }
        }

        .stream-info {
            padding: 20px;
        }

        .stream-title {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }

        .stream-instructor {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 15px;
        }

        .instructor-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--secondary-color);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }

        .stream-stats {
            display: flex;
            gap: 20px;
            margin-bottom: 20px;
        }

        .stat {
            display: flex;
            align-items: center;
            gap: 5px;
            color: var(--gray-color);
        }

        .upcoming-streams {
            background: rgba(42, 42, 114, 0.15);
            border-radius: var(--border-radius);
            padding: 25px;
        }

        .upcoming-title {
            font-size: 1.3rem;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .stream-list {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .stream-item {
            display: flex;
            gap: 15px;
            padding: 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: var(--border-radius);
            transition: var(--transition);
        }

        .stream-item:hover {
            background: rgba(255, 255, 255, 0.1);
        }

        .stream-time {
            background: var(--primary-color);
            color: white;
            padding: 8px 12px;
            border-radius: var(--border-radius);
            text-align: center;
            min-width: 70px;
        }

        .stream-details h4 {
            margin-bottom: 5px;
        }

        .stream-details p {
            color: var(--gray-color);
            font-size: 0.9rem;
        }

        /* Authentication System */
        .auth-system {
            background: linear-gradient(135deg, var(--darker-color), var(--primary-color));
        }

        .auth-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .auth-illustration {
            text-align: center;
        }

        .auth-cards {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .auth-card {
            background: rgba(42, 42, 114, 0.2);
            border-radius: var(--border-radius);
            padding: 30px;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .auth-card:hover {
            transform: translateY(-5px);
            border-color: var(--secondary-color);
        }

        .auth-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .auth-card p {
            color: var(--gray-color);
            margin-bottom: 20px;
        }

        .auth-features {
            margin-top: 20px;
        }

        .auth-features li {
            padding: 8px 0;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .auth-features li::before {
            content: '✓';
            color: var(--success-color);
            font-weight: bold;
        }

        /* Dashboard Preview */
        .dashboard-preview {
            background-color: var(--darker-color);
        }

        .dashboard-container {
            background: rgba(42, 42, 114, 0.15);
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: var(--box-shadow);
        }

        .dashboard-header {
            background: rgba(42, 42, 114, 0.3);
            padding: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .dashboard-nav {
            display: flex;
            gap: 20px;
        }

        .dashboard-nav a {
            color: var(--light-color);
            font-weight: 500;
        }

        .dashboard-content {
            display: grid;
            grid-template-columns: 250px 1fr;
            min-height: 400px;
        }

        .dashboard-sidebar {
            background: rgba(42, 42, 114, 0.2);
            padding: 20px;
            border-right: 1px solid rgba(255, 255, 255, 0.1);
        }

        .sidebar-menu {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .sidebar-menu a {
            padding: 12px 15px;
            border-radius: var(--border-radius);
            color: var(--light-color);
            transition: var(--transition);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .sidebar-menu a:hover, .sidebar-menu a.active {
            background: rgba(0, 159, 253, 0.2);
            color: var(--secondary-color);
        }

        .dashboard-main {
            padding: 30px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .stat-card {
            background: rgba(42, 42, 114, 0.2);
            border-radius: var(--border-radius);
            padding: 20px;
            text-align: center;
            transition: var(--transition);
        }

        .stat-card:hover {
            transform: translateY(-5px);
            background: rgba(42, 42, 114, 0.3);
        }

        .stat-value {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 10px;
            background: linear-gradient(to right, var(--secondary-color), var(--accent-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .stat-label {
            color: var(--gray-color);
            font-size: 0.9rem;
        }

        /* Contact Section */
        .contact {
            background: linear-gradient(135deg, var(--primary-color), var(--darker-color));
        }

        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
        }

        .contact-info h3 {
            margin-bottom: 20px;
            font-size: 1.8rem;
        }

        .contact-info p {
            margin-bottom: 30px;
            color: rgba(255, 255, 255, 0.8);
        }

        .contact-details {
            margin-top: 30px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
            gap: 15px;
        }

        .contact-item i {
            font-size: 1.2rem;
            color: var(--secondary-color);
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
        }

        .contact-form {
            background: rgba(255, 255, 255, 0.05);
            padding: 40px;
            border-radius: var(--border-radius);
            backdrop-filter: blur(10px);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }

        .form-control {
            width: 100%;
            padding: 15px;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: var(--border-radius);
            color: var(--light-color);
            transition: var(--transition);
            font-size: 1rem;
        }

        .form-control:focus {
            outline: none;
            border-color: var(--secondary-color);
            background: rgba(255, 255, 255, 0.15);
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background-color: var(--darker-color);
            padding: 80px 0 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 50px;
        }

        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 25px;
            color: var(--light-color);
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            color: var(--gray-color);
            transition: var(--transition);
        }

        .footer-links a:hover {
            color: var(--secondary-color);
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
            width: 45px;
            height: 45px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 50%;
            transition: var(--transition);
            font-size: 1.2rem;
        }

        .social-links a:hover {
            background: var(--secondary-color);
            transform: translateY(-5px);
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--gray-color);
            font-size: 0.9rem;
        }

        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            z-index: 2000;
            align-items: center;
            justify-content: center;
            backdrop-filter: blur(5px);
        }

        .modal-content {
            background: var(--darker-color);
            width: 90%;
            max-width: 500px;
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5);
            animation: modalAppear 0.3s ease;
        }

        @keyframes modalAppear {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }

        .modal-header {
            background: var(--primary-color);
            padding: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .modal-header h3 {
            margin: 0;
        }

        .close-modal {
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        .modal-body {
            padding: 30px;
        }

        .form-options {
            display: flex;
            margin-bottom: 20px;
            border-radius: var(--border-radius);
            overflow: hidden;
            background: rgba(255, 255, 255, 0.05);
        }

        .form-option {
            flex: 1;
            text-align: center;
            padding: 12px;
            cursor: pointer;
            transition: var(--transition);
        }

        .form-option.active {
            background: var(--secondary-color);
        }

        /* Responsive Design */
        @media (max-width: 1200px) {
            .hero h1 {
                font-size: 3.2rem;
            }
            
            .section-title h2 {
                font-size: 2.4rem;
            }
        }

        @media (max-width: 992px) {
            .hero h1 {
                font-size: 2.8rem;
            }
            
            .stream-container {
                grid-template-columns: 1fr;
            }
            
            .auth-container {
                grid-template-columns: 1fr;
            }
            
            .dashboard-content {
                grid-template-columns: 1fr;
            }
            
            .dashboard-sidebar {
                display: none;
            }
        }

        @media (max-width: 768px) {
            .navbar {
                padding: 15px 0;
            }
            
            .nav-links, .auth-buttons {
                display: none;
            }
            
            .hamburger {
                display: block;
            }
            
            .mobile-menu {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 70px);
                background: var(--darker-color);
                flex-direction: column;
                align-items: center;
                justify-content: flex-start;
                padding-top: 50px;
                transition: var(--transition);
                z-index: 999;
            }
            
            .mobile-menu.active {
                left: 0;
            }
            
            .mobile-menu li {
                margin: 20px 0;
            }
            
            .mobile-auth {
                margin-top: 30px;
                display: flex;
                flex-direction: column;
                gap: 15px;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .hero-buttons .btn {
                width: 80%;
                margin-bottom: 15px;
            }
            
            .section {
                padding: 70px 0;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }

        @media (max-width: 576px) {
            .hero h1 {
                font-size: 1.9rem;
            }
            
            .section-title h2 {
                font-size: 1.8rem;
            }
            
            .feature-card, .auth-card {
                padding: 25px 20px;
            }
            
            .contact-form {
                padding: 25px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav class="navbar">
                <a href="#" class="logo">GUERRAOUI <span>ABDERRAZEK</span></a>
                <ul class="nav-links">
                    <li><a href="#accueil">Accueil</a></li>
                    <li><a href="#fonctionnalites">Fonctionnalités</a></li>
                    <li><a href="#live">Cours en Direct</a></li>
                    <li><a href="#auth">Comptes</a></li>
                    <li><a href="#dashboard">Tableau de Bord</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <div class="auth-buttons">
                    <a href="#" class="btn btn-outline" id="loginBtn">Connexion</a>
                    <a href="#" class="btn" id="registerBtn">Inscription</a>
                </div>
                <div class="hamburger" id="hamburger">
                    ☰
                </div>
            </nav>
        </div>
    </header>

    <!-- Mobile Menu -->
    <div class="mobile-menu" id="mobileMenu">
        <ul>
            <li><a href="#accueil">Accueil</a></li>
            <li><a href="#fonctionnalites">Fonctionnalités</a></li>
            <li><a href="#live">Cours en Direct</a></li>
            <li><a href="#auth">Comptes</a></li>
            <li><a href="#dashboard">Tableau de Bord</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
        <div class="mobile-auth">
            <a href="#" class="btn btn-outline" id="mobileLoginBtn">Connexion</a>
            <a href="#" class="btn" id="mobileRegisterBtn">Inscription</a>
        </div>
    </div>

    <!-- Hero Section -->
    <section class="hero" id="accueil">
        <div class="container">
            <div class="hero-content">
                <h1>Plateforme Éducative Intelligente et Interactive</h1>
                <p>Découvrez une expérience d'apprentissage révolutionnaire avec des cours en direct, un système de gestion complet et des outils collaboratifs avancés.</p>
                <div class="hero-buttons">
                    <a href="#auth" class="btn">Commencer Maintenant</a>
                    <a href="#live" class="btn btn-outline">Voir un Cours en Direct</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="section" id="fonctionnalites">
        <div class="container">
            <div class="section-title">
                <h2>Fonctionnalités Avancées</h2>
                <p>Notre plateforme intègre les dernières technologies pour une expérience d'apprentissage optimale</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">🔐</div>
                    <h3>Authentification Multi-niveaux</h3>
                    <p>Système de connexion sécurisé avec rôles distincts pour étudiants, enseignants et administrateurs.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🎥</div>
                    <h3>Classes Virtuelles en Direct</h3>
                    <p>Interagissez en temps réel avec vos enseignants et camarades via notre système de vidéoconférence intégré.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">📚</div>
                    <h3>Gestion Avancée des Cours</h3>
                    <p>Créez, organisez et suivez vos cours avec des outils de gestion de contenu puissants et intuitifs.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🧠</div>
                    <h3>Évaluations Intelligentes</h3>
                    <p>Quiz interactifs, examens chronométrés et système de notation automatique avec analyses détaillées.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🏆</div>
                    <h3>Certificats Personnalisés</h3>
                    <p>Générez automatiquement des certificats de réussite avec vérification en ligne pour chaque cours complété.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">📊</div>
                    <h3>Tableaux de Bord Analytics</h3>
                    <p>Suivez vos progrès et performances avec des visualisations de données avancées et rapports détaillés.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">💬</div>
                    <h3>Espace Collaboratif</h3>
                    <p>Forums de discussion, messagerie instantanée et partage de fichiers pour une collaboration optimale.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">📱</div>
                    <h3>Application Mobile</h3>
                    <p>Accédez à tous les contenus et fonctionnalités depuis votre smartphone avec nos applications natives.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Live Streaming Section -->
    <section class="section live-streaming" id="live">
        <div class="container">
            <div class="section-title">
                <h2>Cours en Direct</h2>
                <p>Participez à des sessions d'apprentissage interactives en temps réel avec nos experts</p>
            </div>
            <div class="stream-container">
                <div class="stream-main">
                    <div class="stream-video">
                        <div class="live-indicator">EN DIRECT</div>
                        <div style="font-size: 1.5rem; color: white; text-align: center;">
                            🎥 Diffusion en direct<br>
                            <small style="font-size: 1rem; opacity: 0.8;">Rejoignez la session pour interagir</small>
                        </div>
                    </div>
                    <div class="stream-info">
                        <h3 class="stream-title">Introduction à l'Intelligence Artificielle</h3>
                        <div class="stream-instructor">
                            <div class="instructor-avatar">PD</div>
                            <div>
                                <div>Dr. Pierre Dubois</div>
                                <div style="font-size: 0.9rem; color: var(--gray-color);">Expert en IA</div>
                            </div>
                        </div>
                        <div class="stream-stats">
                            <div class="stat">👁️ 245 spectateurs</div>
                            <div class="stat">💬 89 messages</div>
                            <div class="stat">⏱️ 45:32 durée</div>
                        </div>
                        <p>Explorez les fondamentaux de l'intelligence artificielle, du machine learning et des réseaux de neurones dans cette session interactive.</p>
                        <a href="#" class="btn" style="margin-top: 20px;">Rejoindre le Cours</a>
                    </div>
                </div>
                <div class="upcoming-streams">
                    <h3 class="upcoming-title">Prochaines Sessions</h3>
                    <div class="stream-list">
                        <div class="stream-item">
                            <div class="stream-time">
                                <div>14:00</div>
                                <div style="font-size: 0.8rem;">Aujourd'hui</div>
                            </div>
                            <div class="stream-details">
                                <h4>Mathématiques Avancées</h4>
                                <p>Dr. Sophie Martin</p>
                            </div>
                        </div>
                        <div class="stream-item">
                            <div class="stream-time">
                                <div>16:30</div>
                                <div style="font-size: 0.8rem;">Aujourd'hui</div>
                            </div>
                            <div class="stream-details">
                                <h4>Histoire de l'Art Moderne</h4>
                                <p>Prof. Jean Lefebvre</p>
                            </div>
                        </div>
                        <div class="stream-item">
                            <div class="stream-time">
                                <div>09:00</div>
                                <div style="font-size: 0.8rem;">Demain</div>
                            </div>
                            <div class="stream-details">
                                <h4>Programmation Python</h4>
                                <p>Dr. Marie Curie</p>
                            </div>
                        </div>
                        <div class="stream-item">
                            <div class="stream-time">
                                <div>11:00</div>
                                <div style="font-size: 0.8rem;">Demain</div>
                            </div>
                            <div class="stream-details">
                                <h4>Chimie Organique</h4>
                                <p>Prof. Alain Petit</p>
                            </div>
                        </div>
                    </div>
                    <a href="#" class="btn btn-outline" style="width: 100%; margin-top: 20px;">Voir tout le programme</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Authentication System -->
    <section class="section auth-system" id="auth">
        <div class="container">
            <div class="section-title">
                <h2>Comptes Personnalisés</h2>
                <p>Choisissez le type de compte qui correspond à votre profil et accédez à des fonctionnalités adaptées</p>
            </div>
            <div class="auth-container">
                <div class="auth-illustration">
                    <div style="font-size: 5rem; margin-bottom: 20px;">👨‍🎓👩‍🏫</div>
                    <h3>Une plateforme pour tous les acteurs de l'éducation</h3>
                    <p style="color: var(--gray-color); margin-top: 15px;">Que vous soyez étudiant, enseignant ou administrateur, notre système s'adapte à vos besoins spécifiques.</p>
                </div>
                <div class="auth-cards">
                    <div class="auth-card">
                        <h3><span>🎓</span> Compte Étudiant</h3>
                        <p>Accédez à tous les cours, participez aux sessions en direct, soumettez vos travaux et suivez vos progrès.</p>
                        <ul class="auth-features">
                            <li>Accès à tous les cours et ressources</li>
                            <li>Participation aux classes virtuelles en direct</li>
                            <li>Soumission de travaux et devoirs</li>
                            <li>Suivi détaillé de la progression</li>
                            <li>Certificats de réussite</li>
                            <li>Interaction avec les enseignants et autres étudiants</li>
                        </ul>
                        <a href="#" class="btn btn-outline" style="margin-top: 20px;">Créer un compte étudiant</a>
                    </div>
                    <div class="auth-card">
                        <h3><span>👩‍🏫</span> Compte Enseignant</h3>
                        <p>Créez et gérez vos cours, animez des sessions en direct, évaluez les étudiants et analysez les performances.</p>
                        <ul class="auth-features">
                            <li>Création et gestion de cours</li>
                            <li>Animation de classes virtuelles en direct</li>
                            <li>Évaluation et notation des étudiants</li>
                            <li>Outils d'analyse des performances</li>
                            <li>Communication avec les étudiants</li>
                            <li>Génération de rapports détaillés</li>
                        </ul>
                        <a href="#" class="btn" style="margin-top: 20px;">Créer un compte enseignant</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Dashboard Preview -->
    <section class="section dashboard-preview" id="dashboard">
        <div class="container">
            <div class="section-title">
                <h2>Tableau de Bord Intelligent</h2>
                <p>Interface centralisée pour gérer tous les aspects de votre expérience éducative</p>
            </div>
            <div class="dashboard-container">
                <div class="dashboard-header">
                    <div class="logo">Tableau de Bord <span>Étudiant</span></div>
                    <div class="dashboard-nav">
                        <a href="#">Cours</a>
                        <a href="#">Calendrier</a>
                        <a href="#">Messages</a>
                        <a href="#">Paramètres</a>
                    </div>
                </div>
                <div class="dashboard-content">
                    <div class="dashboard-sidebar">
                        <div class="sidebar-menu">
                            <a href="#" class="active">📊 Aperçu</a>
                            <a href="#">📚 Mes Cours</a>
                            <a href="#">🗓️ Calendrier</a>
                            <a href="#">📝 Devoirs</a>
                            <a href="#">🏆 Certificats</a>
                            <a href="#">💬 Discussions</a>
                            <a href="#">⚙️ Paramètres</a>
                        </div>
                    </div>
                    <div class="dashboard-main">
                        <div class="stat-card">
                            <div class="stat-value">12</div>
                            <div class="stat-label">Cours Actifs</div>
                        </div>
                        <div class="stat-card">
                            <div class="stat-value">87%</div>
                            <div class="stat-label">Progression Moyenne</div>
                        </div>
                        <div class="stat-card">
                            <div class="stat-value">5</div>
                            <div class="stat-label">Devoirs en Attente</div>
                        </div>
                        <div class="stat-card">
                            <div class="stat-value">3</div>
                            <div class="stat-label">Sessions Aujourd'hui</div>
                        </div>
                        <div class="stat-card">
                            <div class="stat-value">24</div>
                            <div class="stat-label">Heures Cette Semaine</div>
                        </div>
                        <div class="stat-card">
                            <div class="stat-value">8</div>
                            <div class="stat-label">Certificats Obtenus</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="section contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contactez-Nous</h2>
                <p>Notre équipe est à votre disposition pour répondre à toutes vos questions</p>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Prêt à transformer l'éducation ?</h3>
                    <p>Que vous soyez un établissement éducatif, un enseignant indépendant ou un étudiant motivé, nous avons la solution adaptée à vos besoins.</p>
                    <div class="contact-details">
                        <div class="contact-item">
                            <i>📍</i>
                            <span>123 Avenue de l'Éducation, 75000 Paris, France</span>
                        </div>
                        <div class="contact-item">
                            <i>📞</i>
                            <span>+33 1 23 45 67 89</span>
                        </div>
                        <div class="contact-item">
                            <i>✉️</i>
                            <span>contact@guerraoui-abderrazek.com</span>
                        </div>
                        <div class="contact-item">
                            <i>🕒</i>
                            <span>Lun - Ven: 9h00 - 18h00</span>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Nom complet</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Adresse email</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Sujet</label>
                            <input type="text" id="subject" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" class="form-control" required></textarea>
                        </div>
                        <button type="submit" class="btn" style="width: 100%;">Envoyer le message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>GUERRAOUI ABDERRAZEK</h3>
                    <p>Plateforme éducative innovante pour l'apprentissage en ligne de qualité, avec des fonctionnalités avancées et une expérience utilisateur exceptionnelle.</p>
                    <div class="social-links">
                        <a href="#"><span>📘</span></a>
                        <a href="#"><span>🐦</span></a>
                        <a href="#"><span>📷</span></a>
                        <a href="#"><span>💼</span></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Liens rapides</h3>
                    <ul class="footer-links">
                        <li><a href="#accueil">Accueil</a></li>
                        <li><a href="#fonctionnalites">Fonctionnalités</a></li>
                        <li><a href="#live">Cours en Direct</a></li>
                        <li><a href="#auth">Comptes</a></li>
                        <li><a href="#dashboard">Tableau de Bord</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Ressources</h3>
                    <ul class="footer-links">
                        <li><a href="#">Centre d'aide</a></li>
                        <li><a href="#">Documentation</a></li>
                        <li><a href="#">Tutoriels vidéo</a></li>
                        <li><a href="#">Blog éducatif</a></li>
                        <li><a href="#">Témoignages</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Légal</h3>
                    <ul class="footer-links">
                        <li><a href="#">Conditions d'utilisation</a></li>
                        <li><a href="#">Politique de confidentialité</a></li>
                        <li><a href="#">Mentions légales</a></li>
                        <li><a href="#">Cookies</a></li>
                        <li><a href="#">Accessibilité</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 GUERRAOUI ABDERRAZEK. Tous droits réservés.</p>
            </div>
        </div>
    </footer>

    <!-- Login Modal -->
    <div class="modal" id="loginModal">
        <div class="modal-content">
            <div class="modal-header">
                <h3>Connexion à votre compte</h3>
                <button class="close-modal">&times;</button>
            </div>
            <div class="modal-body">
                <div class="form-options">
                    <div class="form-option active" data-role="student">Étudiant</div>
                    <div class="form-option" data-role="teacher">Enseignant</div>
                    <div class="form-option" data-role="admin">Administrateur</div>
                </div>
                <form id="loginForm">
                    <div class="form-group">
                        <label for="loginEmail">Adresse email</label>
                        <input type="email" id="loginEmail" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="loginPassword">Mot de passe</label>
                        <input type="password" id="loginPassword" class="form-control" required>
                    </div>
                    <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                        <div>
                            <input type="checkbox" id="rememberMe">
                            <label for="rememberMe">Se souvenir de moi</label>
                        </div>
                        <a href="#" style="font-size: 0.9rem;">Mot de passe oublié ?</a>
                    </div>
                    <button type="submit" class="btn" style="width: 100%;">Se connecter</button>
                </form>
                <div style="text-align: center; margin-top: 20px; color: var(--gray-color);">
                    Pas encore de compte ? <a href="#" id="switchToRegister">S'inscrire</a>
                </div>
            </div>
        </div>
    </div>

    <!-- Register Modal -->
    <div class="modal" id="registerModal">
        <div class="modal-content">
            <div class="modal-header">
                <h3>Créer un nouveau compte</h3>
                <button class="close-modal">&times;</button>
            </div>
            <div class="modal-body">
                <div class="form-options">
                    <div class="form-option active" data-role="student">Étudiant</div>
                    <div class="form-option" data-role="teacher">Enseignant</div>
                </div>
                <form id="registerForm">
                    <div class="form-group">
                        <label for="registerName">Nom complet</label>
                        <input type="text" id="registerName" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="registerEmail">Adresse email</label>
                        <input type="email" id="registerEmail" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="registerPassword">Mot de passe</label>
                        <input type="password" id="registerPassword" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="registerConfirmPassword">Confirmer le mot de passe</label>
                        <input type="password" id="registerConfirmPassword" class="form-control" required>
                    </div>
                    <div style="margin-bottom: 20px;">
                        <input type="checkbox" id="acceptTerms" required>
                        <label for="acceptTerms">J'accepte les <a href="#">conditions d'utilisation</a> et la <a href="#">politique de confidentialité</a></label>
                    </div>
                    <button type="submit" class="btn" style="width: 100%;">Créer mon compte</button>
                </form>
                <div style="text-align: center; margin-top: 20px; color: var(--gray-color);">
                    Déjà un compte ? <a href="#" id="switchToLogin">Se connecter</a>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Menu mobile
        document.getElementById('hamburger').addEventListener('click', function() {
            document.getElementById('mobileMenu').classList.toggle('active');
        });

        // Fermer le menu mobile en cliquant sur un lien
        document.querySelectorAll('.mobile-menu a').forEach(link => {
            link.addEventListener('click', function() {
                document.getElementById('mobileMenu').classList.remove('active');
            });
        });

        // Animation au défilement
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.backgroundColor = 'rgba(18, 18, 18, 0.98)';
                header.style.backdropFilter = 'blur(10px)';
            } else {
                header.style.backgroundColor = 'rgba(18, 18, 18, 0.95)';
                header.style.backdropFilter = 'none';
            }
        });

        // Gestion des modales
        const loginModal = document.getElementById('loginModal');
        const registerModal = document.getElementById('registerModal');
        const loginBtn = document.getElementById('loginBtn');
        const registerBtn = document.getElementById('registerBtn');
        const mobileLoginBtn = document.getElementById('mobileLoginBtn');
        const mobileRegisterBtn = document.getElementById('mobileRegisterBtn');
        const closeModals = document.querySelectorAll('.close-modal');
        const switchToRegister = document.getElementById('switchToRegister');
        const switchToLogin = document.getElementById('switchToLogin');

        function openModal(modal) {
            modal.style.display = 'flex';
            document.body.style.overflow = 'hidden';
        }

        function closeModal(modal) {
            modal.style.display = 'none';
            document.body.style.overflow = 'auto';
        }

        loginBtn.addEventListener('click', function(e) {
            e.preventDefault();
            openModal(loginModal);
        });

        registerBtn.addEventListener('click', function(e) {
            e.preventDefault();
            openModal(registerModal);
        });

        mobileLoginBtn.addEventListener('click', function(e) {
            e.preventDefault();
            openModal(loginModal);
            document.getElementById('mobileMenu').classList.remove('active');
        });

        mobileRegisterBtn.addEventListener('click', function(e) {
            e.preventDefault();
            openModal(registerModal);
            document.getElementById('mobileMenu').classList.remove('active');
        });

        closeModals.forEach(btn => {
            btn.addEventListener('click', function() {
                closeModal(loginModal);
                closeModal(registerModal);
            });
        });

        switchToRegister.addEventListener('click', function(e) {
            e.preventDefault();
            closeModal(loginModal);
            openModal(registerModal);
        });

        switchToLogin.addEventListener('click', function(e) {
            e.preventDefault();
            closeModal(registerModal);
            openModal(loginModal);
        });

        // Fermer les modales en cliquant à l'extérieur
        window.addEventListener('click', function(e) {
            if (e.target === loginModal) {
                closeModal(loginModal);
            }
            if (e.target === registerModal) {
                closeModal(registerModal);
            }
        });

        // Gestion des formulaires
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Connexion réussie ! Redirection vers votre tableau de bord...');
            closeModal(loginModal);
        });

        document.getElementById('registerForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Inscription réussie ! Un email de confirmation vous a été envoyé.');
            closeModal(registerModal);
        });

        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Merci pour votre message ! Nous vous répondrons dans les plus brefs délais.');
            this.reset();
        });

        // Changer le type de compte dans les formulaires
        document.querySelectorAll('.form-option').forEach(option => {
            option.addEventListener('click', function() {
                // Retirer la classe active de toutes les options
                this.parentElement.querySelectorAll('.form-option').forEach(opt => {
                    opt.classList.remove('active');
                });
                // Ajouter la classe active à l'option cliquée
                this.classList.add('active');
            });
        });

        // Animation des cartes au défilement
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observer les cartes de fonctionnalités
        document.querySelectorAll('.feature-card').forEach(card => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(20px)';
            card.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
            observer.observe(card);
        });

        // Observer les cartes d'authentification
        document.querySelectorAll('.auth-card').forEach(card => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(20px)';
            card.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
            observer.observe(card);
        });
    </script>
</body>
</html>
