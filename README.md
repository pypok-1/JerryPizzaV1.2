<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Smart Recipe · readme</title>
    <!-- Google Fonts & modern clean look -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&family=Playfair+Display:wght@700;800&display=swap" rel="stylesheet">
    <!-- Font Awesome 6 (free) icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #fcf9f6;  /* soft warm white */
            font-family: 'Inter', system-ui, -apple-system, sans-serif;
            line-height: 1.6;
            color: #1e2b24;
            padding: 2rem 1.5rem;
            display: flex;
            justify-content: center;
        }

        .readme-card {
            max-width: 1100px;
            width: 100%;
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(4px);
            border-radius: 3rem 3rem 2rem 2rem;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25), 0 8px 20px -8px rgba(245, 130, 32, 0.15);
            padding: 2.5rem 3rem;
            border: 1px solid rgba(245, 130, 32, 0.15);
        }

        /* decorative header wave */
        .brand-bar {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .gif-badge {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            background: #f0ebe4;
            padding: 0.5rem 1.5rem 0.5rem 1rem;
            border-radius: 60px;
            border: 1px solid #ffe6d5;
        }

        .gif-badge img {
            width: 48px;
            border-radius: 50%;
        }

        .gif-badge span {
            font-weight: 500;
            color: #2d4635;
            letter-spacing: 0.3px;
        }

        .pill-group {
            display: flex;
            gap: 0.8rem;
            flex-wrap: wrap;
        }

        .pill {
            background: white;
            border-radius: 40px;
            padding: 0.4rem 1.2rem;
            font-size: 0.9rem;
            font-weight: 600;
            box-shadow: 0 2px 6px rgba(0,0,0,0.02);
            border: 1px solid #f0d5c0;
            color: #2d4635;
        }

        .pill i {
            color: #F58220;
            margin-right: 6px;
        }

        h1 {
            text-align: center;
            margin: 1.2rem 0 0.4rem;
            line-height: 1.2;
        }

        .gradient-headline {
            font-size: 4rem;
            font-weight: 800;
            font-family: 'Playfair Display', serif;
            background: linear-gradient(135deg, #F58220 0%, #2D4635 80%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: -0.5px;
            display: inline-block;
            filter: drop-shadow(0 4px 6px rgba(245,130,32,0.15));
        }

        .typing-container {
            min-height: 80px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .badge-strip {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem 1.2rem;
            justify-content: center;
            margin: 2.2rem 0 2.5rem;
        }

        .badge-strip img {
            height: 32px;
            border-radius: 20px;
        }

        /* badges using span style like shields */
        .custom-badge {
            background: #1e2b24;
            color: white;
            padding: 0.35rem 1rem;
            border-radius: 30px;
            font-size: 0.9rem;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }

        .custom-badge.orange {
            background: #F58220;
            color: #1e2b24;
        }

        .custom-badge.green {
            background: #2d4635;
        }

        .custom-badge i {
            font-size: 1rem;
        }

        h2 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
            font-size: 2rem;
            margin: 2.5rem 0 1rem 0;
            border-left: 8px solid #F58220;
            padding-left: 1.2rem;
            color: #1e2b24;
        }

        h3 {
            font-weight: 600;
            font-size: 1.5rem;
            margin: 1.8rem 0 0.8rem;
            color: #2d4635;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        h3 i {
            color: #F58220;
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 1.8rem;
            margin: 2rem 0 1rem;
        }

        .feature-card {
            background: white;
            border-radius: 2rem;
            padding: 1.8rem 1.5rem;
            box-shadow: 0 10px 25px -10px rgba(0,0,0,0.1);
            border: 1px solid #f5e2d4;
            transition: transform 0.1s ease;
        }

        .feature-card:hover {
            transform: translateY(-4px);
            border-color: #F58220;
        }

        .feature-icon {
            background: #fef1e8;
            width: 50px;
            height: 50px;
            border-radius: 18px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            color: #F58220;
            margin-bottom: 1.2rem;
        }

        .feature-card h4 {
            font-size: 1.4rem;
            font-weight: 600;
            margin-bottom: 0.8rem;
        }

        .feature-card p {
            color: #3e4f47;
            font-size: 0.95rem;
        }

        .soon-badge {
            background: #ffe1cc;
            border-radius: 40px;
            padding: 0.2rem 0.9rem;
            font-size: 0.7rem;
            font-weight: 700;
            text-transform: uppercase;
            color: #b34e00;
            margin-left: 10px;
            letter-spacing: 0.5px;
        }

        ul {
            list-style: none;
        }

        ul li {
            margin-bottom: 0.7rem;
            padding-left: 1.8rem;
            position: relative;
        }

        ul li:before {
            font-family: "Font Awesome 6 Free";
            content: "\f00c";
            font-weight: 900;
            color: #F58220;
            position: absolute;
            left: 0;
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem 1.2rem;
            margin: 1.5rem 0;
        }

        .tech-item {
            background: #edf1ef;
            padding: 0.4rem 1.2rem;
            border-radius: 40px;
            font-size: 0.9rem;
            font-weight: 500;
            border: 1px solid #cddad2;
        }

        .code-block {
            background: #1e2b24;
            color: #e4f0e9;
            padding: 1.5rem 2rem;
            border-radius: 28px;
            font-family: 'JetBrains Mono', 'Fira Code', monospace;
            border: 2px solid #F58220;
            margin: 2rem 0;
            overflow-x: auto;
            white-space: pre-wrap;
            word-break: break-word;
            box-shadow: inset 0 0 10px rgba(0,0,0,0.3);
        }

        .code-block span {
            color: #faca9c;
        }

        .dev-grid {
            display: flex;
            gap: 2.5rem;
            margin: 2rem 0 1rem;
            flex-wrap: wrap;
        }

        .dev-profile {
            display: flex;
            align-items: center;
            gap: 1.2rem;
            background: white;
            padding: 0.8rem 1.8rem 0.8rem 1rem;
            border-radius: 60px;
            border: 1px solid #f5cdb2;
            box-shadow: 0 4px 12px rgba(245,130,32,0.1);
        }

        .dev-profile img {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            border: 3px solid #F58220;
        }

        .dev-profile strong {
            font-size: 1.3rem;
            color: #1e2b24;
        }

        .monitor-badges {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            background: #f2ede8;
            border-radius: 40px;
            padding: 1.2rem 2rem;
            margin: 1.8rem 0;
            justify-content: center;
        }

        .monitor-badges span {
            background: white;
            border-radius: 30px;
            padding: 0.3rem 1.2rem;
            font-weight: 600;
            font-size: 0.95rem;
            box-shadow: 0 2px 6px rgba(0,0,0,0.05);
        }

        .footer-note {
            text-align: center;
            margin-top: 3.5rem;
            opacity: 0.8;
            font-size: 0.9rem;
            border-top: 2px dashed #F58220;
            padding-top: 2rem;
        }

        .footer-note a {
            color: #2d4635;
            font-weight: 600;
            text-decoration: none;
            border-bottom: 2px solid #F58220;
        }

        @media (max-width: 600px) {
            .readme-card {
                padding: 1.5rem;
            }
            .gradient-headline {
                font-size: 2.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="readme-card">
        <!-- TOP BAR with gif and pill -->
        <div class="brand-bar">
            <div class="gif-badge">
                <img src="https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExcWh2Z29nbG5xZG4zd282ZXlmYW5kaTN3cXIwZ292cWdlNGV4eXh4OSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/Pcvj0fxvnO4I0khDQX/giphy.gif" alt="chef gif">
                <span><i class="fas fa-robot"></i> AI kitchen · live</span>
            </div>
            <div class="pill-group">
                <span class="pill"><i class="fas fa-check-circle"></i> 5k+ recipes</span>
                <span class="pill"><i class="fas fa-sparkles"></i> OpenRouter AI</span>
                <span class="pill"><i class="fas fa-cloud"></i> Grafana + Loki</span>
            </div>
        </div>

        <!-- MAIN TITLE with gradient (exactly as requested) -->
        <h1>
            <span class="gradient-headline">SMART RECIPE</span>
        </h1>

        <!-- TYPING SVG simulated with simple html & css animation (preserved style) -->
        <div class="typing-container">
            <img src="https://readme-typing-svg.demolab.com?font=Playfair+Display&weight=700&size=28&duration=3000&pause=1000&color=F58220&center=true&vCenter=true&random=false&width=600&lines=Your+AI-Powered+Kitchen+Assistant;4,300%2B+Recipes+at+Your+Fingertips;Cook+Smarter%2C+Not+Harder!" alt="Typing SVG" />
        </div>

        <!-- BADGE ROW (matching original badges + extra style) -->
        <div class="badge-strip">
            <span class="custom-badge green"><i class="fab fa-github"></i> Project: Recipe220</span>
            <span class="custom-badge orange"><i class="fas fa-utensils"></i> Site: Smart Recipe</span>
            <span class="custom-badge"><i class="fas fa-book-open"></i> Recipes: 5k+</span>
            <span class="custom-badge" style="background:#e0a82b;"><i class="fas fa-brain"></i> Generator: AI + Heuristics</span>
        </div>

        <!-- WELCOME TEXT -->
        <p style="font-size: 1.2rem; margin: 1.5rem 0 0.5rem; background: #fef7e9; padding: 1.5rem 2rem; border-radius: 40px; border-left: 8px solid #F58220;">
            <i class="fas fa-fire" style="color: #F58220; margin-right: 12px;"></i> 
            Welcome to <strong>Smart Recipe</strong> — the delightful web experience powered by the Recipe220 project. 
            Smart Recipe helps you discover, create, and cook amazing meals: browse our 5,000+ recipe database, or generate new recipes instantly from the ingredients you already have. 
            Ready to turn leftovers into magic? Let's cook!
        </p>

        <!-- TABLE OF CONTENTS (minimal but clean) -->
        <div style="background: #ffffffd6; border-radius: 40px; padding: 1.5rem 2rem; margin: 2rem 0;">
            <span style="font-weight:700; font-size:1.2rem;"><i class="fas fa-list-ul" style="color:#F58220"></i>  Contents</span>
            <div style="display: flex; flex-wrap: wrap; gap: 1rem 2rem; margin-top: 1rem;">
                <span><a href="#about" style="text-decoration:none; color:#2d4635;">About</a></span>
                <span><a href="#functionality" style="text-decoration:none; color:#2d4635;">Functionality</a></span>
                <span><a href="#key-features" style="text-decoration:none; color:#2d4635;">Key Features</a></span>
                <span><a href="#how-it-works" style="text-decoration:none; color:#2d4635;">How It Works</a></span>
                <span><a href="#tech-stack" style="text-decoration:none; color:#2d4635;">Tech Stack</a></span>
                <span><a href="#getting-started" style="text-decoration:none; color:#2d4635;">Getting Started</a></span>
                <span><a href="#developers" style="text-decoration:none; color:#2d4635;">Developers</a></span>
            </div>
        </div>

        <!-- ABOUT SECTION -->
        <h2 id="about">📘 About</h2>
        <p>Smart Recipe is a modern, friendly site built from the <strong>Recipe220</strong> project. Its core idea: combine a large curated recipe collection (5,000+ recipes) with an intelligent generator that crafts recipe suggestions based on the exact ingredients you have on hand. Whether you want a tried-and-true classic or a brand-new creation, Smart Recipe helps you move from pantry to plate.</p>
        <p style="margin-top: 0.8rem;">🔗 Project repository: <a href="https://github.com/AndriyPy/Recipe220" style="font-weight:600; color:#F58220;">github.com/AndriyPy/Recipe220</a></p>

        <!-- FUNCTIONALITY -->
        <h2 id="functionality">⚙️ Functionality</h2>

        <h3><i class="fas fa-user-lock"></i> User Management</h3>
        <ul>
            <li>Registration with email verification (6-digit code)</li>
            <li>Login with Cloudflare Turnstile (bot protection)</li>
            <li>Google SSO authentication</li>
            <li>Profile editing (gender, birth date, country)</li>
        </ul>

        <h3><i class="fas fa-book"></i> Recipes</h3>
        <ul>
            <li><strong>Database</strong>: 5,000+ recipes</li>
            <li><strong>Search</strong>: Fuzzy search (typo-tolerant), by name and ingredients</li>
            <li><strong>Sorting (SOON)</strong>: <span class="soon-badge">soon</span> by name, rating, time, servings</li>
            <li><strong>Recipe details (soon)</strong>: <span class="soon-badge">soon</span> with ingredients, steps, prep time, rating</li>
        </ul>

        <h3><i class="fas fa-robot"></i> AI Assistant</h3>
        <ul>
            <li>Generate recipes based on available ingredients</li>
            <li>Personalized recommendations</li>
            <li>OpenRouter AI integration</li>
        </ul>

        <h3><i class="fas fa-chart-line"></i> Monitoring Stack</h3>
        <div class="monitor-badges">
            <span>📊 Grafana</span> <span>📈 Prometheus</span> <span>📦 Loki</span> <span>🐳 cAdvisor</span> <span>📋 Promtail</span>
        </div>

        <!-- KEY FEATURES grid -->
        <h2 id="key-features">✨ Key Features</h2>
        <div class="feature-grid">
            <div class="feature-card">
                <div class="feature-icon"><i class="fas fa-magnifying-glass"></i></div>
                <h4>Fuzzy search</h4>
                <p>Find any recipe even with typos — search by name or ingredients.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon"><i class="fas fa-wand-magic-sparkles"></i></div>
                <h4>AI generation</h4>
                <p>Turn your leftover ingredients into new recipes via OpenRouter.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon"><i class="fas fa-cloud-sun"></i></div>
                <h4>Cloudflare Turnstile</h4>
                <p>Bot-proof but user-friendly captcha-free protection.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon"><i class="fas fa-chart-pie"></i></div>
                <h4>Full observability</h4>
                <p>Grafana + Prometheus + Loki, container monitoring with cAdvisor.</p>
            </div>
        </div>

        <!-- HOW IT WORKS (simplified) -->
        <h2 id="how-it-works">🧑‍🍳 How It Works</h2>
        <ol style="margin-left: 1.8rem; list-style-type: decimal; font-weight: 500;">
            <li style="margin-bottom: 0.8rem;"><strong>Tell us your ingredients</strong> — type what’s in your fridge.</li>
            <li style="margin-bottom: 0.8rem;"><strong>AI suggests recipes</strong> — heuristics + OpenRouter generate instant ideas.</li>
            <li style="margin-bottom: 0.8rem;"><strong>Browse 5k+ database</strong> — fuzzy search helps you find any dish.</li>
            <li style="margin-bottom: 0.8rem;"><strong>Cook & share</strong> — step-by-step, rating, and personal collections (soon).</li>
        </ol>

        <!-- TECH STACK with icons -->
        <h2 id="tech-stack">🛠️ Tech Stack</h2>
        <div class="tech-stack">
            <span class="tech-item">React / TypeScript</span>
            <span class="tech-item">Node.js (Express)</span>
            <span class="tech-item">PostgreSQL</span>
            <span class="tech-item">Redis</span>
            <span class="tech-item">Docker / k8s</span>
            <span class="tech-item">Grafana</span>
            <span class="tech-item">Prometheus</span>
            <span class="tech-item">Loki</span>
            <span class="tech-item">OpenRouter AI</span>
            <span class="tech-item">Cloudflare</span>
            <span class="tech-item">OAuth2 (Google)</span>
        </div>

        <!-- GETTING STARTED + code block -->
        <h2 id="getting-started">🚀 Getting Started</h2>
        <h3>Prerequisites</h3>
        <ul>
            <li>Node.js 18+ & npm</li>
            <li>PostgreSQL & Redis running</li>
            <li>OpenRouter API key (for AI generation)</li>
            <li>Cloudflare Turnstile keys (optional but recommended)</li>
        </ul>

        <h3>Install & Run</h3>
        <div class="code-block">
            <span># clone repository</span><br>
            git clone https://github.com/AndriyPy/Recipe220.git<br>
            cd Recipe220<br><br>
            <span># install dependencies</span><br>
            npm install<br><br>
            <span># configure environment (see .env.example)</span><br>
            cp .env.example .env<br><br>
            <span># run database migrations</span><br>
            npm run migrate<br><br>
            <span># start development server</span><br>
            npm run dev<br><br>
            <span># Smart Recipe will be available at http://localhost:3000</span>
        </div>

        <!-- USAGE EXAMPLES (small) -->
        <h2>🍳 Usage Examples</h2>
        <div style="background: #f5efe9; border-radius: 28px; padding: 1.5rem; margin: 1.5rem 0;">
            <p><i class="fas fa-search" style="color:#F58220"></i>  <strong>Fuzzy search:</strong> type "spageti" → finds "spaghetti carbonara"</p>
            <p><i class="fas fa-lightbulb" style="color:#F58220"></i>  <strong>Generate from:</strong> "chicken, lemon, garlic" → AI proposes lemon-garlic roast chicken with herbs</p>
            <p><i class="fas fa-star" style="color:#F58220"></i>  <strong>Filter soon:</strong> sort by rating, time, or servings</p>
        </div>

        <!-- DATABASE & CONTENT -->
        <h2>📀 Database & Content</h2>
        <p>We maintain a curated collection of 5,000+ recipes with rich metadata: ingredients, step-by-step instructions, prep time, and average rating. The dataset is periodically updated and augmented by heuristics + AI validation. Dump available for contributors.</p>

        <!-- CONTRIBUTING / LICENSE quick -->
        <h2>🤝 Contributing</h2>
        <p>We welcome PRs and ideas! Please check the <a href="#">contributing guide</a> (in repo). Feel free to open issues for feature requests or bugs.</p>

        <h2>📄 License</h2>
        <p>MIT © 2025 Smart Recipe · Recipe220. See <a href="#">LICENSE</a> for details.</p>

        <!-- DEVELOPERS (exactly with avatars) -->
        <h2 id="developers">👨‍🍳 Developers</h2>
        <div class="dev-grid">
            <div class="dev-profile">
                <img src="https://avatars.githubusercontent.com/u/187444054?v=4" alt="AndriyPy">
                <div>
                    <strong>AndriyPy</strong>
                    <div style="display:flex; gap:8px; margin-top:6px;">
                        <a href="https://github.com/AndriyPy"><i class="fab fa-github" style="color:#F58220; font-size:1.5rem;"></i></a>
                    </div>
                </div>
            </div>
            <div class="dev-profile">
                <img src="https://avatars.githubusercontent.com/u/187442340?v=4" alt="pypok-1">
                <div>
                    <strong>pypok-1</strong>
                    <div style="display:flex; gap:8px; margin-top:6px;">
                        <a href="https://github.com/pypok-1"><i class="fab fa-github" style="color:#F58220; font-size:1.5rem;"></i></a>
                    </div>
                </div>
            </div>
        </div>

        <!-- FOOTER NOTE with sparkle -->
        <div class="footer-note">
            <i class="fas fa-heart" style="color:#F58220"></i>  Smart Recipe — where AI meets delicious · <a href="https://github.com/AndriyPy/Recipe220">Recipe220 repo</a>
        </div>
    </div>
</body>
</html>
