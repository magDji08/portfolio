# 📚 Guide d'Utilisation - Portfolio MAG Dev Modernisé

## 🎯 Vue d'Ensemble

Votre portfolio a été modernisé avec deux sections complètement refaites :
- **Mes Compétences** : Design en grille avec catégories
- **Mes Projets** : Cartes interactives avec système de filtres

---

## 🧩 Section "Mes Compétences"

### Structure

La section est organisée en **6 catégories** :

1. **Frontend** (6 technologies)
   - HTML, CSS, JavaScript, React, Angular, Tailwind

2. **Backend** (5 technologies)
   - Laravel, Node.js, Spring Boot, Django, MySQL

3. **Mobile** (4 technologies)
   - Flutter, GetX, Android, iOS

4. **DevOps & Outils** (5 outils)
   - Git, GitHub, Docker, VS Code, NPM

5. **Design** (4 outils)
   - Figma, Photoshop, Illustrator, UI/UX

6. **Langages de Programmation** (6 langages)
   - PHP, Python, Java, Dart, TypeScript, C++

### Personnalisation

Pour modifier les pourcentages de compétences :

```html
<div class="w-full bg-gray-200 rounded-full h-2 mb-1">
    <div class="bg-orange-600 h-2 rounded-full" style="width: 95%"></div>
    <!-- Changez la valeur width pour ajuster le niveau -->
</div>
<span class="text-xs text-gray-600">95%</span>
<!-- Changez le pourcentage affiché -->
```

### Ajouter une Nouvelle Technologie

```html
<div class="bg-white p-6 rounded-xl shadow-sm hover:shadow-lg transition-all duration-300 hover:-translate-y-1 group">
    <div class="flex flex-col items-center text-center">
        <i class="ri-ICON-NAME text-4xl text-COLOR mb-3 group-hover:scale-110 transition-transform"></i>
        <h4 class="font-semibold text-gray-900 mb-2">NOM TECHNO</h4>
        <div class="w-full bg-gray-200 rounded-full h-2 mb-1">
            <div class="bg-COLOR h-2 rounded-full" style="width: XX%"></div>
        </div>
        <span class="text-xs text-gray-600">XX%</span>
    </div>
</div>
```

---

## 🚀 Section "Mes Projets"

### Système de Filtres

Les projets peuvent être filtrés par catégories :
- **Tous** : Affiche tous les projets
- **Web** : Applications web uniquement
- **Mobile** : Applications mobiles
- **E-commerce** : Projets de boutique en ligne
- **Gestion** : Systèmes de gestion

### Ajouter un Filtre

1. Ajoutez un bouton dans la section filtres :

```html
<button class="filter-btn px-6 py-2.5 rounded-xl text-gray-700 font-medium hover:bg-white transition-all duration-300" data-filter="nouvelle-categorie">
    <i class="ri-icon-line mr-2"></i>Nouveau Filtre
</button>
```

2. Ajoutez la catégorie au projet :

```html
<div class="project-item fade-up" data-category="web mobile nouvelle-categorie">
```

### Ajouter un Nouveau Projet

```html
<div class="project-item fade-up" data-category="web mobile">
    <div class="group relative bg-white rounded-2xl overflow-hidden shadow-md hover:shadow-2xl transition-all duration-500">
        <!-- Badge optionnel -->
        <div class="absolute top-4 right-4 z-10">
            <span class="bg-blue-500 text-white text-xs font-bold px-3 py-1.5 rounded-full shadow-lg">
                <i class="ri-flashlight-fill mr-1"></i>Nouveau
            </span>
        </div>
        
        <!-- Image -->
        <div class="relative h-64 overflow-hidden">
            <img src="chemin/vers/image.jpg" alt="Description" class="w-full h-full object-cover transform group-hover:scale-110 transition-transform duration-700">
            <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-black/30 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
        </div>
        
        <!-- Contenu -->
        <div class="p-6">
            <!-- Tags de catégorie -->
            <div class="flex items-center gap-2 mb-3">
                <span class="inline-flex items-center px-3 py-1 rounded-full text-xs font-medium bg-blue-100 text-blue-700">
                    <i class="ri-window-line mr-1"></i>Web
                </span>
            </div>
            
            <!-- Titre -->
            <h3 class="text-xl font-bold text-gray-900 mb-2 group-hover:text-primary transition-colors">
                Nom du Projet
            </h3>
            
            <!-- Description -->
            <p class="text-gray-600 text-sm mb-4 line-clamp-2">
                Description courte du projet...
            </p>
            
            <!-- Technologies -->
            <div class="flex flex-wrap gap-2 mb-4">
                <span class="text-xs bg-gray-100 text-gray-700 px-2 py-1 rounded">Laravel</span>
                <span class="text-xs bg-gray-100 text-gray-700 px-2 py-1 rounded">Vue.js</span>
            </div>
            
            <!-- Bouton -->
            <a href="lien-vers-projet.html" class="inline-flex items-center gap-2 px-6 py-3 bg-primary text-white font-medium rounded-xl hover:bg-primary/90 transition-all duration-300 hover:gap-3 group/btn w-full justify-center">
                Voir le projet
                <i class="ri-arrow-right-line group-hover/btn:translate-x-1 transition-transform"></i>
            </a>
        </div>
    </div>
</div>
```

---

## 🎨 Personnalisation des Couleurs

### Badges de Projets

- **Nouveau** : `bg-blue-500` (Bleu)
- **Featured** : `bg-green-500` (Vert)
- **Premium** : `bg-purple-500` (Violet)
- **En vedette** : `bg-yellow-500` (Jaune)

### Tags de Catégories

```html
<!-- Web -->
<span class="bg-blue-100 text-blue-700">Web</span>

<!-- Mobile -->
<span class="bg-green-100 text-green-700">Mobile</span>

<!-- E-commerce -->
<span class="bg-orange-100 text-orange-700">E-commerce</span>

<!-- Gestion -->
<span class="bg-purple-100 text-purple-700">Gestion</span>
```

---

## 🔧 Modification du JavaScript

Le script de filtrage se trouve à la fin du fichier, juste avant `</body>`.

### Modifier l'Animation

```javascript
// Changer le délai entre chaque projet
setTimeout(() => {
    item.style.display = 'block';
    item.style.animation = `fadeUp 0.6s ease-out forwards`;
}, index * 100); // Changer 100 pour ajuster le délai
```

### Ajouter un Événement

```javascript
// Exemple : Compter les projets filtrés
filterButtons.forEach(button => {
    button.addEventListener('click', function() {
        // ... code existant ...
        
        // Compter les projets visibles
        const visibleProjects = document.querySelectorAll('.project-item[style*="display: block"]');
        console.log(`Nombre de projets affichés : ${visibleProjects.length}`);
    });
});
```

---

## 📱 Responsive Design

Le portfolio s'adapte automatiquement :

- **Mobile** (< 768px) : 1-2 colonnes
- **Tablet** (768px - 1024px) : 2-3 colonnes
- **Desktop** (> 1024px) : 3-6 colonnes

### Modifier la Grille

```html
<!-- Pour les compétences -->
<div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-4">
    <!-- Modifiez les valeurs : 
         grid-cols-X pour mobile
         md:grid-cols-X pour tablet
         lg:grid-cols-X pour desktop
    -->
</div>
```

---

## ✨ Animations Disponibles

### Dans le CSS

1. **fadeIn** : Apparition en fondu
2. **fadeUp** : Apparition du bas vers le haut
3. **hover:scale-110** : Agrandissement au survol
4. **hover:-translate-y-1** : Translation vers le haut

### Comment les Utiliser

```html
<!-- Ajouter fade-in -->
<div class="fade-in">Contenu</div>

<!-- Ajouter fade-up -->
<div class="fade-up">Contenu</div>

<!-- Hover effects -->
<div class="hover:scale-110 transition-transform">Contenu</div>
```

---

## 🐛 Dépannage

### Les Filtres ne Fonctionnent Pas

1. Vérifiez que le JavaScript est bien chargé
2. Vérifiez que les attributs `data-filter` et `data-category` correspondent
3. Ouvrez la console du navigateur (F12) pour voir les erreurs

### Les Animations ne s'Affichent Pas

1. Vérifiez que les classes CSS sont bien définies
2. Assurez-vous que le CSS est chargé avant le HTML
3. Testez dans un autre navigateur

### Les Icônes ne s'Affichent Pas

1. Vérifiez que RemixIcon est bien chargé :
```html
<link href="https://cdnjs.cloudflare.com/ajax/libs/remixicon/4.6.0/remixicon.min.css" rel="stylesheet">
```

2. Vérifiez le nom des classes d'icônes sur [RemixIcon.com](https://remixicon.com/)

---

## 📚 Ressources

- **Tailwind CSS** : https://tailwindcss.com/docs
- **RemixIcon** : https://remixicon.com/
- **Gradients** : https://uigradients.com/
- **Couleurs** : https://tailwindcss.com/docs/customizing-colors

---

## 🎯 Prochaines Étapes

1. ✅ Sections modernisées
2. ⏳ Ajouter vos vrais projets
3. ⏳ Mettre à jour les pourcentages de compétences
4. ⏳ Ajouter des images de projets de qualité
5. ⏳ Tester sur différents appareils
6. ⏳ Optimiser les performances
7. ⏳ Déployer en ligne

---

**Besoin d'aide ?** Consultez la documentation Tailwind CSS ou RemixIcon !

Bon développement ! 🚀
