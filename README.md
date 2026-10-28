<!DOCTYPE html>
<html lang="fr" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mon Portfolio</title>
    <!-- Intégration de Tailwind CSS pour le style -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Configuration des couleurs personnalisées Tailwind -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#4f46e5', // Couleur Indigo principale
                        secondary: '#1e293b', // Couleur sombre pour le texte
                    }
                }
            }
        }
    </script>
    <!-- Polices Google -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <!-- Icônes FontAwesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        body { font-family: 'Inter', sans-serif; }
        /* Style pour masquer la barre de défilement tout en permettant le défilement */
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
    </style>
</head>
<body class="bg-gray-50 text-gray-800 antialiased selection:bg-primary selection:text-white">

    <!-- BARRE DE NAVIGATION -->
    <nav class="fixed w-full z-50 bg-white/90 backdrop-blur-md border-b border-gray-100 shadow-sm transition-all duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- Logo / Nom -->
                <div class="flex-shrink-0">
                    <a href="#accueil" class="text-2xl font-bold text-secondary tracking-tight">Mon<span class="text-primary">Portfolio</span></a>
                </div>
                
                <!-- Menu Bureau -->
                <div class="hidden md:flex space-x-8 items-center">
                    <a href="#accueil" class="text-gray-600 hover:text-primary transition-colors font-medium">Accueil</a>
                    <a href="#apropos" class="text-gray-600 hover:text-primary transition-colors font-medium">À propos</a>
                    <a href="#portfolio" class="text-gray-600 hover:text-primary transition-colors font-medium">Portfolio</a>
                    <a href="#contact" class="px-5 py-2 rounded-full bg-primary text-white font-medium hover:bg-indigo-700 transition-all shadow-md hover:shadow-lg transform hover:-translate-y-0.5">Me contacter</a>
                </div>

                <!-- Bouton Menu Mobile -->
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-btn" class="text-gray-600 hover:text-primary focus:outline-none">
                        <i class="fas fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Menu Mobile (Caché par défaut) -->
        <div id="mobile-menu" class="hidden md:hidden bg-white border-t border-gray-100 shadow-lg absolute w-full">
            <div class="px-4 pt-2 pb-6 space-y-2">
                <a href="#accueil" class="block px-3 py-3 rounded-md text-base font-medium text-gray-700 hover:text-primary hover:bg-gray-50">Accueil</a>
                <a href="#apropos" class="block px-3 py-3 rounded-md text-base font-medium text-gray-700 hover:text-primary hover:bg-gray-50">À propos</a>
                <a href="#portfolio" class="block px-3 py-3 rounded-md text-base font-medium text-gray-700 hover:text-primary hover:bg-gray-50">Portfolio</a>
                <a href="#contact" class="block px-3 py-3 rounded-md text-base font-medium text-primary hover:bg-gray-50">Me contacter</a>
            </div>
        </div>
    </nav>

    <!-- SECTION ACCUEIL (HERO) -->
    <section id="accueil" class="pt-32 pb-20 md:pt-48 md:pb-32 px-4 flex flex-col items-center justify-center text-center min-h-screen">
        <div class="max-w-4xl mx-auto">
            <h2 class="text-sm font-semibold text-primary uppercase tracking-widest mb-3">Bonjour, je suis</h2>
            <h1 class="text-5xl md:text-7xl font-extrabold text-secondary mb-6 leading-tight">
                Créateur de <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-purple-600">Solutions</span>
            </h1>
            <p class="text-xl text-gray-600 mb-10 max-w-2xl mx-auto leading-relaxed">
                Bienvenue sur mon espace personnel. Je suis passionné par la création de contenus interactifs, le développement web et le design de solutions innovantes.
            </p>
            <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
                <a href="#portfolio" class="w-full sm:w-auto px-8 py-4 bg-primary text-white rounded-full font-semibold hover:bg-indigo-700 transition-all shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                    Découvrir mon travail
                </a>
                <a href="#contact" class="w-full sm:w-auto px-8 py-4 bg-white text-secondary border border-gray-200 rounded-full font-semibold hover:border-primary hover:text-primary transition-all shadow-sm">
                    Parlons-en
                </a>
            </div>
        </div>
    </section>

    <!-- SECTION À PROPOS -->
    <section id="apropos" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row items-center gap-12">
                <!-- Image de profil -->
                <div class="w-full md:w-1/2 flex justify-center">
                    <div class="relative w-72 h-72 md:w-96 md:h-96 rounded-full p-2 bg-gradient-to-tr from-primary to-purple-500 shadow-2xl">
                        <!-- REMPLACEZ L'URL CI-DESSOUS PAR VOTRE PROPRE IMAGE -->
                        <img src="https://placehold.co/800x800/1e293b/ffffff?text=Votre+Photo" alt="Ma photo de profil" class="w-full h-full object-cover rounded-full border-4 border-white">
                    </div>
                </div>
                
                <!-- Texte de présentation -->
                <div class="w-full md:w-1/2">
                    <h2 class="text-3xl md:text-4xl font-bold text-secondary mb-6 relative inline-block">
                        À propos de moi
                        <span class="absolute bottom-0 left-0 w-1/2 h-1 bg-primary rounded-full"></span>
                    </h2>
                    <p class="text-gray-600 mb-6 leading-relaxed text-lg">
                        Je suis un professionnel créatif avec une forte expérience dans la conception de projets visuels et techniques. J'aime transformer des idées complexes en expériences simples, belles et intuitives.
                    </p>
                    <p class="text-gray-600 mb-8 leading-relaxed text-lg">
                        Sur ce site, vous trouverez une sélection de mes meilleurs projets. Que ce soit du code, de la vidéo, ou du design, mon objectif est toujours d'apporter de la valeur et de raconter une histoire.
                    </p>
                    
                    <div class="grid grid-cols-2 gap-4">
                        <div class="bg-gray-50 p-4 rounded-lg border border-gray-100">
                            <h3 class="font-bold text-secondary text-xl">5+</h3>
                            <p class="text-gray-500 text-sm">Années d'expérience</p>
                        </div>
                        <div class="bg-gray-50 p-4 rounded-lg border border-gray-100">
                            <h3 class="font-bold text-secondary text-xl">30+</h3>
                            <p class="text-gray-500 text-sm">Projets complétés</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SECTION PORTFOLIO / VIDÉOS -->
    <section id="portfolio" class="py-20 bg-gray-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-secondary mb-4">Mon Portfolio</h2>
                <p class="text-gray-600 max-w-2xl mx-auto">Une sélection de mes travaux récents, incluant des projets web, des créations graphiques et des montages vidéos.</p>
            </div>

            <!-- Grille de projets -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                
                <!-- PROJET 1 : Article / Lien classique -->
                <div class="bg-white rounded-2xl overflow-hidden shadow-md hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 group">
                    <div class="relative h-48 overflow-hidden">
                        <img src="https://placehold.co/600x400/4f46e5/ffffff?text=Projet+Web" alt="Projet 1" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                    </div>
                    <div class="p-6">
                        <div class="text-xs font-semibold text-primary mb-2 uppercase tracking-wide">Développement Web</div>
                        <h3 class="text-xl font-bold text-secondary mb-2">Application de Gestion</h3>
                        <p class="text-gray-600 mb-4 text-sm">Une application web complète permettant aux entreprises de gérer leurs stocks en temps réel.</p>
                        <a href="#" class="inline-flex items-center text-primary font-medium hover:text-indigo-800 transition-colors">
                            Voir le projet <i class="fas fa-arrow-right ml-2 text-sm"></i>
                        </a>
                    </div>
                </div>

                <!-- PROJET 2 : Intégration Vidéo YouTube -->
                <div class="bg-white rounded-2xl overflow-hidden shadow-md hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2">
                    <!-- Conteneur vidéo responsive (aspect 16:9) -->
                    <div class="relative w-full aspect-video bg-gray-200">
                        <!-- Pour ajouter votre vidéo, remplacez l'ID de la vidéo Youtube dans le src (ex: dQw4w9WgXcQ) -->
                        <iframe class="absolute top-0 left-0 w-full h-full" 
                                src="https://www.youtube.com/embed/dQw4w9WgXcQ?si=abcdefgh" 
                                title="YouTube video player" 
                                frameborder="0" 
                                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                                allowfullscreen>
                        </iframe>
                    </div>
                    <div class="p-6">
                        <div class="text-xs font-semibold text-red-500 mb-2 uppercase tracking-wide">Montage Vidéo</div>
                        <h3 class="text-xl font-bold text-secondary mb-2">Showreel 2024</h3>
                        <p class="text-gray-600 mb-4 text-sm">Compilation de mes meilleurs plans tournés au drone et montages dynamiques pour divers clients.</p>
                        <a href="https://youtube.com" target="_blank" class="inline-flex items-center text-primary font-medium hover:text-indigo-800 transition-colors">
                            Ma chaîne YouTube <i class="fab fa-youtube ml-2 text-sm"></i>
                        </a>
                    </div>
                </div>

                <!-- PROJET 3 : Lien externe stylisé -->
                <div class="bg-white rounded-2xl overflow-hidden shadow-md hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 group">
                    <div class="relative h-48 overflow-hidden bg-gray-800 flex items-center justify-center">
                        <i class="fab fa-github text-6xl text-white group-hover:scale-110 transition-transform duration-500"></i>
                    </div>
                    <div class="p-6">
                        <div class="text-xs font-semibold text-primary mb-2 uppercase tracking-wide">Open Source</div>
                        <h3 class="text-xl font-bold text-secondary mb-2">Librairie JS</h3>
                        <p class="text-gray-600 mb-6 text-sm">Contribution à un projet Open Source sur Github, création d'une librairie d'animations légères.</p>
                        
                        <!-- Bouton stylisé complet -->
                        <a href="#" class="block w-full text-center px-4 py-3 bg-secondary text-white rounded-lg font-medium hover:bg-gray-800 transition-colors">
                            <i class="fab fa-github mr-2"></i> Code source
                        </a>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- SECTION CONTACT -->
    <section id="contact" class="py-20 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="bg-gradient-to-br from-primary to-purple-600 rounded-3xl p-8 md:p-16 text-center text-white shadow-2xl">
                <h2 class="text-3xl md:text-4xl font-bold mb-6">Prêt à collaborer ?</h2>
                <p class="text-indigo-100 mb-10 text-lg max-w-2xl mx-auto">
                    Si vous avez un projet en tête ou si vous souhaitez simplement échanger, n'hésitez pas à me contacter via mes réseaux ou par e-mail.
                </p>
                
                <div class="flex flex-wrap justify-center gap-6">
                    <!-- Bouton Email -->
                    <a href="mailto:votre.email@exemple.com" class="flex items-center px-6 py-3 bg-white text-primary rounded-full font-bold hover:bg-gray-100 transition-all transform hover:scale-105 shadow-md">
                        <i class="fas fa-envelope mr-2 text-lg"></i> M'envoyer un e-mail
                    </a>
                    
                    <!-- Réseaux Sociaux -->
                    <div class="flex gap-4 items-center">
                        <a href="#" class="w-12 h-12 bg-white/20 backdrop-blur-sm flex items-center justify-center rounded-full hover:bg-white/40 transition-all">
                            <i class="fab fa-linkedin-in text-xl"></i>
                        </a>
                        <a href="#" class="w-12 h-12 bg-white/20 backdrop-blur-sm flex items-center justify-center rounded-full hover:bg-white/40 transition-all">
                            <i class="fab fa-twitter text-xl"></i>
                        </a>
                        <a href="#" class="w-12 h-12 bg-white/20 backdrop-blur-sm flex items-center justify-center rounded-full hover:bg-white/40 transition-all">
                            <i class="fab fa-instagram text-xl"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- PIED DE PAGE -->
    <footer class="bg-secondary py-8 text-center text-gray-400">
        <div class="max-w-7xl mx-auto px-4">
            <p>&copy; <span id="year"></span> Mon Portfolio. Tous droits réservés.</p>
            <p class="text-sm mt-2">Créé avec <i class="fas fa-heart text-red-500 mx-1"></i> et hébergé sur GitHub Pages.</p>
        </div>
    </footer>

    <!-- SCRIPT POUR LES INTERACTIONS DE BASE -->
    <script>
        // Mettre à jour l'année automatiquement dans le footer
        document.getElementById('year').textContent = new Date().getFullYear();

        // Gestion du Menu Mobile
        const btn = document.getElementById('mobile-menu-btn');
        const menu = document.getElementById('mobile-menu');
        const menuLinks = menu.querySelectorAll('a');

        // Ouvrir/Fermer le menu au clic sur l'icône hamburger
        btn.addEventListener('click', () => {
            menu.classList.toggle('hidden');
        });

        // Fermer le menu mobile lorsqu'un lien est cliqué
        menuLinks.forEach(link => {
            link.addEventListener('click', () => {
                menu.classList.add('hidden');
            });
        });
    </script>
</body>
</html>
