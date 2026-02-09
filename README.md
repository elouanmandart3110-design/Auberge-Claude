<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>L'Auberge Claude - Résidence Senior de Charme</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background: #1a1a1a; color: #f5f5f5; line-height: 1.6; }
        header { background: linear-gradient(135deg, #000 0%, #2a2a2a 100%); padding: 60px 20px; text-align: center; border-bottom: 4px solid #ff6b35; }
        h1 { font-size: 3em; color: #ff6b35; margin-bottom: 20px; text-shadow: 2px 2px 4px rgba(0,0,0,0.5); }
        .subtitle { font-size: 1.3em; max-width: 800px; margin: 0 auto; color: #ddd; }
        .container { max-width: 1200px; margin: 0 auto; padding: 20px; }
        
        /* Carrousel */
        .carousel { position: relative; max-width: 100%; margin: 40px auto; overflow: hidden; border-radius: 10px; box-shadow: 0 10px 30px rgba(255,107,53,0.3); }
        .carousel-inner { display: flex; transition: transform 0.5s ease; }
        .carousel-item { min-width: 100%; height: 500px; background-size: cover; background-position: center; }
        .carousel-btn { position: absolute; top: 50%; transform: translateY(-50%); background: rgba(255,107,53,0.8); color: #fff; border: none; padding: 15px 20px; cursor: pointer; font-size: 24px; transition: 0.3s; }
        .carousel-btn:hover { background: #ff6b35; }
        .prev { left: 10px; } .next { right: 10px; }
        
        .section { margin: 60px 0; }
        h2 { color: #ff6b35; font-size: 2.2em; margin-bottom: 20px; border-left: 5px solid #ff6b35; padding-left: 15px; }
        .concept { background: #2a2a2a; padding: 30px; border-radius: 10px; margin: 20px 0; border: 2px solid #ff6b35; }
        
        .services { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin: 30px 0; }
        .service-card { background: #2a2a2a; padding: 25px; border-radius: 10px; border-left: 4px solid #ff6b35; transition: 0.3s; }
        .service-card:hover { transform: translateX(10px); background: #333; }
        
        table { width: 100%; border-collapse: collapse; margin: 30px 0; background: #2a2a2a; border-radius: 10px; overflow: hidden; }
        th { background: #ff6b35; color: #000; padding: 15px; font-weight: bold; }
        td { padding: 12px; border-bottom: 1px solid #444; }
        tr:hover { background: #333; }
        .libre { color: #4caf50; font-weight: bold; }
        .reserve { color: #f44336; font-weight: bold; }
        
        .gallery { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin: 30px 0; }
        .gallery-item { height: 250px; background-size: cover; background-position: center; border-radius: 10px; box-shadow: 0 5px 15px rgba(255,107,53,0.3); transition: 0.3s; position: relative; overflow: hidden; }
        .gallery-item:hover { transform: scale(1.05); box-shadow: 0 8px 25px rgba(255,107,53,0.5); }
        .gallery-label { position: absolute; bottom: 0; left: 0; right: 0; background: rgba(255,107,53,0.9); color: #000; padding: 10px; font-weight: bold; }
    </style>
</head>
<body>
    <header>
        <h1>Bienvenue à l'Auberge Claude</h1>
        <p class="subtitle">Un lieu calme, sécurisé et chaleureux pour les personnes âgées. Ici, chaque jour est une nouvelle occasion de profiter de la vie dans un cadre bienveillant et convivial.</p>
    </header>

    <div class="container">
        <!-- Carrousel des chambres -->
        <div class="carousel">
            <div class="carousel-inner" id="carouselInner">
                <div class="carousel-item" style="background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22800%22 height=%22500%22><rect fill=%22%23000%22 width=%22800%22 height=%22500%22/><text x=%2250%25%22 y=%2240%25%22 font-size=%2240%22 fill=%22%23ff6b35%22 text-anchor=%22middle%22>Chambre Confort</text><text x=%2250%25%22 y=%2250%25%22 font-size=%2220%22 fill=%22%23fff%22 text-anchor=%22middle%22>Lit double • Vue jardin</text><rect x=%22100%22 y=%22300%22 width=%22200%22 height=%22150%22 fill=%22%23ff6b35%22/><rect x=%22500%22 y=%22300%22 width=%22200%22 height=%22150%22 fill=%22%23333%22/></svg>');"></div>
                <div class="carousel-item" style="background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22800%22 height=%22500%22><rect fill=%22%23111%22 width=%22800%22 height=%22500%22/><text x=%2250%25%22 y=%2240%25%22 font-size=%2240%22 fill=%22%23ff6b35%22 text-anchor=%22middle%22>Chambre Premium</text><text x=%2250%25%22 y=%2250%25%22 font-size=%2220%22 fill=%22%23fff%22 text-anchor=%22middle%22>Suite avec salon • Balcon privé</text><circle cx=%22200%22 cy=%22350%22 r=%2270%22 fill=%22%23ff6b35%22/><circle cx=%22600%22 cy=%22350%22 r=%2270%22 fill=%22%23444%22/></svg>');"></div>
                <div class="carousel-item" style="background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22800%22 height=%22500%22><rect fill=%22%23000%22 width=%22800%22 height=%22500%22/><text x=%2250%25%22 y=%2240%25%22 font-size=%2240%22 fill=%22%23ff6b35%22 text-anchor=%22middle%22>Chambre Standard</text><text x=%2250%25%22 y=%2250%25%22 font-size=%2220%22 fill=%22%23fff%22 text-anchor=%22middle%22>Lit simple • Salle de bain adaptée</text><rect x=%22150%22 y=%22280%22 width=%22180%22 height=%22180%22 fill=%22%23ff6b35%22 opacity=%220.7%22/><rect x=%22470%22 y=%22280%22 width=%22180%22 height=%22180%22 fill=%22%23222%22/></svg>');"></div>
            </div>
            <button class="carousel-btn prev" onclick="moveCarousel(-1)">❮</button>
            <button class="carousel-btn next" onclick="moveCarousel(1)">❯</button>
        </div>

        <!-- Concept -->
        <div class="section">
            <h2>Notre Concept</h2>
            <div class="concept">
                <p>L'Auberge Claude est bien plus qu'une simple résidence pour seniors. C'est un véritable lieu de vie où le confort côtoie la convivialité. Nous avons créé un environnement pensé pour le bien-être de nos résidents, avec des espaces chaleureux et sécurisés.</p>
                <p style="margin-top: 15px;">Chaque jour, notre équipe dévouée accompagne les résidents dans leur quotidien, en respectant leur autonomie et leurs choix. Nous privilégions le lien humain, l'écoute et la bienveillance. Des activités variées rythment les journées, favorisant les rencontres et le maintien d'une vie sociale épanouie.</p>
                <p style="margin-top: 15px;">Le confort de nos résidents est notre priorité : chambres personnalisables, repas fait maison préparés avec soin, et une attention constante portée à leurs besoins. À l'Auberge Claude, nous créons ensemble un cadre de vie où il fait bon vieillir.</p>
            </div>
        </div>

        <!-- Services -->
        <div class="section">
            <h2>Nos Services</h2>
            <div class="services">
                <div class="service-card">
                    <h3 style="color: #ff6b35; margin-bottom: 10px;">🛏️ Logement Confortable</h3>
                    <p>Chambres spacieuses et adaptées, avec tout le confort moderne</p>
                </div>
                <div class="service-card">
                    <h3 style="color: #ff6b35; margin-bottom: 10px;">🍲 Repas Faits Maison</h3>
                    <p>Plats mijotés, soupes maison, bœuf bourguignon et spécialités traditionnelles</p>
                </div>
                <div class="service-card">
                    <h3 style="color: #ff6b35; margin-bottom: 10px;">🎯 Activités Quotidiennes</h3>
                    <p>Aquagym, salle à cigare, terrain de pétanque, loto, réveil musculaire, jeu apéro</p>
                </div>
                <div class="service-card">
                    <h3 style="color: #ff6b35; margin-bottom: 10px;">👥 Aide Permanente</h3>
                    <p>Personnel disponible à tout moment pour accompagner nos résidents</p>
                </div>
            </div>
        </div>

        <!-- Planning -->
        <div class="section">
            <h2>Disponibilités des Chambres</h2>
            <table>
                <thead>
                    <tr>
                        <th>Date</th>
                        <th>Chambre</th>
                        <th>Type</th>
                        <th>Statut</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>15 Mars 2026</td>
                        <td>Chambre 12</td>
                        <td>Confort</td>
                        <td class="libre">✓ LIBRE</td>
                    </tr>
                    <tr>
                        <td>20 Mars 2026</td>
                        <td>Chambre 08</td>
                        <td>Premium</td>
                        <td class="reserve">✗ RÉSERVÉ</td>
                    </tr>
                    <tr>
                        <td>25 Mars 2026</td>
                        <td>Chambre 15</td>
                        <td>Standard</td>
                        <td class="libre">✓ LIBRE</td>
                    </tr>
                    <tr>
                        <td>01 Avril 2026</td>
                        <td>Chambre 03</td>
                        <td>Premium</td>
                        <td class="libre">✓ LIBRE</td>
                    </tr>
                    <tr>
                        <td>10 Avril 2026</td>
                        <td>Chambre 19</td>
                        <td>Confort</td>
                        <td class="reserve">✗ RÉSERVÉ</td>
                    </tr>
                    <tr>
                        <td>15 Avril 2026</td>
                        <td>Chambre 22</td>
                        <td>Standard</td>
                        <td class="libre">✓ LIBRE</td>
                    </tr>
                </tbody>
            </table>
        </div>

        <!-- Galerie -->
        <div class="section">
            <h2>La Vie à l'Auberge</h2>
            <div class="gallery">
                <div class="gallery-item" style="background: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.4)), url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22400%22 height=%22300%22><rect fill=%22%23000%22 width=%22400%22 height=%22300%22/><circle cx=%22200%22 cy=%22100%22 r=%2240%22 fill=%22%23ff6b35%22/><rect x=%2250%22 y=%22160%22 width=%22300%22 height=%2280%22 fill=%22%23333%22 rx=%2210%22/><text x=%22200%22 y=%22210%22 font-size=%2230%22 fill=%22%23ff6b35%22 text-anchor=%22middle%22>Restaurant</text></svg>');">
                    <div class="gallery-label">Restaurant Gastronomique</div>
                </div>
                <div class="gallery-item" style="background: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.4)), url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22400%22 height=%22300%22><rect fill=%22%23111%22 width=%22400%22 height=%22300%22/><rect x=%2250%22 y=%2250%22 width=%22300%22 height=%22200%22 fill=%22%234a9eff%22 opacity=%220.6%22 rx=%2215%22/><text x=%22200%22 y=%22160%22 font-size=%2235%22 fill=%22%23fff%22 text-anchor=%22middle%22>Aquagym</text></svg>');">
                    <div class="gallery-label">Piscine & Aquagym</div>
                </div>
                <div class="gallery-item" style="background: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.4)), url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22400%22 height=%22300%22><rect fill=%22%23000%22 width=%22400%22 height=%22300%22/><circle cx=%22100%22 cy=%22150%22 r=%2215%22 fill=%22%23ff6b35%22/><circle cx=%22200%22 cy=%22150%22 r=%2215%22 fill=%22%23ff6b35%22/><circle cx=%22300%22 cy=%22150%22 r=%2215%22 fill=%22%23ff6b35%22/><text x=%22200%22 y=%22240%22 font-size=%2225%22 fill=%22%23fff%22 text-anchor=%22middle%22>Terrain Pétanque</text></svg>');">
                    <div class="gallery-label">Terrain de Pétanque</div>
                </div>
                <div class="gallery-item" style="background: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.4)), url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22400%22 height=%22300%22><rect fill=%22%230a0a0a%22 width=%22400%22 height=%22300%22/><rect x=%2280%22 y=%2280%22 width=%22240%22 height=%22140%22 fill=%22%23222%22 rx=%2210%22/><circle cx=%22150%22 cy=%22150%22 r=%2225%22 fill=%22%23ff6b35%22/><circle cx=%22250%22 cy=%22150%22 r=%2225%22 fill=%22%23ff6b35%22/><text x=%22200%22 y=%22260%22 font-size=%2222%22 fill=%22%23fff%22 text-anchor=%22middle%22>Salle Cigare</text></svg>');">
                    <div class="gallery-label">Salon & Salle à Cigare</div>
                </div>
                <div class="gallery-item" style="background: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.4)), url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22400%22 height=%22300%22><rect fill=%22%23000%22 width=%22400%22 height=%22300%22/><rect x=%22100%22 y=%2280%22 width=%2260%22 height=%2290%22 fill=%22%23ff6b35%22 rx=%225%22/><rect x=%22240%22 y=%2280%22 width=%2260%22 height=%2290%22 fill=%22%23ff6b35%22 rx=%225%22/><text x=%22200%22 y=%22230%22 font-size=%2228%22 fill=%22%23fff%22 text-anchor=%22middle%22>Loto</text></svg>');">
                    <div class="gallery-label">Salle de Loto</div>
                </div>
                <div class="gallery-item" style="background: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.4)), url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22400%22 height=%22300%22><rect fill=%22%23111%22 width=%22400%22 height=%22300%22/><path d=%22M 150 100 Q 200 80 250 100%22 stroke=%22%23ff6b35%22 stroke-width=%225%22 fill=%22none%22/><circle cx=%22200%22 cy=%22180%22 r=%2235%22 fill=%22%23ff6b35%22 opacity=%220.7%22/><text x=%22200%22 y=%22260%22 font-size=%2224%22 fill=%22%23fff%22 text-anchor=%22middle%22>Réveil Musculaire</text></svg>');">
                    <div class="gallery-label">Salle de Fitness</div>
                </div>
            </div>
        </div>
    </div>

    <script>
        let currentSlide = 0;
        const slides = document.querySelectorAll('.carousel-item');
        const totalSlides = slides.length;

        function moveCarousel(direction) {
            currentSlide = (currentSlide + direction + totalSlides) % totalSlides;
            document.getElementById('carouselInner').style.transform = `translateX(-${currentSlide * 100}%)`;
        }

        // Auto-défilement
        setInterval(() => moveCarousel(1), 5000);
    </script>
</body>
</html>
