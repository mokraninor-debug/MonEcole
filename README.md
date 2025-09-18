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
