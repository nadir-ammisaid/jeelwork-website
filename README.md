<a href="#fr">
  <img src="https://flagcdn.com/w40/fr.png" width="20" alt="Français"> Français
</a>&nbsp;&nbsp;|&nbsp;&nbsp;
<a href="#en">
  <img src="https://flagcdn.com/w40/gb.png" width="20" alt="English"> English
</a>

<hr style="margin-top: 4px; margin-bottom: 12px; border: none; border-top: 1px solid #ccc;" />

<img id="fr" src="https://flagcdn.com/w40/fr.png" width="20" alt="Français"> Français

<h1>Site vitrine Jeelwork</h1>

![Next.js](https://img.shields.io/badge/Next.js-15-black)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue)

Site web officiel de présentation de **Jeelwork Algeria**, une plateforme qui met en relation les utilisateurs avec des prestataires de services locaux qualifiés dans les 58 wilayas (villes).

Construit avec **Next.js 15** et **App Router** et **TypeScript**, le projet est optimisé pour :
- ⚡ SEO et performances (export statique, images responsives, lazy loading)
- 📱 Design responsive mobile-first
- ♿ Meilleures pratiques d'accessibilité
<!--
- 🌍 Préparation multi-langues
-->

Ce site web sert de point d'entrée public de l'écosystème Jeelwork.

<br>

**🔗 Démo en direct :** [https://www.jeelwork.com](https://www.jeelwork.com)

<br>

## 🖼️ Aperçu

![Aperçu du site Jeelwork](public/images/websitePreview.avif)

<br>

## 🚀 Démarrer

### Prérequis

Assurez-vous d'avoir installé :

- [Node.js](https://nodejs.org/) (v18+ recommandé)
- [npm](https://www.npmjs.com/) ou [pnpm](https://pnpm.io/) ou [yarn](https://yarnpkg.com/)
- Git avec accès SSH configuré si clonage via SSH

### Installation

Cloner le dépôt et installer les dépendances :

```bash
# SSH (recommandé)
git clone git@github.com:nadir-ammisaid/jeelwork-website.git

# ou HTTPS
git clone https://github.com/nadir-ammisaid/jeelwork-website.git
```

```bash
cd jeelwork-website
```

```bash
npm install
```

### Serveur de développement
Pour lancer le serveur de développement localement : 

```bash
npm run dev
```

Visitez http://localhost:3000 dans votre navigateur.


### Scripts disponibles

```bash
npm run dev          # Serveur de développement
npm run build        # Build de production  
npm run start        # Démarrer le serveur de production
npm run lint         # Lancer ESLint
npm run export       # Export statique (si configuré)
```

<br>



## 🧱 Structure du projet

Ce projet utilise **Next.js App Router** avec la structure suivante :

```
JEELWORK-website
├── .next/                               # Sortie de build Next.js (généré)
├── node_modules/                        # Dépendances npm (généré)
├── public/                              # Assets statiques (servis à la racine)
│   ├── icons/
│   ├── images/
│   ├── manifest.json                    # Manifest PWA
│   ├── robots.txt                       # Fichier robots SEO
│   └── sitemap.xml                      # Sitemap SEO
├── src/
│   ├── app/                             # App Router (Next.js 15)
│   │   ├── (legal)/                     # Pages légales statiques
│   │   │   ├── privacy-policy/
│   │   │   │   ├── page.tsx             # Page Politique de confidentialité
│   │   │   │   └── privacy-policy.css   
│   │   │   └── terms-of-use/
│   │   │       ├── page.tsx             # Page Conditions d'utilisation
│   │   │       └── terms-of-use.css     
│   │   ├── (marketing)/services/        # Pages marketing
│   │   │   ├── [slug]/                  # Route dynamique pour un service unique
│   │   │   │   └── page.tsx             # Page détail du service
│   │   │   ├── layout.tsx               
│   │   │   └── page.tsx                 # Index /services (liste des services)
│   │   ├── api/                         # Routes API
│   │   │   └── route.ts                 
│   │   ├── apple-icon.png               
│   │   ├── criticalStyles.css.ts        # CSS critique (inline comme string)
│   │   ├── criticalStyles.tsx           # Composant d'injection CSS critique
│   │   ├── favicon.ico                  
│   │   ├── globals.css                  # Styles globaux (CSS non-critique)
│   │   ├── icon.png                     
│   │   ├── layout.tsx                   # Layout racine (metadata & <head/>)
│   │   └── page.tsx                     # Page d'accueil
│   ├── components/                      # Sections UI réutilisables
│   │   ├── AreasServedSection.tsx
│   │   ├── CTASection.tsx
│   │   ├── DownloadSection.tsx
│   │   ├── FAQSection.tsx
│   │   ├── Footer.tsx
│   │   ├── Header.tsx
│   │   ├── HeroSection.tsx
│   │   ├── HowItWorksSection.tsx
│   │   ├── RecentJobbersSection.tsx
│   │   ├── ServicesSection.tsx
│   │   └── TestimonialsSection.tsx
│   ├── data/
│   │   └── services.ts                  # Catalogue de services (contenu statique)
│   └── lib/
│       └── jobbers.ts                   # Données des prestataires (ISR / mocks)
├── .eslintrc.json                       
├── .gitignore                           
├── env.d.ts                             
├── middleware.ts                        # Middleware pour les requêtes API et gestion Googlebot     
├── next-env.d.ts                        
├── next.config.ts                       # Configuration Next.js
├── package-lock.json                    
├── package.json                         
├── README.md                            # Documentation du projet
└── tsconfig.json                        
```



<br>



## ✨ Fonctionnalités

- ✅ Génération de site statique (SSG) pour un temps de chargement rapide
- 🔒 Optimisation SEO et headers de sécurité dans next.config.ts `next.config.ts`
- 📱 Design responsive mobile-first avec optimisation tablette et desktop
- 🧑‍💻 Support d'accessibilité (rôles ARIA, navigation clavier)
- ⚡ Polices et images optimisées (`next/image`, `sharp`, font-display swap)
- 🧭 Navigation par ancres avec défilement fluide


<!--
- 🌓 Support du mode sombre (via prefers-color-scheme)
- 🌍 Contenu entièrement traduit (routes français + anglais)
-->


<br>


## Auteur

Projet personnel développé en autonomie par [**Nadir AMMI SAID**](https://www.linkedin.com/in/nadir-ammisaid/), pour approfondir mes compétences en développement Next.js et TypeScript.
<br/>
🔗 Découvrez le projet en ligne : **[www.jeelwork.com](https://www.jeelwork.com)**

**💬 Vos avis m'intéressent - n'hésitez pas à me faire part de vos retours ou suggestions !**
<br/>
📩 Vous pouvez me contacter directement sur LinkedIn : **[https://www.linkedin.com/in/nadir-ammisaid/](https://www.linkedin.com/in/nadir-ammisaid/)**


## Contribution

Pour contribuer au projet :
1. **Fork** le dépôt
2. **Clone** votre fork sur votre machine locale
3. Créez une nouvelle branche pour votre fonctionnalité (`git switch -c feature/votre-fonctionnalite`)
4. **Commit** vos modifications (`git commit -m 'Ajout de fonctionnalité'`)
5. **Push** vers votre branche (`git push origin feature/votre-fonctionnalite`)
6. Créez une **Pull Request** sur le dépôt principal

**Bonnes pratiques** :
- Exécutez `npm run check` avant de pousser vos modifications
- Ajoutez des tests pour toute nouvelle fonctionnalité
- Suivez les principes SOLID pour une architecture de code propre et maintenable

<br/>
<hr id="en" style="margin-top: 4px; margin-bottom: 12px; border: none; border-top: 1px solid #ccc;" />
<br/>

<img src="https://flagcdn.com/w40/gb.png" width="20" alt="English"> English

<h1>Jeelwork Showcase Website</h1>

![Next.js](https://img.shields.io/badge/Next.js-15-black)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue)

Official showcase website for **Jeelwork Algeria**, a platform that connects users with skilled local jobbers and service providers across all 58 wilayas (cities).

Built using **Next.js 15** with the **App Router** and **TypeScript**, the project is optimized for:
- ⚡ SEO and performance (static export, responsive images, lazy loading)
- 📱 Mobile-first responsive design
- ♿ Accessibility best practices
<!--
- 🌍 Multi-language readiness
-->

This website serves as the public-facing entry point of the Jeelwork ecosystem.

<br>

**🔗 Live Demo:** [https://www.jeelwork.com](https://www.jeelwork.com)

<br>

## 🖼️ Preview

![Jeelwork Website Preview](public/images/websitePreview.avif)


<br>


## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v18+ recommended)
- [npm](https://www.npmjs.com/) or [pnpm](https://pnpm.io/) or [yarn](https://yarnpkg.com/)
- Git with SSH access configured if cloning via SSH

### Installation

Clone the repository and install dependencies:

```bash
# SSH (recommended)
git clone git@github.com:nadir-ammisaid/jeelwork-website.git

# or HTTPS
git clone https://github.com/nadir-ammisaid/jeelwork-website.git
```

```bash
cd jeelwork-website
```

```bash
npm install
```

### Development server
To run the dev server locally: 

```bash
npm run dev
```

Visit http://localhost:3000 in your browser.


### Available Scripts

```bash
npm run dev          # Development server
npm run build        # Production build  
npm run start        # Start production server
npm run lint         # Run ESLint
npm run export       # Static export (if configured)
```

<br>



## 🧱 Project Structure

This project uses **Next.js App Router** with the following structure:

```
JEELWORK-website
├── .next/                               # Next.js build output (generated)
├── node_modules/                        # npm dependencies (generated)
├── public/                              # static assets (served at root)
│   ├── icons/
│   ├── images/
│   ├── manifest.json                    # PWA manifest
│   ├── robots.txt                       # SEO robots file
│   └── sitemap.xml                      # SEO sitemap
├── src/
│   ├── app/                             # App Router (Next.js 15)
│   │   ├── (legal)/                     # Static legal pages
│   │   │   ├── privacy-policy/
│   │   │   │   ├── page.tsx             # Privacy Policy page
│   │   │   │   └── privacy-policy.css   
│   │   │   └── terms-of-use/
│   │   │       ├── page.tsx             # Terms of Use page
│   │   │       └── terms-of-use.css     
│   │   ├── (marketing)/services/        # Marketing pages
│   │   │   ├── [slug]/                  # Dynamic route for a single service
│   │   │   │   └── page.tsx             # Service detail page
│   │   │   ├── layout.tsx               
│   │   │   └── page.tsx                 # /services index (list of services)
│   │   ├── api/                         # API routes
│   │   │   └── route.ts                 
│   │   ├── apple-icon.png               
│   │   ├── criticalStyles.css.ts        # Critical CSS (inline as string)
│   │   ├── criticalStyles.tsx           # Critical CSS injection component
│   │   ├── favicon.ico                  
│   │   ├── globals.css                  # global styles (non-critical CSS)
│   │   ├── icon.png                     
│   │   ├── layout.tsx                   # Root layout (metadata & <head/>)
│   │   └── page.tsx                     # Homepage
│   ├── components/                      # Reusable UI sections
│   │   ├── AreasServedSection.tsx
│   │   ├── CTASection.tsx
│   │   ├── DownloadSection.tsx
│   │   ├── FAQSection.tsx
│   │   ├── Footer.tsx
│   │   ├── Header.tsx
│   │   ├── HeroSection.tsx
│   │   ├── HowItWorksSection.tsx
│   │   ├── RecentJobbersSection.tsx
│   │   ├── ServicesSection.tsx
│   │   └── TestimonialsSection.tsx
│   ├── data/
│   │   └── services.ts                  # Services catalog (static content)
│   └── lib/
│       └── jobbers.ts                   # Jobbers data (ISR / mocks)
├── .eslintrc.json                       
├── .gitignore                           
├── env.d.ts                             
├── middleware.ts                        # Middleware for API requests & Googlebot handling     
├── next-env.d.ts                        
├── next.config.ts                       # Next.js configuration
├── package-lock.json                    
├── package.json                         
├── README.md                            # Project documentation
└── tsconfig.json                        
```



<br>



## ✨ Features

- ✅ Static Site Generation (SSG) for fast load time
- 🔒 SEO optimization & security headers in next.config.ts `next.config.ts`
- 📱 Mobile-first responsive design with tablet & desktop optimization
- 🧑‍💻 Accessibility support (ARIA roles, keyboard navigation)
- ⚡ Optimized fonts & images (`next/image`, `sharp`, font-display swap)
- 🧭 Anchor navigation with smooth scrolling


<!--
- 🌓 Dark mode support (via prefers-color-scheme)
- 🌍 Fully translated content (French + English routes)
-->


<br>


## Author

Personal project independently developed by [**Nadir AMMI SAID**](https://www.linkedin.com/in/nadir-ammisaid/) to deepen my Next.js and TypeScript development skills.
<br/>
🔗 Discover the project online: **[www.jeelwork.com](https://www.jeelwork.com)**

**💬 Your feedback matters - don't hesitate to share your thoughts or suggestions!**
<br/>
📩 You can contact me directly on LinkedIn: **[https://www.linkedin.com/in/nadir-ammisaid/](https://www.linkedin.com/in/nadir-ammisaid/)**


## Contribution

To contribute to the project:
1. **Fork** the repository
2. **Clone** your fork to your local machine
3. Create a new branch for your feature (`git switch -c feature/your-feature`)
4. **Commit** your changes (`git commit -m 'Add feature'`)
5. **Push** to your branch (`git push origin feature/your-feature`)
6. Create a **Pull Request** on the main repository

**Best practices**:
- Run `npm run check` before pushing your changes
- Add tests for any new feature
- Follow SOLID principles for clean and maintainable code architecture


<!-- Default Next.js README 

This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

 -->