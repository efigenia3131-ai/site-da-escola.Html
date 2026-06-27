# site-da-escola.Html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>site comum</title>
    <style>
        :root {
            --azul: #174b7a;
            --azul-claro: #3f84c5;
            --laranja: #ff8c1a;
            --branco: #fffaf3;
            --cinza: #f2f6fb;
            --texto: #22374d;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: "Segoe UI", Arial, sans-serif;
            background: linear-gradient(135deg, #eef6ff 0%, #fff7ea 100%);
            color: var(--texto);
            line-height: 1.6;
            overflow-x: hidden;
        }

        header {
            background: linear-gradient(90deg, var(--azul) 0%, var(--azul-claro) 100%);
            color: white;
            padding: 24px 20px;
            box-shadow: 0 6px 20px rgba(0,0,0,0.15);
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
        }

        .cabecalho {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 16px;
            flex-wrap: wrap;
        }

        .cabecalho h1 {
            font-size: 1.6rem;
        }

        .cabecalho p {
            opacity: 0.95;
        }

        main {
            padding: 30px 20px 60px;
        }

        .hero {
            background: linear-gradient(90deg, rgba(7,45,81,0.88), rgba(15,88,143,0.75)), url('sua-imagem-de-fundo.jpg');
            background-size: cover;
            background-position: center;
            border-radius: 24px;
            padding: 42px;
            color: white;
            box-shadow: 0 10px 30px rgba(0,0,0,0.18);
        }

        .hero h2 {
            font-size: clamp(1.8rem, 3vw, 2.7rem);
            margin-bottom: 12px;
        }

        .hero p {
            max-width: 700px;
            font-size: 1.05rem;
            margin-bottom: 20px;
        }

        .botao {
            display: inline-block;
            background: var(--laranja);
            color: white;
            padding: 12px 20px;
            border: none;
            border-radius: 999px;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            text-decoration: none;
            transition: transform 0.25s ease, box-shadow 0.25s ease, background 0.25s ease;
            box-shadow: 0 6px 14px rgba(0,0,0,0.15);
        }

        .botao:hover {
            transform: translateY(-3px) scale(1.04);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
            background: #ff9d33;
        }

        .botao:active {
            transform: translateY(1px) scale(0.98);
        }

        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
            margin-top: 24px;
        }

        .card {
            background: white;
            border-radius: 18px;
            padding: 20px;
            box-shadow: 0 8px 24px rgba(0,0,0,0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 28px rgba(0,0,0,0.12);
        }

        .card h3 {
            color: var(--azul);
            margin-bottom: 8px;
        }

        .sobre {
            margin-top: 28px;
            background: white;
            border-radius: 18px;
            padding: 24px;
            box-shadow: 0 8px 24px rgba(0,0,0,0.08);
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s ease, transform 0.8s ease;
        }

        .sobre.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .sobre h3 {
            color: var(--azul);
            margin-bottom: 10px;
        }

        footer {
            text-align: center;
            padding: 20px;
            color: #4e6478;
            font-size: 0.95rem;
        }
    </style>
</head>
<body>
    <header>
        <div class="container cabecalho">
            <div>
                <h1>Colégio e Curso Evolução (CCE)</h1>
                <p>Site oficial da turma do 8º ano</p>
            </div>
            <span>creditos:gabriel milton</span>
        </div>
    </header>

    <main class="container">
        <section class="hero">
            <h2>Bem-vindos à meu site.... quer dizer, ao nosso site! (otimismo lixo)</h2>
            <p>texto em desenvolvimeto....</p>
            <button class="botao" type="button" onclick="redirectToSite()">Conhecer mais</button>
        </section>

        <section class="cards">
            <article class="card">
                <h3>haverá atualizações?</h3>
                <p>Sim, o site será atualizado com novos conteúdos e funcionalidades ao longo do ano.</p>
            </article>
            <article class="card">
                <h3>qual é a utilidade desse site?</h3>
                <p>nem eu sei, mas oque o povo (voces) decidirem está decidido.</p>
            </article>
            <article class="card">
                <h3>como eu fiz?</h3>
                <p>usando uma caçetada de progamas!</p>
            </article>
        </section>

        <section class="sobre">
            <h3>Sobre o site</h3>
            <p>fala galera, obrigado pela confiaça de entrar em um llink suspeito que eu dropei no grupo</p>
        </section>
    </main>

    <footer>
        <p>Fim, mas calma ainda tem uma baita coisa para melhorar no site</p>
    </footer>

    <script>
        function redirectToSite() {
            var url = 'https://example.com';
            window.location.href = url;
        }

        const sobre = document.querySelector('.sobre');

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.2 });

        if (sobre) {
            observer.observe(sobre);
        }
    </script>
</body>
</html>

<html>







</html>

