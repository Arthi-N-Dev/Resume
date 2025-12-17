<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arthi N — Software Engineer</title>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --cream: #faf8f5;
            --warm-white: #fffdf9;
            --sand: #f5f0e8;
            --terracotta: #c9553d;
            --terracotta-light: #e07860;
            --charcoal: #2d2d2d;
            --slate: #5a5a5a;
            --muted: #8a8a8a;
            --border: #e8e4dc;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; }

        body {
            font-family: 'Inter', sans-serif;
            background: var(--cream);
            color: var(--charcoal);
            line-height: 1.7;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 1.5rem 3rem;
            background: rgba(250, 248, 245, 0.95);
            backdrop-filter: blur(10px);
            z-index: 100;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid var(--border);
        }

        .nav-logo {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.75rem;
            font-weight: 600;
            color: var(--charcoal);
            letter-spacing: -0.5px;
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--slate);
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 500;
            letter-spacing: 0.5px;
            transition: color 0.3s;
        }

        .nav-links a:hover { color: var(--terracotta); }

        /* Hero */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 120px 3rem 80px;
            background: linear-gradient(180deg, var(--warm-white) 0%, var(--cream) 100%);
        }

        .hero-container {
            max-width: 1300px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1.2fr 1fr;
            gap: 6rem;
            align-items: center;
        }

        .hero-content { animation: fadeIn 1s ease-out; }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .hero-intro {
            font-size: 0.85rem;
            font-weight: 600;
            color: var(--terracotta);
            letter-spacing: 3px;
            text-transform: uppercase;
            margin-bottom: 1.5rem;
        }

        .hero-name {
            font-family: 'Cormorant Garamond', serif;
            font-size: 5rem;
            font-weight: 600;
            line-height: 1.05;
            color: var(--charcoal);
            margin-bottom: 1.5rem;
            letter-spacing: -2px;
        }

        .hero-tagline {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.75rem;
            font-weight: 400;
            color: var(--slate);
            font-style: italic;
            margin-bottom: 2rem;
        }

        .hero-desc {
            font-size: 1.05rem;
            color: var(--slate);
            max-width: 520px;
            margin-bottom: 2.5rem;
        }

        .hero-cta {
            display: flex;
            gap: 1rem;
        }

        .btn {
            padding: 1rem 2rem;
            font-size: 0.9rem;
            font-weight: 600;
            letter-spacing: 0.5px;
            border-radius: 4px;
            text-decoration: none;
            transition: all 0.3s;
            cursor: pointer;
            border: none;
        }

        .btn-primary {
            background: var(--terracotta);
            color: white;
        }

        .btn-primary:hover {
            background: var(--terracotta-light);
            transform: translateY(-2px);
        }

        .btn-outline {
            background: transparent;
            color: var(--charcoal);
            border: 2px solid var(--charcoal);
        }

        .btn-outline:hover {
            background: var(--charcoal);
            color: white;
        }

        /* Profile Card */
        .hero-visual {
            animation: fadeIn 1s ease-out 0.3s both;
        }

        .profile-card {
            background: white;
            border-radius: 16px;
            padding: 3rem;
            box-shadow: 0 30px 60px rgba(0,0,0,0.08);
            position: relative;
        }

        .profile-card::before {
            content: '';
            position: absolute;
            top: -8px;
            left: -8px;
            right: -8px;
            bottom: -8px;
            border: 2px solid var(--terracotta);
            border-radius: 20px;
            opacity: 0.2;
        }

        .avatar-wrapper {
            width: 140px;
            height: 140px;
            margin: 0 auto 1.5rem;
            position: relative;
        }

        .avatar {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--terracotta), var(--terracotta-light));
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: 'Cormorant Garamond', serif;
            font-size: 3.5rem;
            font-weight: 600;
            color: white;
        }

        .status-dot {
            position: absolute;
            bottom: 8px;
            right: 8px;
            width: 24px;
            height: 24px;
            background: #22c55e;
            border: 4px solid white;
            border-radius: 50%;
        }

        .profile-name {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.75rem;
            font-weight: 600;
            text-align: center;
            margin-bottom: 0.25rem;
        }

        .profile-title {
            text-align: center;
            color: var(--muted);
            font-size: 0.9rem;
            margin-bottom: 2rem;
        }

        .profile-info {
            display: flex;
            flex-direction: column;
            gap: 0.75rem;
        }

        .info-row {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            padding: 0.75rem 1rem;
            background: var(--sand);
            border-radius: 8px;
            font-size: 0.9rem;
            color: var(--slate);
        }

        .info-row svg {
            width: 18px;
            height: 18px;
            fill: var(--terracotta);
            flex-shrink: 0;
        }

        /* Stats Section */
        .stats-section {
            padding: 5rem 3rem;
            background: white;
            border-top: 1px solid var(--border);
            border-bottom: 1px solid var(--border);
        }

        .stats-container {
            max-width: 1100px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 2rem;
        }

        .stat-item {
            text-align: center;
            padding: 1.5rem;
        }

        .stat-value {
            font-family: 'Cormorant Garamond', serif;
            font-size: 3.5rem;
            font-weight: 600;
            color: var(--terracotta);
            line-height: 1;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 0.85rem;
            color: var(--muted);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Section Styles */
        section {
            padding: 6rem 3rem;
            max-width: 1100px;
            margin: 0 auto;
        }

        .section-header {
            margin-bottom: 3.5rem;
        }

        .section-tag {
            font-size: 0.8rem;
            font-weight: 600;
            color: var(--terracotta);
            letter-spacing: 3px;
            text-transform: uppercase;
            margin-bottom: 0.75rem;
        }

        .section-title {
            font-family: 'Cormorant Garamond', serif;
            font-size: 3rem;
            font-weight: 600;
            color: var(--charcoal);
            letter-spacing: -1px;
        }

        /* Skills */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
        }

        .skill-card {
            background: white;
            border: 1px solid var(--border);
            border-radius: 12px;
            padding: 2rem;
            transition: all 0.3s;
        }

        .skill-card:hover {
            border-color: var(--terracotta);
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            transform: translateY(-4px);
        }

        .skill-header {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.25rem;
        }

        .skill-icon {
            width: 48px;
            height: 48px;
            background: var(--sand);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .skill-icon svg {
            width: 24px;
            height: 24px;
            fill: var(--terracotta);
        }

        .skill-name {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.5rem;
            font-weight: 600;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .skill-tag {
            padding: 0.4rem 0.9rem;
            background: var(--sand);
            border-radius: 20px;
            font-size: 0.85rem;
            color: var(--slate);
        }

        /* Experience */
        .experience-list {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        .exp-card {
            background: white;
            border: 1px solid var(--border);
            border-radius: 12px;
            padding: 2.5rem;
            transition: all 0.3s;
        }

        .exp-card:hover {
            border-color: var(--terracotta);
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
        }

        .exp-top {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 0.5rem;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .exp-company {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.75rem;
            font-weight: 600;
        }

        .exp-period {
            font-size: 0.85rem;
            color: var(--terracotta);
            font-weight: 600;
            padding: 0.5rem 1rem;
            background: rgba(201, 85, 61, 0.1);
            border-radius: 20px;
        }

        .exp-role {
            color: var(--muted);
            font-size: 1rem;
            margin-bottom: 1.5rem;
        }

        .exp-highlights {
            list-style: none;
        }

        .exp-highlights li {
            position: relative;
            padding-left: 1.5rem;
            margin-bottom: 0.75rem;
            color: var(--slate);
            font-size: 0.95rem;
        }

        .exp-highlights li::before {
            content: '—';
            position: absolute;
            left: 0;
            color: var(--terracotta);
            font-weight: 600;
        }

        /* Projects */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1.5rem;
        }

        .project-card {
            background: white;
            border: 1px solid var(--border);
            border-radius: 12px;
            padding: 2rem;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, var(--terracotta), var(--terracotta-light));
            transform: scaleX(0);
            transition: transform 0.3s;
        }

        .project-card:hover::before { transform: scaleX(1); }

        .project-card:hover {
            border-color: var(--terracotta);
            transform: translateY(-4px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.08);
        }

        .project-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--terracotta), var(--terracotta-light));
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1.25rem;
        }

        .project-icon svg {
            width: 26px;
            height: 26px;
            fill: white;
        }

        .project-name {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.35rem;
            font-weight: 600;
            margin-bottom: 0.75rem;
        }

        .project-desc {
            font-size: 0.9rem;
            color: var(--slate);
            margin-bottom: 1rem;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.4rem;
        }

        .project-tag {
            font-size: 0.75rem;
            padding: 0.3rem 0.6rem;
            background: var(--sand);
            border-radius: 4px;
            color: var(--muted);
        }

        /* Education */
        .edu-card {
            background: white;
            border: 1px solid var(--border);
            border-radius: 12px;
            padding: 2.5rem;
            display: flex;
            align-items: center;
            gap: 2rem;
            max-width: 700px;
        }

        .edu-icon {
            width: 80px;
            height: 80px;
            background: var(--sand);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
        }

        .edu-icon svg {
            width: 36px;
            height: 36px;
            fill: var(--terracotta);
        }

        .edu-content h4 {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 0.25rem;
        }

        .edu-content p {
            color: var(--slate);
        }

        .edu-content .year {
            display: inline-block;
            margin-top: 0.5rem;
            font-size: 0.85rem;
            color: var(--terracotta);
            font-weight: 600;
        }

        /* Contact */
        .contact-section {
            background: var(--charcoal);
            padding: 6rem 3rem;
            margin-top: 4rem;
        }

        .contact-container {
            max-width: 900px;
            margin: 0 auto;
            text-align: center;
        }

        .contact-title {
            font-family: 'Cormorant Garamond', serif;
            font-size: 3.5rem;
            font-weight: 600;
            color: white;
            margin-bottom: 1rem;
            letter-spacing: -1px;
        }

        .contact-subtitle {
            color: rgba(255,255,255,0.6);
            font-size: 1.1rem;
            margin-bottom: 2.5rem;
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .contact-link {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            padding: 1rem 1.5rem;
            background: rgba(255,255,255,0.1);
            border: 1px solid rgba(255,255,255,0.2);
            border-radius: 8px;
            color: white;
            text-decoration: none;
            transition: all 0.3s;
        }

        .contact-link:hover {
            background: var(--terracotta);
            border-color: var(--terracotta);
        }

        .contact-link svg {
            width: 20px;
            height: 20px;
            fill: currentColor;
        }

        /* Footer */
        footer {
            background: var(--charcoal);
            padding: 2rem 3rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            text-align: center;
        }

        footer p {
            color: rgba(255,255,255,0.4);
            font-size: 0.9rem;
        }

        /* Responsive */
        @media (max-width: 1024px) {
            .hero-container { grid-template-columns: 1fr; gap: 3rem; }
            .hero-name { font-size: 3.5rem; }
            .stats-container { grid-template-columns: repeat(2, 1fr); }
            .projects-grid { grid-template-columns: repeat(2, 1fr); }
        }

        @media (max-width: 768px) {
            nav { padding: 1rem 1.5rem; }
            .nav-links { display: none; }
            .hero { padding: 100px 1.5rem 60px; }
            .hero-name { font-size: 2.75rem; }
            .hero-tagline { font-size: 1.35rem; }
            section { padding: 4rem 1.5rem; }
            .section-title { font-size: 2.25rem; }
            .skills-grid { grid-template-columns: 1fr; }
            .projects-grid { grid-template-columns: 1fr; }
            .stats-container { grid-template-columns: repeat(2, 1fr); gap: 1rem; }
            .stat-value { font-size: 2.5rem; }
            .edu-card { flex-direction: column; text-align: center; }
            .contact-title { font-size: 2.5rem; }
        }

        @media (max-width: 480px) {
            .hero-cta { flex-direction: column; }
            .btn { width: 100%; text-align: center; }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-logo">Arthi N</div>
        <ul class="nav-links">
            <li><a href="#about">About</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#experience">Experience</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Hero -->
    <section class="hero" id="about">
        <div class="hero-container">
            <div class="hero-content">
                <p class="hero-intro">Software Engineer</p>
                <h1 class="hero-name">Arthi N</h1>
                <p class="hero-tagline">Building elegant digital experiences</p>
                <p class="hero-desc">
                    Results-driven Full Stack Developer with 2.7+ years crafting enterprise applications. 
                    I specialize in Angular, .NET Core & SQL — delivering solutions that boost performance by 70% 
                    and transform complex business needs into intuitive software.
                </p>
                <div class="hero-cta">
                    <a href="mailto:arthinithi09@gmail.com" class="btn btn-primary">Get In Touch</a>
                    <a href="#projects" class="btn btn-outline">View Projects</a>
                </div>
            </div>
            <div class="hero-visual">
                <div class="profile-card">
                    <div class="avatar-wrapper">
                        <div class="avatar">AN</div>
                        <div class="status-dot"></div>
                    </div>
                    <h3 class="profile-name">Arthi N</h3>
                    <p class="profile-title">Full Stack Developer • Chennai</p>
                    <div class="profile-info">
                        <div class="info-row">
                            <svg viewBox="0 0 24 24"><path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/></svg>
                            +91 9629182486
                        </div>
                        <div class="info-row">
                            <svg viewBox="0 0 24 24"><path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
                            arthinithi09@gmail.com
                        </div>
                        <div class="info-row">
                            <svg viewBox="0 0 24 24"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg>
                            Chennai, India
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats -->
    <section class="stats-section">
        <div class="stats-container">
            <div class="stat-item">
                <div class="stat-value">2.7+</div>
                <div class="stat-label">Years Experience</div>
            </div>
            <div class="stat-item">
                <div class="stat-value">70%</div>
                <div class="stat-label">Performance Boost</div>
            </div>
            <div class="stat-item">
                <div class="stat-value">90%</div>
                <div class="stat-label">Faster Resolution</div>
            </div>
            <div class="stat-item">
                <div class="stat-value">3+</div>
                <div class="stat-label">Major Projects</div>
            </div>
        </div>
    </section>

    <!-- Skills -->
    <section id="skills">
        <div class="section-header">
            <p class="section-tag">Expertise</p>
            <h2 class="section-title">Technical Skills</h2>
        </div>
        <div class="skills-grid">
            <div class="skill-card">
                <div class="skill-header">
                    <div class="skill-icon">
                        <svg viewBox="0 0 24 24"><path d="M9.4 16.6L4.8 12l4.6-4.6L8 6l-6 6 6 6 1.4-1.4zm5.2 0l4.6-4.6-4.6-4.6L16 6l6 6-6 6-1.4-1.4z"/></svg>
                    </div>
                    <h4 class="skill-name">Frontend</h4>
                </div>
                <div class="skill-tags">
                    <span class="skill-tag">Angular 14+</span>
                    <span class="skill-tag">TypeScript</span>
                    <span class="skill-tag">HTML5</span>
                    <span class="skill-tag">CSS3</span>
                    <span class="skill-tag">PrimeNG</span>
                </div>
            </div>
            <div class="skill-card">
                <div class="skill-header">
                    <div class="skill-icon">
                        <svg viewBox="0 0 24 24"><path d="M20 3H4c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm0 16H4V5h16v14z"/></svg>
                    </div>
                    <h4 class="skill-name">Backend</h4>
                </div>
                <div class="skill-tags">
                    <span class="skill-tag">.NET Core</span>
                    <span class="skill-tag">C#</span>
                    <span class="skill-tag">REST APIs</span>
                    <span class="skill-tag">Entity Framework</span>
                </div>
            </div>
            <div class="skill-card">
                <div class="skill-header">
                    <div class="skill-icon">
                        <svg viewBox="0 0 24 24"><path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-7 14c-3.31 0-6-2.69-6-6s2.69-6 6-6 6 2.69 6 6-2.69 6-6 6z"/></svg>
                    </div>
                    <h4 class="skill-name">Database</h4>
                </div>
                <div class="skill-tags">
                    <span class="skill-tag">SQL Server</span>
                    <span class="skill-tag">MySQL</span>
                    <span class="skill-tag">Stored Procedures</span>
                    <span class="skill-tag">Optimization</span>
                </div>
            </div>
            <div class="skill-card">
                <div class="skill-header">
                    <div class="skill-icon">
                        <svg viewBox="0 0 24 24"><path d="M17 1.01L7 1c-1.1 0-2 .9-2 2v18c0 1.1.9 2 2 2h10c1.1 0 2-.9 2-2V3c0-1.1-.9-1.99-2-1.99zM17 19H7V5h10v14z"/></svg>
                    </div>
                    <h4 class="skill-name">Mobile</h4>
                </div>
                <div class="skill-tags">
                    <span class="skill-tag">Android</span>
                    <span class="skill-tag">Kotlin</span>
                    <span class="skill-tag">Flutter</span>
                    <span class="skill-tag">Play Store</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience -->
    <section id="experience">
        <div class="section-header">
            <p class="section-tag">Career</p>
            <h2 class="section-title">Work Experience</h2>
        </div>
        <div class="experience-list">
            <div class="exp-card">
                <div class="exp-top">
                    <h4 class="exp-company">Leiten Info Tech</h4>
                    <span class="exp-period">May 2023 – Present</span>
                </div>
                <p class="exp-role">Software Engineer – Full Stack Developer • Chennai</p>
                <ul class="exp-highlights">
                    <li>Develop enterprise web applications using Angular with .NET Core backend</li>
                    <li>Achieved 70% improvement in application performance through optimization</li>
                    <li>Reduced client issue resolution time by 90% within two months</li>
                    <li>Implemented 15% more efficient database solutions with optimized queries</li>
                    <li>Published Android application independently on Google Play Store</li>
                </ul>
            </div>
            <div class="exp-card">
                <div class="exp-top">
                    <h4 class="exp-company">Leiten Info Tech</h4>
                    <span class="exp-period">Jan 2023 – May 2023</span>
                </div>
                <p class="exp-role">Software Development Intern • Chennai</p>
                <ul class="exp-highlights">
                    <li>Gained hands-on experience in full-stack development with Angular & .NET</li>
                    <li>Contributed to live projects and production deployments</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Projects -->
    <section id="projects">
        <div class="section-header">
            <p class="section-tag">Portfolio</p>
            <h2 class="section-title">Key Projects</h2>
        </div>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-icon">
                    <svg viewBox="0 0 24 24"><path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-5 14H7v-2h7v2zm3-4H7v-2h10v2zm0-4H7V7h10v2z"/></svg>
                </div>
                <h4 class="project-name">Manufacturing ERP</h4>
                <p class="project-desc">End-to-end ERP covering Material, Purchase, Production, Quality, Sales, Accounts & MIS modules.</p>
                <div class="project-tags">
                    <span class="project-tag">Angular</span>
                    <span class="project-tag">.NET</span>
                    <span class="project-tag">SQL</span>
                </div>
            </div>
            <div class="project-card">
                <div class="project-icon">
                    <svg viewBox="0 0 24 24"><path d="M22.7 19l-9.1-9.1c.9-2.3.4-5-1.5-6.9-2-2-5-2.4-7.4-1.3L9 6 6 9 1.6 4.7C.4 7.1.9 10.1 2.9 12.1c1.9 1.9 4.6 2.4 6.9 1.5l9.1 9.1c.4.4 1 .4 1.4 0l2.3-2.3c.5-.4.5-1.1.1-1.4z"/></svg>
                </div>
                <h4 class="project-name">Maintenance System</h4>
                <p class="project-desc">TMS with Breakdown, Job Cards, Preventive Maintenance, MTBF/MTTR analytics & cost tracking.</p>
                <div class="project-tags">
                    <span class="project-tag">Angular</span>
                    <span class="project-tag">Charts</span>
                    <span class="project-tag">Reports</span>
                </div>
            </div>
            <div class="project-card">
                <div class="project-icon">
                    <svg viewBox="0 0 24 24"><path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/></svg>
                </div>
                <h4 class="project-name">Visitor Management</h4>
                <p class="project-desc">Check-in/out system with scheduling, Firebase notifications & automated email reporting.</p>
                <div class="project-tags">
                    <span class="project-tag">Firebase</span>
                    <span class="project-tag">Notifications</span>
                    <span class="project-tag">Email</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Education -->
    <section id="education">
        <div class="section-header">
            <p class="section-tag">Education</p>
            <h2 class="section-title">Academic Background</h2>
        </div>
        <div class="edu-card">
            <div class="edu-icon">
                <svg viewBox="0 0 24 24"><path d="M5 13.18v4L12 21l7-3.82v-4L12 17l-7-3.82zM12 3L1 9l11 6 9-4.91V17h2V9L12 3z"/></svg>
            </div>
            <div class="edu-content">
                <h4>B.E. in Electronics & Communication</h4>
                <p>Anna University, Chennai</p>
                <span class="year">2016 – 2020</span>
            </div>
        </div>
    </section>

    <!-- Contact -->
    <section class="contact-section" id="contact">
        <div class="contact-container">
            <h2 class="contact-title">Let's Work Together</h2>
            <p class="contact-subtitle">I'm open to new opportunities and exciting projects</p>
            <div class="contact-links">
                <a href="mailto:arthinithi09@gmail.com" class="contact-link">
                    <svg viewBox="0 0 24 24"><path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
                    arthinithi09@gmail.com
                </a>
                <a href="tel:+919629182486" class="contact-link">
                    <svg viewBox="0 0 24 24"><path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/></svg>
                    +91 9629182486
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>© 2024 Arthi N — Crafted with care</p>
    </footer>
</body>
</html>
