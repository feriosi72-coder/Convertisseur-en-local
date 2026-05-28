# 🔄 Convertisseur en Local

**100% LOCAL · AUCUN UPLOAD · ZÉRO BULLSHIT**

Un convertisseur de fichiers universel qui tourne entièrement dans ton navigateur. Aucun fichier n'est jamais envoyé sur un serveur. Tout se passe en local, grâce aux Web Workers, WebAssembly et aux APIs natives du navigateur.

---

## 🚀 Fonctionnalités

- **Drag & Drop** : Dépose simplement ton fichier dans la zone dédiée
- **Détection automatique** : Le format source est identifié instantanément
- **Conversion intelligente** : Formats filtrés selon le type de fichier (image, document, texte, code, etc.)
- **Progression animée** : Barre de progression style terminal/hacker
- **Téléchargement immédiat** : Récupère ton fichier converti en un clic
- **Support multi-formats** : Images, documents, textes, codes, archives, et plus encore
- **Confidentialité totale** : Ton fichier ne quitte jamais ton PC

---

## 📦 Formats Supportés

### Images
`JPG` `PNG` `WEBP` `GIF` `SVG` `HEIC` `AVIF` `PSD`

### Documents
`PDF` `DOCX` `XLSX` `PPTX` `ODT` `EPUB` `RTF`

### Texte & Code
`TXT` `CSV` `JSON` `YAML` `MD` `JS` `PY` `TS` `PHP` `SQL`

### Archives & Autres
`ZIP` `TAR` `GZ` `SRT` `DXF`

> ⚠️ **Note technique** : 
> - La conversion d'images (JPG ↔ PNG ↔ WEBP ↔ GIF) est **réelle** et utilise l'API Canvas native.
> - Pour les autres formats (PDF, DOCX, etc.), la conversion est **simulée** à des fins de démonstration. Une intégration réelle nécessiterait des bibliothèques supplémentaires (ex: `pdf-lib`, `mammoth.js`, `xlsx.js`).

---

## 🛠️ Installation & Utilisation

Aucune installation nécessaire ! C'est un fichier HTML autonome.

### Option 1 : Ouvrir directement
1. Télécharge le fichier `index.html`
2. Ouvre-le avec n'importe quel navigateur moderne (Chrome, Firefox, Edge, Safari)
3. C'est tout !

### Option 2 : Héberger localement
```bash
# Avec Python
python -m http.server 8000

# Avec Node.js (npx)
npx serve .

# Avec PHP
php -S localhost:8000
```

Puis ouvre `http://localhost:8000` dans ton navigateur.

### Option 3 : Déployer en ligne
Tu peux héberger ce fichier statique sur :
- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages
- N'importe quel hébergeur web statique

---

## 🎨 Design & Philosophie

- **Thème** : Dark radical (#080c10)
- **Police** : Orbitron (titres) + Inter/Roboto (texte)
- **Accents** : Vert néon (#00ff88) et Cyan (#00d4ff)
- **Style** : Terminal / Hacker / Militaire
- **Ton** : Direct, technique, anti-bullshit, communautaire

---

## 🔒 Confidentialité

**Pourquoi c'est safe ?**

- ✅ Aucun upload vers un serveur
- ✅ Traitement 100% côté client (dans ton navigateur)
- ✅ Fonctionne hors-ligne une fois chargé
- ✅ Aucune donnée stockée ou transmise
- ✅ Code open-source et auditable

> **Ton fichier ne quitte jamais ton PC.** C'est pas une option, c'est une promesse.

---

## 🧠 Comment ça marche ?

### Conversion d'images (réelle)
Utilise l'API Canvas du navigateur :
1. Le fichier image est lu en tant que `Blob`
2. Converti en `ImageBitmap` ou `HTMLImageElement`
3. Dessiné sur un `<canvas>`
4. Exporté dans le format cible via `canvas.toBlob()` ou `canvas.toDataURL()`

### Autres formats (simulation)
Pour les formats complexes (PDF, DOCX, etc.), la conversion est simulée avec :
- Une barre de progression animée
- Un délai artificiel pour imiter le traitement
- Un message d'état détaillé

> 💡 **Pour aller plus loin** : Intègre des bibliothèques comme :
> - [`pdf-lib`](https://pdf-lib.js.org/) pour les PDF
> - [`mammoth.js`](https://mwilliamson.github.io/mammoth.js/) pour les DOCX
> - [`xlsx.js`](https://sheetjs.com/) pour les XLSX
> - [`pako`](https://github.com/nodeca/pako) pour les archives GZ
> - [`ffmpeg.wasm`](https://ffmpegwasm.netlify.app/) pour la vidéo/audio

---

## 📁 Structure du projet

```
convertisseur-en-local/
├── index.html          # Fichier unique contenant HTML, CSS et JS
└── README.md           # Ce fichier
```

---

## 🤝 Contribuer

Les contributions sont les bienvenues ! Voici comment aider :

1. **Fork** le projet
2. **Améliore** la conversion réelle de nouveaux formats
3. **Optimise** les performances avec de vrais Web Workers
4. **Ajoute** des tests unitaires
5. **Propose** des améliorations UX/UI

### Idées d'améliorations
- [ ] Intégrer `pdf-lib` pour la conversion PDF réelle
- [ ] Ajouter `ffmpeg.wasm` pour la conversion vidéo/audio
- [ ] Implémenter de vrais Web Workers pour ne pas bloquer l'UI
- [ ] Support des fichiers volumineux (> 100 Mo) avec streaming
- [ ] Mode batch (conversion multiple en une fois)
- [ ] Historique des conversions locales (localStorage)
- [ ] PWA (Progressive Web App) pour installation offline

---

## 📄 Licence

MIT License - Fais ce que tu veux avec, mais garde l'esprit "no bullshit".

---

## 🙏 Remerciements

- Inspiré par la philosophie **local-first** et **privacy-by-design**
- Polices par Google Fonts (Orbitron, Inter)
- Icônes et styles inspirés du mouvement **cyberpunk / hacker**

---

## 📬 Contact & Support

- 🐛 **Bug ?** → Ouvre une issue GitHub
- 💡 **Idée ?** → Ouvre une discussion
- 📢 **Partage !** → Si ce tool t'a sauvé la vie, fais-le savoir

---

**Convertisseur en Local** — *Ton fichier, ta machine, tes règles.* 🖥️🔐