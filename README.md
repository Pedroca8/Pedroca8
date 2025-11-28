## Hi there 👋

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu GitHub Aprimorado</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #2d333b;
            --secondary-color: #22272e;
            --accent-color: #539bf5;
            --text-color: #adbac7;
            --border-color: #444c56;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--primary-color);
            color: var(--text-color);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header com vídeo */
        .header {
            position: relative;
            height: 400px;
            overflow: hidden;
            border-bottom: 1px solid var(--border-color);
        }
        
        .video-container {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
        }
        
        .video-container video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .video-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
            z-index: 2;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
        }
        
        .profile-image {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 4px solid var(--accent-color);
            margin-bottom: 20px;
            object-fit: cover;
        }
        
        .profile-name {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: white;
        }
        
        .profile-bio {
            font-size: 1.2rem;
            max-width: 600px;
        }
        
        /* Seções principais */
        .section {
            padding: 60px 0;
            border-bottom: 1px solid var(--border-color);
        }
        
        .section-title {
            font-size: 2rem;
            margin-bottom: 30px;
            color: white;
            text-align: center;
        }
        
        /* Tecnologias */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .tech-card {
            background-color: var(--secondary-color);
            border-radius: 8px;
            padding: 20px;
            text-align: center;
            transition: transform 0.3s ease;
            border: 1px solid var(--border-color);
        }
        
        .tech-card:hover {
            transform: translateY(-5px);
            border-color: var(--accent-color);
        }
        
        .tech-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
            color: var(--accent-color);
        }
        
        .tech-name {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: white;
        }
        
        /* Estatísticas */
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .stat-card {
            background-color: var(--secondary-color);
            border-radius: 8px;
            padding: 30px 20px;
            text-align: center;
            border: 1px solid var(--border-color);
        }
        
        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            color: var(--accent-color);
            margin-bottom: 10px;
        }
        
        .stat-label {
            font-size: 1.1rem;
        }
        
        /* Projetos */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .project-card {
            background-color: var(--secondary-color);
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid var(--border-color);
            transition: transform 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            border-color: var(--accent-color);
        }
        
        .project-image {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-title {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: white;
        }
        
        .project-description {
            margin-bottom: 15px;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 15px;
        }
        
        .tech-tag {
            background-color: rgba(83, 155, 245, 0.2);
            color: var(--accent-color);
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.85rem;
        }
        
        .project-links {
            display: flex;
            gap: 15px;
        }
        
        .project-link {
            color: var(--accent-color);
            text-decoration: none;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .project-link:hover {
            text-decoration: underline;
        }
        
        /* Contato */
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
        }
        
        .contact-link {
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--text-color);
            text-decoration: none;
            font-size: 1.1rem;
            transition: color 0.3s ease;
        }
        
        .contact-link:hover {
            color: var(--accent-color);
        }
        
        .contact-icon {
            font-size: 1.5rem;
        }
        
        /* Footer */
        .footer {
            padding: 30px 0;
            text-align: center;
            color: var(--text-color);
            font-size: 0.9rem;
        }
        
        /* Responsividade */
        @media (max-width: 768px) {
            .header {
                height: 300px;
            }
            
            .profile-image {
                width: 100px;
                height: 100px;
            }
            
            .profile-name {
                font-size: 1.8rem;
            }
            
            .profile-bio {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header com vídeo -->
    <header class="header">
        <div class="video-container">
            <video autoplay muted loop>
                <source src="https://assets.mixkit.co/videos/preview/mixkit-abstract-background-with-moving-lines-176-large.mp4" type="video/mp4">
                Seu navegador não suporta vídeos HTML5.
            </video>
        </div>
        <div class="video-overlay">
            <img src="https://avatars.githubusercontent.com/u/1?v=4" alt="Foto de perfil" class="profile-image">
            <h1 class="profile-name">Seu Nome</h1>
            <p class="profile-bio">Desenvolvedor Full Stack | Apaixonado por tecnologia e inovação</p>
        </div>
    </header>

    <div class="container">
        <!-- Seção de Tecnologias -->
        <section class="section" id="technologies">
            <h2 class="section-title">Tecnologias que Domino</h2>
            <div class="tech-grid">
                <div class="tech-card">
                    <i class="fab fa-js-square tech-icon"></i>
                    <h3 class="tech-name">JavaScript</h3>
                    <p>ES6+, Node.js, Express</p>
                </div>
                <div class="tech-card">
                    <i class="fab fa-python tech-icon"></i>
                    <h3 class="tech-name">Python</h3>
                    <p>Django, Flask, Data Science</p>
                </div>
                <div class="tech-card">
                    <i class="fab fa-react tech-icon"></i>
                    <h3 class="tech-name">React</h3>
                    <p>Hooks, Context API, Redux</p>
                </div>
                <div class="tech-card">
                    <i class="fab fa-html5 tech-icon"></i>
                    <h3 class="tech-name">HTML & CSS</h3>
                    <p>Responsive Design, Flexbox, Grid</p>
                </div>
                <div class="tech-card">
                    <i class="fab fa-git-alt tech-icon"></i>
                    <h3 class="tech-name">Git & GitHub</h3>
                    <p>Versionamento, CI/CD, Actions</p>
                </div>
                <div class="tech-card">
                    <i class="fas fa-database tech-icon"></i>
                    <h3 class="tech-name">Banco de Dados</h3>
                    <p>MySQL, MongoDB, PostgreSQL</p>
                </div>
            </div>
        </section>

        <!-- Seção de Estatísticas -->
        <section class="section" id="stats">
            <h2 class="section-title">Minhas Estatísticas</h2>
            <div class="stats-container">
                <div class="stat-card">
                    <div class="stat-number">1,254</div>
                    <div class="stat-label">Commits no Total</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">42</div>
                    <div class="stat-label">Repositórios</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">18</div>
                    <div class="stat-label">Projetos Concluídos</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">3</div>
                    <div class="stat-label">Anos de Experiência</div>
                </div>
            </div>
        </section>

        <!-- Seção de Projetos -->
        <section class="section" id="projects">
            <h2 class="section-title">Projetos em Destaque</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <img src="https://images.unsplash.com/photo-1555066931-4365d14bab8c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="Projeto 1" class="project-image">
                    <div class="project-content">
                        <h3 class="project-title">Sistema de E-commerce</h3>
                        <p class="project-description">Plataforma completa de e-commerce com carrinho de compras, pagamentos e painel administrativo.</p>
                        <div class="project-tech">
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">Node.js</span>
                            <span class="tech-tag">MongoDB</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="project-link"><i class="fab fa-github"></i> Código</a>
                            <a href="#" class="project-link"><i class="fas fa-external-link-alt"></i> Demo</a>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="Projeto 2" class="project-image">
                    <div class="project-content">
                        <h3 class="project-title">App de Finanças Pessoais</h3>
                        <p class="project-description">Aplicativo para controle de gastos e orçamentos pessoais com gráficos e relatórios.</p>
                        <div class="project-tech">
                            <span class="tech-tag">React Native</span>
                            <span class="tech-tag">Firebase</span>
                            <span class="tech-tag">Chart.js</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="project-link"><i class="fab fa-github"></i> Código</a>
                            <a href="#" class="project-link"><i class="fas fa-external-link-alt"></i> Demo</a>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <img src="https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1074&q=80" alt="Projeto 3" class="project-image">
                    <div class="project-content">
                        <h3 class="project-title">Plataforma de Cursos Online</h3>
                        <p class="project-description">Sistema de gerenciamento de cursos com videoaulas, exercícios e certificados.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Django</span>
                            <span class="tech-tag">PostgreSQL</span>
                            <span class="tech-tag">AWS S3</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="project-link"><i class="fab fa-github"></i> Código</a>
                            <a href="#" class="project-link"><i class="fas fa-external-link-alt"></i> Demo</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Seção de Contato -->
        <section class="section" id="contact">
            <h2 class="section-title">Entre em Contato</h2>
            <div class="contact-links">
                <a href="https://github.com/seu-usuario" class="contact-link">
                    <i class="fab fa-github contact-icon"></i>
                    GitHub
                </a>
                <a href="https://linkedin.com/in/seu-perfil" class="contact-link">
                    <i class="fab fa-linkedin contact-icon"></i>
                    LinkedIn
                </a>
                <a href="mailto:seu-email@exemplo.com" class="contact-link">
                    <i class="fas fa-envelope contact-icon"></i>
                    E-mail
                </a>
                <a href="https://twitter.com/seu-usuario" class="contact-link">
                    <i class="fab fa-twitter contact-icon"></i>
                    Twitter
                </a>
            </div>
        </section>
    </div>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <p>&copy; 2023 Seu Nome. Todos os direitos reservados.</p>
        </div>
    </footer>

    <script>
        // Efeito de contagem animada para as estatísticas
        document.addEventListener('DOMContentLoaded', function() {
            const statNumbers = document.querySelectorAll('.stat-number');
            
            statNumbers.forEach(stat => {
                const target = parseInt(stat.textContent);
                let current = 0;
                const increment = target / 100;
                const timer = setInterval(() => {
                    current += increment;
                    if (current >= target) {
                        stat.textContent = target.toLocaleString();
                        clearInterval(timer);
                    } else {
                        stat.textContent = Math.floor(current).toLocaleString();
                    }
                }, 20);
            });
        });
    </script>
</body>
</html>
