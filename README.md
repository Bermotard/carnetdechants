🎶 CarnetDeChants

Bienvenue sur CarnetDeChants, une application web ultra-légère, moderne et entièrement autonome permettant de consulter et de rechercher des chants à travers plusieurs carnets thématiques.

👉 Consulter le carnet de chants en ligne

🚀 Le Projet

Ce dépôt contient le visualiseur web (Front-office) généré par le logiciel CarnetDeChant.

L'application est conçue pour être 100 % statique et portable : elle fonctionne sans aucune base de données ni serveur lourd. Elle peut être hébergée gratuitement sur GitHub Pages ou être lancée localement en faisant simplement un double-clic sur le fichier index.html (idéal pour un usage hors-ligne, sur clé USB, tablette ou smartphone).

Fonctionnalités de l'interface :

📂 Multi-carnets : Navigation intuitive entre différents recueils (Fêtes de la musique, Messes, Chants de lutte, etc.).

🔍 Recherche instantanée : Filtrage dynamique des chants par titre ou par paroles.

📝 Rendu Markdown automatique : Les chants stockés en Markdown (.md) sont interprétés à la volée pour un rendu propre et agréable à lire sur scène ou en répétition.

📱 Adapté aux mobiles (Responsive) : Conçu pour s'adapter parfaitement aux écrans de smartphones et de tablettes.

📂 Structure du Dépôt

L'application s'articule autour d'un point d'entrée unique et d'un dossier structuré de données :

carnetdechants/
├── index.html          # Point d'entrée de l'application (Visualiseur JS)
├── .nojekyll           # Force GitHub Pages à ignorer Jekyll (requis pour charger les données)
├── README.md           # Cette documentation
└── data/               # Dossier contenant tous les carnets et fichiers sources
    ├── index.json      # Fichier d'index centralisant la liste des carnets et des chants
    ├── chants/         # Bibliothèque globale de tous les chants convertis (.md)
    │   ├── Le_chant_des_partisans.md
    │   ├── Le_déserteur.md
    │   └── ...
    └── [nom_du_carnet]/ # Dossiers thématiques contenant les chants du carnet (ou pointeurs)
        ├── fetes_de_la_musique_2026/
        ├── messe_du_dimanche/
        └── ...

🛠️ Comment ça marche ?

La Collecte et la Conversion : Le logiciel de gestion importe des fichiers issus de divers formats standards (.docx, .ods, .rtf, .txt) et les convertit automatiquement au format Markdown (.md) en encodage UTF-8.

L'indexation : Un fichier central data/index.json référence l'ensemble des carnets créés et associe chaque carnet aux fichiers Markdown correspondants.

Le Rendu Dynamique : Lors de l'ouverture d'index.html dans votre navigateur, un script JavaScript léger charge le fichier index.json, construit le menu de navigation et utilise un parseur Markdown (ex: Marked.js) pour afficher les paroles sélectionnées de manière fluide.

📝 Licence

Ce projet est sous licence MIT. Vous pouvez librement l'utiliser, le modifier et le distribuer pour vos propres chorales, groupes de musique ou événements.
