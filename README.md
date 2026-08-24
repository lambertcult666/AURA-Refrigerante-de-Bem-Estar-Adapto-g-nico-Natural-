<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AURA | Refrigerante Funcional & Adaptogênico</title>
    <style>
        :root {
            --bg-color: #f7f9fc;
            --text-dark: #2d3748;
            --text-muted: #718096;
            --focus-grad: linear-gradient(135deg, #fef08a, #bef264);
            --chill-grad: linear-gradient(135deg, #c084fc, #818cf8);
            --glow-grad: linear-gradient(135deg, #f472b6, #fb923c);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Header / Navbar */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.5rem 10%;
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(10px);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid rgba(0,0,0,0.05);
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 800;
            letter-spacing: 3px;
            background: linear-gradient(45deg, #818cf8, #f472b6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        nav a {
            margin-left: 2rem;
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #818cf8;
        }

        .btn-nav {
            background: var(--text-dark);
            color: #fff !important;
            padding: 0.6rem 1.2rem;
            border-radius: 20px;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 10%;
            padding-top: 80px;
            background: radial-gradient(circle at 80% 20%, #fbcfe8 0%, #e0e7ff 40%, #f7f9fc 70%);
            gap: 2rem;
        }

        .hero-text {
            flex: 1;
            max-width: 500px;
        }

        .hero-text h1 {
            font-size: 3.5rem;
            line-height: 1.1;
            margin-bottom: 1.5rem;
        }

        .hero-text p {
            font-size: 1.2rem;
            color: var(--text-muted);
            margin-bottom: 2rem;
        }

        .btn-primary {
            display: inline-block;
            padding: 1rem 2.5rem;
            border-radius: 30px;
            background: var(--text-dark);
            color: #fff;
            text-decoration: none;
            font-weight: 600;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 25px rgba(0,0,0,0.15);
        }

        .hero-image {
            flex: 1.2;
            display: flex;
            justify-content: center;
        }

        .product-img {
            width: 100%;
            max-width: 650px;
            border-radius: 24px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.12);
            object-fit: cover;
        }

        /* Flavors Section */
        .flavors {
            padding: 6rem 10%;
            text-align: center;
        }

        .section-title {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .section-subtitle {
            color: var(--text-muted);
            margin-bottom: 4rem;
        }

        .cards-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2.5rem;
        }

        .card {
            background: #fff;
            border-radius: 24px;
            padding: 2.5rem 1.5rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.03);
            transition: transform 0.3s;
            position: relative;
            overflow: hidden;
        }

        .card:hover {
            transform: translateY(-10px);
        }

        .card-badge {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            margin: 0 auto 1.5rem auto;
        }

        .focus .card-badge { background: var(--focus-grad); }
        .chill .card-badge { background: var(--chill-grad); }
        .glow .card-badge  { background: var(--glow-grad); }

        .card h3 {
            font-size: 1.8rem;
            margin-bottom: 0.5rem;
        }

        .card-flavor {
            color: var(--text-muted);
            font-size: 0.95rem;
            margin-bottom: 1.5rem;
            font-weight: 600;
        }

        .card-benefits {
            list-style: none;
            text-align: left;
            margin-top: 1rem;
            border-top: 1px solid #edf2f7;
            padding-top: 1rem;
        }

        .card-benefits li {
            margin-bottom: 0.5rem;
            font-size: 0.9rem;
            color: var(--text-dark);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 3rem 10%;
            background: #fff;
            border-top: 1px solid #edf2f7;
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        /* Responsividade */
        @media (max-width: 900px) {
            .hero {
                flex-direction: column;
                text-align: center;
                padding-top: 120px;
                padding-bottom: 3rem;
            }
            .hero-text { margin-bottom: 2rem; }
            .hero-image { width: 100%; }
            nav { display: none; }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="logo">AURA</div>
        <nav>
            <a href="#sabores">Sabores</a>
            <a href="#beneficios">Benefícios</a>
            <a href="#comprar" class="btn-nav">Comprar Agora</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-text">
            <h1>Efervescência para a sua mente.</h1>
            <p>O primeiro refrigerante funcional adaptogênico do Brasil. Sabor natural, zero açúcar e o impulso certo para o seu dia.</p>
            <a href="#sabores" class="btn-primary">Descubra os Sabores</a>
        </div>
        <div class="hero-image">
            <!-- Coloque a imagem salva com o nome 'aura-produtos.png' na mesma pasta -->
            <img src="aura-produtos.png" alt="Latas AURA - Chill, Focus e Glow" class="product-img">
        </div>
    </section>

    <!-- Sabores Section -->
    <section class="flavors" id="sabores">
        <h2 class="section-title">Escolha a sua Vibe</h2>
        <p class="section-subtitle">Formulado com botânicos e adaptógenos para cada momento do seu dia.</p>

        <div class="cards-grid">
            <!-- Chill -->
            <div class="card chill">
                <div class="card-badge"></div>
                <h3>AURA Chill</h3>
                <p class="card-flavor">Lavanda, Amora & Limão</p>
                <ul class="card-benefits">
                    <li>🌿 Ashwagandha & Camomila</li>
                    <li>🧘‍♂️ Alívio de estresse natural</li>
                    <li>🌱 Zero Açúcar / Vegano</li>
                </ul>
            </div>

            <!-- Focus -->
            <div class="card focus">
                <div class="card-badge"></div>
                <h3>AURA Focus</h3>
                <p class="card-flavor">Yuzu, Gengibre & Maçã Verde</p>
                <ul class="card-benefits">
                    <li>⚡ L-Teanina & Chá Verde</li>
                    <li>🧠 Clareza mental sem agitação</li>
                    <li>🌱 Zero Açúcar / Vegano</li>
                </ul>
            </div>

            <!-- Glow -->
            <div class="card glow">
                <div class="card-badge"></div>
                <h3>AURA Glow</h3>
                <p class="card-flavor">Pitaya, Maracujá & Manjericão</p>
                <ul class="card-benefits">
                    <li>✨ Colágeno Vegetal & Zinco</li>
                    <li>🌸 Saúde da pele e hidratação</li>
                    <li>🌱 Zero Açúcar / Vegano</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>© 2026 AURA Bebidas Funcionais Ltda. Todos os direitos reservados.</p>
    </footer>

</body>
</html>
