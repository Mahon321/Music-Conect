# Música-conecta
<!DOCTYPE html>
<HTML lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Music Connect - Divulgação Musical</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #121212;
            color: #ffffff;
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, #1DB954, #191414);
            padding: 2rem 0;
             text-align: center; 
        }
        
        .logo {
            font-size: 2.5rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        nav {
            background-color: #191414;
            padding: 1rem 0;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
        }
        
        nav ul li {
            margin: 0 1rem;
        }
        
        nav ul li a {
            color: #ffffff;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: #1DB954;
        }
        
        .hero {
            padding: 4rem 0;
            text-align: center;
            background: url('/api/placeholder/1200/500') center/cover no-repeat;
            position: relative;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 1;
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1.5rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .btn {
            display: inline-block;
            background-color: #1DB954;
            color: #ffffff;
            padding: 0.8rem 2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #18a349;
        }
        
        .releases {
            padding: 4rem 0;
            background-color: #191414;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-size: 2rem;
        }
        
        .releases-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .release-card {
            background-color: #282828;
            border-radius: 8px;
            overflow: hidden;
            transition: transform 0.3s;
        }
        
        .release-card:hover {
            transform: translateY(-10px);
        }
        
        .release-image {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }
        
        .release-info {
            padding: 1.5rem;
        }
        
        .release-title {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }
        
        .release-platforms {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .platform-icon {
            width: 24px;
            height: 24px;
            background-color: #fff;
            border-radius: 50%;
        }
        
        .streams {
            padding: 4rem 0;
        }
        
        .platforms {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .platform {
            background-color: #282828;
            padding: 2rem;
            border-radius: 8px;
            text-align: center;
            width: 180px;
            transition: transform 0.3s;
        }
        
        .platform:hover {
            transform: scale(1.05);
        }
        
        .platform-logo {
            width: 60px;
            height: 60px;
            margin: 0 auto 1rem;
            background-color: #fff;
            border-radius: 12px;
        }
        
        .contact {
            padding: 4rem 0;
            background-color: #191414;
        }
        
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-input, .form-textarea {
            width: 100%;
            padding: 0.8rem;
            border: none;
            border-radius: 4px;
            background-color: #282828;
            color: #ffffff;
        }
        
        .form-textarea {
            resize: vertical;
            min-height: 150px;
        }
        
        .form-submit {
            background-color: #1DB954;
            color: #ffffff;
            border: none;
            padding: 0.8rem 2rem;
            border-radius: 50px;
            font-weight: bold;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .form-submit:hover {
            background-color: #18a349;
        }
        
        footer {
            background-color: #121212;
            padding: 2rem 0;
            text-align: center;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }
        
        .social-icon {
            width: 40px;
            height: 40px;
            background-color: #282828;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: background-color 0.3s;
        }
        
        .social-icon:hover {
            background-color: #1DB954;
        }
        
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            nav ul {
                flex-direction: column;
                align-items: center;
            }
            
            nav ul li {
                margin: 0.5rem 0;
            }
            
            .releases-grid {
                grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="logo">Music Connect</div>
            <p>Conectando sua música com o mundo</p>
        </div>
    </header>
    
    <nav>
        <div class="container">
            <ul>
                <li><a href="#home">Início</a></li>
                <li><a href="#releases">Lançamentos</a></li>
                <li><a href="#streams">Plataformas</a></li>
                <li><a href="#contact">Contato</a></li>
            </ul>
        </div>
    </nav>
    
    <section id="home" class="hero">
        <div class="container hero-content">
            <h1>Divulgação Musical Profissional</h1>
            <p>Distribuímos sua música para todas as plataformas digitais com código DI, ISRC e estudos de audiência para maximizar seu alcance e sucesso.</p>
             <a href="#contact" class="btn">Entre em Contato</a> 
        </div>
    </section>
    
    <section id="releases" class="releases">
        <div class="container">
            <h2 class="section-title">Últimos Lançamentos</h2>
            <div class="releases-grid">
                <div class="release-card">
                    <img src="/api/placeholder/300/300" alt="Capa do Álbum" class="release-image">
                    <div class="release-info">
                        <h3 class="release-title">Nome da Música</h3>
                        <p>Artista</p>
                        <div class="release-platforms">
                            <div class="platform-icon"></div>
                            <div class="platform-icon"></div>
                            <div class="platform-icon"></div>
                        </div>
                    </div>
                </div>
                
                <div class="release-card">
                     <img src="/api/placeholder/300/300" alt="Capa do Álbum" class="release-image"> 
                    <div class="release-info">
                        <h3 class="release-title">Nome da Música</h3>
                        <p>Artista</p>
                        <div class="release-platforms">
                            <div class="platform-icon"></div>
                            <div class="platform-icon"></div>
                            <div class="platform-icon"></div>
                        </div>
                    </div>
                </div>
                
                <div class="release-card">
                     <img src="/api/placeholder/300/300" alt="Capa do Álbum" class="release-image"> 
                    <div class="release-info">
                        <h3 class="release-title">Nome da Música</h3>
                        <p>Artista</p>
                        <div class="release-platforms">
                            <div class="platform-icon"></div>
                            <div class="platform-icon"></div>
                            <div class="platform-icon"></div>
                        </div>
                    </div>
                </div>
                
                <div class="release-card">
                     <img src="/api/placeholder/300/300" alt="Capa do Álbum" class="release-image"> 
                    <div class="release-info">
                        <h3 class="release-title">Nome da Música</h3>
                        <p>Artista</p>
                        <div class="release-platforms">
                            <div class="platform-icon"></div>
                            <div class="platform-icon"></div>
                            <div class="platform-icon"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="streams" class="streams">
        <div class="container">
               <h2 class="section-title">Distribuição em Todas as Plataformas</h2>   
            <div class="platforms">
                <div class="platform">
                    <div class="platform-logo"></div>
                    <h3>Spotify</h3>
                </div>
                
                <div class="platform">
                    <div class="platform-logo"></div>
                    <h3>Apple Music</h3>
                </div>
                
                <div class="platform">
                    <div class="platform-logo"></div>
                    <h3>YouTube Music</h3>
                </div>
                
                <div class="platform">
                    <div class="platform-logo"></div>
                    <h3>Amazon Music</h3>
                </div>
                
                <div class="platform">
                    <div class="platform-logo"></div>
                    <h3>Deezer</h3>
                </div>
                
                <div class="platform">
                    <div class="platform-logo"></div>
                    <h3>TikTok</h3>
                </div>
            </div>
        </div>
    </section>
    
    <section id="contact" class="contact">
        <div class="container">
                  <h2 class="section-title">Entre em Contato</h2>      
               <form class="contact-form">   
                <div class="form-group">
                    <label for="name" class="form-label">Nome</label>
                    <input type="text" id="name" class="form-input" required>
                </div>
                
                <div class="form-group">
                    <label for="email" class="form-label">Email</label>
                    <input type="email" id="email" class="form-input" required>
                </div>
                
                <div class="form-group">
                            <label for="subject" class="form-label">Assunto</label>        
                    <input type="text" id="subject" class="form-input" required>
                </div>
                
     <div class="form-group"> 
                           <label for="message" class="form-label">Mensagem</label>       
     <textarea id="mensagem" class="form-textarea" required>textarea> 
     </div> 
                
                       <button type="submit" class="form-submit">Enviar Mensagem</button>       
           <Formulário>       
     </div> 
    </seção>
    
    <pés>
           <div class="contêiner">       
           <div class="ligações sociais">       
     <a href="#" class="social-icon">FB</a> 
     <a href="#" class="social-icon">IG</a> 
     <a href="#" class="social-icon">TW</a> 
     <a href="#" class="social-icon">YT</a> 
     </div> 
                   <p>&copy; 2025 Music Connect. Todos os direitos reservados.</p>       
     </div> 
    </pé>
</"Corpo">
<<HTML>><HTML>>
