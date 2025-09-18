<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ILAC Formations</title>
    <link rel="stylesheet" href="ecole.css">
</head>
<body>
    <nav class="navbar">
        <div class="logo">ILAC Formations</div>
       <div class="account-menu">
        <a href="#" class="login-btn">Se connecter</a>
        <a href="#" class="signup-btn">Créer un compte</a>
    </div>
    </nav>
    
    <header class="hero">
        <div class="hero-content">
            <h1>Développez vos compétences avec ILAC Formations</h1>
            <p>Des formations professionnelles pour réussir votre avenir.</p>
            <a href="#courses" class="cta-btn">Voir nos cours</a>
        </div>
    </header>
    <main>
        <section id="about" class="section about-section">
            <h2>À propos de nous</h2>
            <p>Notre école propose des formations certifiantes et adaptées au marché du travail. Rejoignez-nous pour apprendre un métier d’avenir !</p>
        </section>
       <section id="courses" class="section courses-section">
    <h2>Nos cours</h2>
    <div class="courses-list">
        <div class="course-card">
            <span class="course-icon">🔧</span>
            <h3>Plomberie</h3>
            <p>Maîtrisez les bases et les techniques avancées de la plomberie pour intervenir efficacement sur tous types d’installations.</p>
            <a href="#" class="course-btn">En savoir plus</a>
        </div>
        <div class="course-card">
            <span class="course-icon">🩺</span>
            <h3>Secourisme</h3>
            <p>Apprenez les gestes qui sauvent, obtenez votre certification et soyez prêt à agir en situation d’urgence.</p>
            <a href="#" class="course-btn">En savoir plus</a>
        </div>
        <div class="course-card">
            <span class="course-icon">🚗</span>
            <h3>Mécanique</h3>
            <p>Devenez expert en réparation et entretien de véhicules, du diagnostic à l’intervention technique.</p>
            <a href="#" class="course-btn">En savoir plus</a>
        </div>
        <div class="course-card">
            <span class="course-icon">💡</span>
            <h3>Électricité</h3>
            <p>Formez-vous aux installations électriques, à la sécurité et aux normes en vigueur pour devenir un professionnel reconnu.</p>
            <a href="#" class="course-btn">En savoir plus</a>
        </div>
    </div>
</section>
               <section id="contact" class="section contact-section">
            <h2>Contactez-nous</h2>
            <div class="contact-flex">
                <form class="contact-form">
                    <input type="text" placeholder="Votre nom" required>
                    <input type="email" placeholder="Votre email" required>
                    <textarea placeholder="Votre message" required></textarea>
                    <button type="submit">Envoyer</button>
                </form>
                <div class="contact-details">
                    <div class="contact-item">
                        <span class="contact-icon">📧</span>
                        <span>ilacformations@gmail.com</span>
                    </div>
                    <div class="contact-item">
                        <span class="contact-icon">📞</span>
                        <span>JE NE SAIS PAS</span>
                    </div>
                    <div class="contact-item">
                        <span class="contact-icon">📍</span>
                        <span><a href="https://www.google.com/maps/place/Ecole+de+langues/@36.5171321,3.9808242,18.42z/data=!4m6!3m5!1s0x128c33004207259d:0x5d834fdc9351ce08!8m2!3d36.5169797!4d3.9813219!16s%2Fg%2F11xt39mff8?entry=ttu&g_ep=EgoyMDI1MDkwOC4wIKXMDSoASAFQAw%3D%3D">Devant toi, Paris</a></span>
                    </div>
                </div>
            </div>
        </section>
    </main>
    <div id="login-modal" class="modal">
    <div class="modal-content">
        <span class="close-modal">&times;</span>
        <h2>Connexion</h2>
        <form class="login-form">
            <input type="email" placeholder="Email" required>
            <input type="password" placeholder="Mot de passe" required>
            <button type="submit">Se connecter</button>
        </form>
        <p class="modal-link">Pas encore de compte ? <a href="#">Créer un compte</a></p>
    </div>
</div>
<div id="signup-modal" class="modal">
    <div class="modal-content">
        <span class="close-signup">&times;</span>
        <h2>Créer un compte</h2>
        <form class="signup-form" method="POST" action="signup.php" target="_blank">
            <input type="text" name="name" placeholder="Nom complet" required>
            <input type="email" name="email" placeholder="Email" required>
            <input type="password" name="password" placeholder="Mot de passe" required>
            <button type="submit">S'inscrire</button>
        </form>
        <p class="modal-link">Déjà inscrit ? <a href="#" id="open-login">Se connecter</a></p>
    </div>
</div>
<script>
document.querySelector('.login-btn').onclick = function(e) {
    e.preventDefault();
    document.getElementById('login-modal').style.display = 'flex';
};
document.querySelector('.close-modal').onclick = function() {
    document.getElementById('login-modal').style.display = 'none';
};
window.onclick = function(event) {
    const modal = document.getElementById('login-modal');
    if (event.target === modal) modal.style.display = 'none';
};
    document.querySelector('.signup-btn').onclick = function(e) {
    e.preventDefault();
    document.getElementById('signup-modal').style.display = 'flex';
};
document.querySelector('.close-signup').onclick = function() {
    document.getElementById('signup-modal').style.display = 'none';
};
document.getElementById('open-login').onclick = function(e) {
    e.preventDefault();
    document.getElementById('signup-modal').style.display = 'none';
    document.getElementById('login-modal').style.display = 'flex';
};
window.onclick = function(event) {
    const signupModal = document.getElementById('signup-modal');
    const loginModal = document.getElementById('login-modal');
    if (event.target === signupModal) signupModal.style.display = 'none';
    if (event.target === loginModal) loginModal.style.display = 'none';
};
</script>
</body>
</html>
body {
    margin: 0;
    font-family: 'Segoe UI', Arial, sans-serif;
    background: #f7f8fa;
    color: #222;
}

.navbar {
    background: #0055b8;
    color: #fff;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 40px;
    height: 60px;
    box-shadow: 0 2px 8px rgba(0,85,184,0.07);
}

.logo {
    font-size: 1.5em;
    font-weight: bold;
    letter-spacing: 1px;
}

.account-menu {
    display: flex;
    gap: 18px;
    align-items: center;
}

.login-btn, .signup-btn {
    padding: 10px 28px;
    border-radius: 25px;
    font-weight: 500;
    text-decoration: none;
    font-size: 1em;
    transition: background 0.2s, color 0.2s;
    border: 2px solid transparent;
    cursor: pointer;
}

.login-btn {
    background: #fff;
    color: #0055b8;
    border: 2px solid #0055b8;
}

.login-btn:hover {
    background: #0055b8;
    color: #fff;
}

.signup-btn {
    background: #ffffff;
    color: #0055b8;
    border: 2px solid #0055b8;
}

.signup-btn:hover {
    background: #0055b8;
    color: #ffffff;
    border: 2px solid #0055b8;
}

.hero {
    background: linear-gradient(90deg, #0055b8 60%, #0077e3 100%);
    color: #fff;
    padding: 60px 20px 40px 20px;
    text-align: center;
}

.hero-content h1 {
    font-size: 2.5em;
    margin-bottom: 10px;
}

.hero-content p {
    font-size: 1.2em;
    margin-bottom: 25px;
}

.cta-btn {
    background: #ffd600;
    color: #0055b8;
    padding: 12px 32px;
    border: none;
    border-radius: 25px;
    font-size: 1.1em;
    font-weight: bold;
    text-decoration: none;
    transition: background 0.2s;
    box-shadow: 0 2px 8px rgba(0,85,184,0.07);
}

.cta-btn:hover {
    background: #fff;
    color: #0055b8;
}

.section {
    max-width: 900px;
    margin: 40px auto;
    background: #fff;
    border-radius: 12px;
    box-shadow: 0 2px 8px rgba(0,85,184,0.07);
    padding: 40px 30px;
}

.section h2 {
    color: #0055b8;
    margin-top: 0;
    font-size: 2em;
}

.courses-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 25px;
    margin-top: 30px;
}

.course-card {
    background: #f7f8fa;
    border-radius: 10px;
    box-shadow: 0 1px 4px rgba(0,85,184,0.07);
    padding: 25px 20px;
    text-align: center;
    transition: transform 0.2s;
    position: relative;
}

.course-card:hover {
    transform: translateY(-5px) scale(1.03);
    box-shadow: 0 4px 16px rgba(0,85,184,0.13);
}

.course-icon {
    font-size: 2.2em;
    display: block;
    margin-bottom: 12px;
}

.course-btn {
    display: inline-block;
    margin-top: 16px;
    padding: 10px 24px;
    background: #0055b8;
    color: #fff;
    border-radius: 20px;
    text-decoration: none;
    font-weight: 500;
    transition: background 0.2s;
    box-shadow: 0 1px 4px rgba(0,85,184,0.07);
}

.course-btn:hover {
    background: #ffd600;
    color: #0055b8;
}

.contact-flex {
    display: flex;
    gap: 40px;
    flex-wrap: wrap;
    align-items: flex-start;
}

.contact-form {
    flex: 1 1 300px;
    background: #f7f8fa;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 1px 4px rgba(0,85,184,0.07);
    display: flex;
    flex-direction: column;
    gap: 15px;
}

.contact-form input,
.contact-form textarea {
    padding: 12px;
    border: 1px solid #cfd8dc;
    border-radius: 6px;
    font-size: 1em;
    resize: vertical;
}

.contact-form button {
    background: #0055b8;
    color: #fff;
    border: none;
    border-radius: 25px;
    padding: 12px 0;
    font-size: 1.1em;
    font-weight: bold;
    cursor: pointer;
    transition: background 0.2s;
}

.contact-form button:hover {
    background: #0077e3;
}

.contact-details {
    flex: 1 1 220px;
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin-top: 10px;
}

.contact-item {
    display: flex;
    align-items: center;
    gap: 12px;
    font-size: 1.1em;
    background: #eef3fa;
    padding: 12px 16px;
    border-radius: 8px;
}

.contact-icon {
    font-size: 1.5em;
}

footer {
    width: 100%;
    position: fixed;
    left: 0;
    bottom: 0;
    background: #222;
    color: #fff;
    text-align: center;
    padding: 15px 0;
    font-size: 1em;
    z-index: 100;
    box-shadow: 0 -2px 8px rgba(0,0,0,0.07);
}


.modal {
    display: none;
    position: fixed;
    z-index: 999;
    left: 0; top: 0;
    width: 100%; height: 100%;
    background: rgba(0,0,0,0.4);
    justify-content: center;
    align-items: center;
}

.modal-content {
    background: #fff;
    padding: 32px 24px;
    border-radius: 12px;
    box-shadow: 0 4px 24px rgba(0,85,184,0.13);
    max-width: 350px;
    width: 90%;
    position: relative;
    text-align: center;
}

.close-modal, .close-signup {
    position: absolute;
    top: 12px; right: 18px;
    font-size: 1.5em;
    cursor: pointer;
}

.login-form input,
.signup-form input {
    width: 90%;
    margin: 10px 0;
    padding: 10px;
    border-radius: 6px;
    border: 1px solid #cfd8dc;
    font-size: 1em;
}

.login-form button,
.signup-form button {
    width: 95%;
    padding: 12px;
    background: #0055b8;
    color: #fff;
    border: none;
    border-radius: 25px;
    font-size: 1.1em;
    font-weight: bold;
    cursor: pointer;
    margin-top: 10px;
    transition: background 0.2s;
}

.login-form button:hover,
.signup-form button:hover {
    background: #0077e3;
}

.modal-link {
    margin-top: 18px;
    font-size: 0.95em;
}

.modal-link a {
    color: #0055b8;
    text-decoration: underline;
    cursor: pointer;
}


@media (max-width: 900px) {
    .section {
        padding: 25px 10px;
    }
    .navbar {
        padding: 0 15px;
    }
    .account-menu {
        padding: 0;
    }
}

@media (max-width: 700px) {
    .contact-flex {
        flex-direction: column;
        gap: 20px;
    }
}

@media (max-width: 600px) {
    .navbar {
        flex-direction: column;
        height: auto;
        padding: 10px 0;
    }
    .account-menu {
        gap: 10px;
        padding: 12px 0 0 0;
    }
    .login-btn, .signup-btn {
        padding: 8px 16px;
        font-size: 0.95em;
    }
    .hero-content h1 {
        font-size: 1.5em;
    }
    .section h2 {
        font-size: 1.3em;
    }
    .courses-list {
        grid-template-columns: 1fr;
    }
}



