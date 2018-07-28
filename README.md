<h1 align="center">
<br>
  <img src="https://raw.githubusercontent.com/thedaviddias/Front-End-Performance-Checklist/master/images/logo-front-end-performance-checklist.jpg" alt="Front-End Performance Checklist" width="170">
  <br>
    <br>
  Front-End Performance Checklist
  <br>
</h1>

<h4 align="center">🎮 La seule checklist de performance Front-end qui tourne plus rapidement que les autres.</h4>
<p align="center">Une simple règle: "Design et code avec la performance en tête"</p>

<p align="center">
  <a href="http://makeapullrequest.com">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square" alt="PRs Welcome">
  </a>
  <a href="https://gitter.im/Front-End-Checklist/Lobby?utm_source=share-link&utm_medium=link&utm_campaign=share-link">
    <img src="https://img.shields.io/badge/chat-on_gitter-008080.svg?style=flat-square" alt="Gitter">
  </a>
    <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square" alt="Licence MIT">
  </a>
</p>

<p align="center">
  <a href="#how-to-use">Comment l'utiliser</a> • <a href="#contributing">Contribuer</a> • <a href="https://www.producthunt.com/posts/front-end-performance-checklist">Product Hunt</a>
</p>
<p align="center">
    <span>Autres checklists:</span>
    <br>
  🗂 <a href="https://github.com/thedaviddias/Front-End-Checklist#---------front-end-checklist-">Front-End Checklist</a> • 💎 <a href="https://github.com/thedaviddias/Front-End-Design-Checklist#front-end-design-checklist">Front-End Design Checklist</a>
</p>

## Sommaire

1. **[HTML](#html)**
2. **[CSS](#css)**
3. **[Polices de caractère](#fonts)**
4. **[Images](#images)**
5. **[JavaScript](#javascript)**
6. **[Server](#server) (en cours)**
7. **[Frameworks JS](#js-frameworks) (en cours)**

## Introduction

La performance est un grand sujet, mais pas toujours un sujet "back-end" ou "admin": c'est également une responsabilité front-end. La Front-End Performance Checklist est une liste non exhaustive d'élément qui doit être vérifiée, ou au moins pris en compte, en tant que développeur front-end et appliqué à vos projets (personnels ou professionnels).

### Comment l'utiliser?

Pour chaque règle, vous aurez un paragraphe expliquant *pourquoi* cette règle est importante et *comment* vous pouvez la corriger. Pour plus d'informations, vous trouverez des liens qui pointent vers des 🛠 outils, 📖 articles ou 📹 videos qui peuvent compléter cette checklist.

Tous les items dans la **Front-End Performance Checklist** sont essentiels pour atteindre le plus haut score de performance mais vous trouvez un indicateur pour vous aider à éventuellement prioriser quelques règles plutôt que d'autres. Il y a 3 niveaux de priorités / impact: 

* ![Low][low] signifie que l'item a une priorité ou impact **faible** sur votre projet.
* ![Medium][medium] signifie que l'item a une priorité ou impact **moyen** sur votre projet. Vous ne devriez pas ignorer cet item.
* ![High][high] signifie que l'item a un **très grand** impact sur votre projet. Vous ne pouvez pas passer à côté de cette règle et devriez apporter les corrections au plus vite.

### Outils de performance

Liste d'outils que vous pouvez utiliser pour tester et surveiller votre site ou application:
 
 * 🛠 [WebPagetest - Website Performance and Optimization Test](https://www.webpagetest.org/)
 * 🛠 ☆ [Dareboost: Website Speed Test and Website Analysis](https://www.dareboost.com/) (utilisez le coupon WPCDD20 pour -20%)
 * 🛠 [GTmetrix | Website Speed and Performance Optimization](https://gtmetrix.com/)
 * 🛠 [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/)
 * 🛠 [Pingdom Website Speed Test](https://tools.pingdom.com)
 * 📖 [Pagespeed - The tool and optimization guide](https://varvy.com/pagespeed/)
 * 📖 [Make the Web Faster | Google Developers](https://developers.google.com/speed/)
 * 🛠 [Sitespeed.io - Welcome to the wonderful world of Web Performance](https://www.sitespeed.io/)
 * 🛠 [Calibre](https://calibreapp.com/)
 * 🛠 [Website and Server Uptime Monitoring - Pingdom](https://www.pingdom.com/product/uptime-monitoring/) ([Free Signup Link](https://www.pingdom.com/free))
 * 🛠 [Uptime Robot](https://uptimerobot.com)
 
### Références

 * 📖 [The Cost Of JavaScript - YouTube](https://www.youtube.com/watch?v=_bzqF05xsC4)
 * 📖 [Get Started With Analyzing Runtime Performance  |  Google Developers](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/)
 * 📖 [State of the Web | 2018_01_01](https://httparchive.org/reports/state-of-the-web?start=2018_01_01)
 * 📖 [Page Weight Doesn't Matter](https://www.speedshop.co/2015/11/05/page-weight-doesnt-matter.html)
---

## HTML

![html]

- [ ] **Minifier HTML:** ![medium] Le code HTML est minifié, les commentaires, espaces blancs et les nouvelles lignes sont enlevées sur les fichiers de production.

    *Pourquoi:*
    > Enlever tous les espaces, commentaires et sauts de lignes non nécessaires vont réduire la taille de votre HTML et diminuer le temps de chargement de votre page, et bien évidemment réduire le temps de download à vos utilisateurs.

    *Comment:*
    > ⁃ La plupart des frameworks ont des plugins qui facilitent la minification des pages. Vous pouvez utiliser quelques modules NPM qui feront le travail automatiquement.

    * 🛠 [HTML minifier | Minify Code](http://minifycode.com/html-minifier/)
    * 📖 [Experimenting with HTML minifier — Perfection Kills](http://perfectionkills.com/experimenting-with-html-minifier/#use_short_doctype)

- [ ] **Enlever les commentaires inutiles:** ![low] Assurez-vous que les commentaires soient enlevés de vos pages.

    *Pourquoi:*
    > Les commentaires ne sont pas très utiles aux utilisateurs, alors ils devraient être enlevés des fichiers de production. Le seul cas où vous voudriez garder les commentaires serait de garder l'origine d'une librairie.

    *Comment:*
    > ⁃ La plupart du temps, les commentaires peuvent être retirés en utilisant un plugin pour minifier le code HTML.

 * 🛠 [remove-html-comments - npm](https://www.npmjs.com/package/remove-html-comments)

- [ ] **Enlever les attributs inutiles:** ![low] Les attributs type comme `type="text/javascript"` ou `type="text/css"` ne sont plus nécessaires et devraient être enlevés.

    ```html
    <!-- Avant HTML5 -->
    <script type="text/javascript">
        // Javascript code
    </script>

    <!-- Aujourd'hui -->
    <script>
        // Javascript code
    </script>
    ```

    *Pourquoi:*
    > L'attribut type n'est plus nécessaire car l'HTML5 considère text/css et text/javascript par défaut. Le code non utilisé devrait être enlevé comme ils ajoutent du poids inutilement à vos pages.

    *Comment:*
    > ⁃ Assurez-vous que tous vos `<link>` et `<script>` tags n'aient pas d'attribut type.

    * 📖 [The Script Tag | CSS-Tricks](https://css-tricks.com/the-script-tag/)
   
- [ ] **Placez les tags CSS toujours avant les tags JavaScript:** ![high] Assurez-vous que votre CSS est toujours chargé avant le code JavaScript.

    ```html
    <!-- Non recommandé -->
    <script src="jquery.js"></script>
    <script src="foo.js"></script>
    <link rel="stylesheet" href="foo.css"/>

    <!-- Recommandé -->
    <link rel="stylesheet" href="foo.css"/>
    <script src="jquery.js"></script>
    <script src="foo.js"></script>
    ```

    *Pourquoi:*
    > Avoir les tags CSS qui se chargent avant le JavaScript permet d'avoir un téléchargement en parallèle qui augmente le temps de rendu.

    *Comment:*
    > ⁃ Assurez-vous que `<link>` et `<style>` dans votre balise `<head>` est toujours avant `<script>`.

    * 📖 [Ordering your styles and scripts for pagespeed](https://varvy.com/pagespeed/style-script-order.html)

- [ ] **Minimisez le nombre d'iframes:** ![high] Utilisez des iframes uniquement si vous n'avez pas d'autres moyens techniques. Essayez d'éviter le plus possible les iframes.

**[⬆ Retour au sommaire](#table-of-contents)**

## CSS

![css]

- [ ] **Minification:** ![high] Tous les fichiers CSS doivent être minifiés, commentaires, espaces blancs et les nouvelles lignes sont supprimées des fichiers de production.

    *Pourquoi:*
    > Quand les fichiers CSS sont minifiés, le contenu est chargé plus rapidement et moins de donnés est envoyé au client. C'est important de toujours minifier les fichiers CSS en production. C'est bénéfique pour l'utilisateur tout comme n'importe quel business qui veut un faible usage en bande passante et un usage de ressources moins important.

    *Comment:*
    > ⁃ Utilisez des outils pour minifier vos fichiers automatiquement avant et pendant le processus de build & de déploiement.

    * 🛠 [cssnano: A modular minifier based on the PostCSS ecosystem. - cssnano](https://cssnano.co/)
    * 🛠 [@neutrinojs/style-minify - npm](https://www.npmjs.com/package/@neutrinojs/style-minify)

- [ ] **Concaténation:** ![medium] Les fichiers CSS sont concaténés en un seul fichier. *(Pas toujours valide pour HTTP/2)*

    ```html

    <!-- Non recommandé -->
    <script src="foo.js"></script>
    <script src="ajax.js"></script>

    <!-- Recommandé -->
    <script src="combined.js"></script>
    ```

    *Pourquoi:*
    > Si vous utilisez toujours HTTP/1, vous devriez quand même contacténer vos fichiers, c'est moins le cas si vous utilisez HTTP/2 (des tests doivent être faits).

    *Comment:*
    > ⁃ Utilisez un outil en ligne ou un plugin avant ou pendant le processus de build ou déploiement pour concaténer vos fichiers.
    ⁃ Assurez-vous bien évidemment que la concaténation ne casse rien dans votre projet.

    * 📖 [HTTP: Optimizing Application Delivery - High Performance Browser Networking (O'Reilly)](https://hpbn.co/optimizing-application-delivery/#optimizing-for-http2)
    * 📖 [Performance Best Practices in the HTTP/2 Era](https://deliciousbrains.com/performance-best-practices-http2/)

- [ ] **Non-bloquant:** ![high] Les fichiers CSS doivent être non bloquant pour ne pas empêcher le DOM de mettre trop de temps à se charger.

    ```html
    <link rel="preload" href="global.min.css" as="style" onload="this.rel='stylesheet'">
    <noscript><link rel="stylesheet" href="global.min.css"></noscript>
    ```

    *Pourquoi:*
    > Les fichiers CSS peuvent bloquer le chargement de la page et délayer le rendu de celle-ci. L'utilisation de `preload` peut charger les fichiers CSS avant que le navigateur ne commence à afficher le contenu de votre page.

    *Comment:*
    > ⁃ Vous devez ajouter un attribut `rel` avec la valeur `preload` et ajouter `as="style"` sur l'element `<link>`.

    * 📖 [loadCSS by filament group](https://github.com/filamentgroup/loadCSS)
    * 📖 [Example of preload CSS using loadCSS](https://gist.github.com/thedaviddias/c24763b82b9991e53928e66a0bafc9bf)
    * 📖 [Preloading content with rel="preload"](https://developer.mozilla.org/en-US/docs/Web/HTML/Preloading_content)
    * 📖 [Preload: What Is It Good For? — Smashing Magazine](https://www.smashingmagazine.com/2016/02/preload-what-is-it-good-for/)

- [ ] **Taille des classes CSS:** ![low] La longueur des classes peut avoir (un tout petit) impact sur votre HTML et vos fichiers CSS.

    *Pourquoi:*
    > Même si les impacts sur les performances sont discutables, prendre une décision sur une nomenclature sur votre projet peut avoir un impact sur la maintenabilité de vos fichiers de style. Si vous utilisez BEM, dans certains cas, vous pouvez vous retrouver avec des classes qui ont plus de caractères qu'elles ont en besoin. C'est toujours important de bien choisir les noms et les namespaces.

    *Comment:*
    > ⁃ En imposant une limite dans le nombre de caractères serait intéressant pour certaines personnes, mais en s'assurant de diviser votre site en composants peut aider à réduire le nombre de classes (et de déclarations), ainsi que la longueur des classes.

    * 🛠 [long vs short class · jsPerf](https://jsperf.com/long-vs-short-class)

- [ ] **CSS non utilisé:** ![medium] Enlever tous les sélecteurs CSS non utilisés.

    *Pourquoi:*
    > Enlever tous les sélecteurs CSS non utilisés peut réduire la taille de vos fichiers et réduire le temps de chargement de vos assets.

    *Comment:*
    > ⁃ ⚠️ Toujours vérifier si votre framework CSS que vous utilisez n'a pas déjà une classe qui fait la même chose.

    * 🛠 [UnCSS Online](https://uncss-online.com/)
    * 🛠 [PurifyCSS](https://github.com/purifycss/purifycss)
    * 🛠 [PurgeCSS](https://github.com/FullHuman/purgecss)
    * 🛠 [Chrome DevTools Coverage](https://developers.google.com/web/updates/2017/04/devtools-release-notes#coverage)

* [ ] **CSS critique:** ![high] Le CSS critique (ou "au-dessus de la ligne de flottaison") collecte tout le CSS utilisé pour render la portion visible de la page. Il est inclus avant l'appel principal de votre CSS et entre `<style></style>` dans une seule ligne (minifié si possible).

    *Pourquoi:*
    > L'ajout d'un CSS critique en une ligne aide à augmenter la vitesse de rendu de vos pages en réduisant le nombre de requêtes serveur.

    *Comment:*
    > ⁃ Générez le CSS critique avec des outils en ligne ou des plugins comme celui qu'Addy Osmani à développé

    * 📖 [Understanding Critical CSS](https://www.smashingmagazine.com/2015/08/understanding-critical-css/)
    * 🛠 [Critical by Addy Osmani on GitHub](https://github.com/addyosmani/critical) automates this.
    * 📖 [Inlining critical CSS for better web performance | Go Make Things](https://gomakethings.com/inlining-critical-css-for-better-web-performance/)
     * 🛠 [Critical Path CSS Generator - Prioritize above the fold content :: SiteLocity](https://www.sitelocity.com/critical-path-css-generator)

- [ ] **CSS intégré ou inline:** ![high] Evitez d'utiliser du CSS integré ou inline dans votre `<body>` *(Non valide pour HTTP/2)*

    *Pourquoi:*
    > L'une des premières raisons c'est qu'il s'agit d'une bonne pratique de **séparer le contenu du design**. Ça aide également à avoir une meilleure maintenabilité du code et garde votre site accessible. Mais question performance, cela décroît la taille de votre fichier HTML et réduit le temps de chargement.

    *Comment:*
    > ⁃ Utilisez toujours un fichier de style externe ou intégrez le CSS dans le `<head>` (et suivez les autres règles de performance)

    * 📖 [Observe CSS Best Practices: Avoid CSS Inline Styles](https://www.lifewire.com/avoid-inline-styles-for-css-3466846)

- [ ] **Analysez la compléxité de votre style:** ![high] Analyser votre style peut vous aider à détecter des problèmes, redondances et des doublons dans vos sélecteurs CSS.

    *Pourquoi:*
    > Quelquesfois vous avez des redondances ou des erreurs de validation dans votre CSS, analysez vos fichiers CSS et enlevez ces complexifications peuvent vous aider à accélérer vos fichiers CSS (car votre navigateur va les lire plus rapidement)

    *Comment:*
    > ⁃ Votre CSS doit être organisé, utiliser un préprocesseur CSS peut vous aider avec ça. Quelques outils en ligne listés en dessous peuvent également vous aider à analyser votre code.

    * 🛠 [TestMyCSS | Optimize and Check CSS Performance](http://www.testmycss.com/)
    * 📖 [CSS Stats](https://cssstats.com/)
    * 🛠 [macbre/analyze-css: CSS selectors complexity and performance analyzer](https://github.com/macbre/analyze-css)

**[⬆ Retour au sommaire](#table-of-contents)**

## Polices de caractère

![fonts]

* 📖 [A Book Apart, Webfont Handbook](https://abookapart.com/products/webfont-handbook)

- [ ] **Webfont formats:** ![medium] Vous utilisez WOFF2 dans votre projet ou application.

    *Pourquoi:*
    > Selon Google, le format de compression WOFF 2.0 Web Font offre un gain moyen de 30% comparé à WOFF 1.0. C'est alors bien d'utiliser WOFF 2.0, WOFF 1.0 en fallback puis TTF.

    *Comment:*
    > ⁃ Vérifiez avant d'acheter une nouvelle police de caracètre que le fournisseur vous donne le format WOFF2. Si vous utilisez une police de caractère gratuite, vous pouvez toujours utiliser Font Squirrel pour générer les autres formats.

    * 📖 [WOFF 2.0 – Learn more about the next generation Web Font Format and convert TTF to WOFF2](https://gist.github.com/sergejmueller/cf6b4f2133bcb3e2f64a)
    * 🛠 [Create Your Own @font-face Kits » Font Squirrel](https://www.fontsquirrel.com/tools/webfont-generator)
    * 🛠 [IcoMoon App - Icon Font, SVG, PDF & PNG Generator](https://icomoon.io/app/)
    * 📖 [Using @font-face | CSS-Tricks](https://css-tricks.com/snippets/css/using-font-face/?ref=frontendchecklist)
    * 📖 [Can I use... WOFF2](https://caniuse.com/#feat=woff2)

- [ ] **Utilisez `preconnect` pour charger vos polices de caractère plus rapidement:** ![medium]

    ```html
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    ```

    *Pourquoi:*
    > Quand vous arrivez sur un site web, votre appareil a besoin de savoir où votre site se trouve et dans quel serveur il a besoin de se connecter. Votre navigateur contacte alors un serveur DNS et attends pour son retour avant de charger les ressources (fonts, fichiers CSS...).

    *Comment:*
    > ⁃ Avant de pré-charger vos webfonts, utilisez webpagetest pour évalier votre site internet.
    ⁃ Recherchez les recherches DNS couleur sarcelle et notez l'hôte qui est demandé.
    ⁃ Prefetch vos webfonts dans votre `<head>` et ajoutez éventuellement ces noms d'hôtes que vous devriez préférez aussi.

    * 📖 [Faster Google Fonts with Preconnect - CDN Planet](https://www.cdnplanet.com/blog/faster-google-webfonts-preconnect/)
    * 📖 [Make Your Site Faster with Preconnect Hints | Viget](https://www.viget.com/articles/make-your-site-faster-with-preconnect-hints/)
    * 📖 [Ultimate Guide to Browser Hints: Preload, Prefetch, and Preconnect - MachMetrics Speed Blog](https://www.machmetrics.com/speed-blog/guide-to-browser-hints-preload-preconnect-prefetch/)
    * 📖 [A Comprehensive Guide to Font Loading Strategies—zachleat.com](https://www.zachleat.com/web/comprehensive-webfonts/#font-face)

- [ ] **Webfont size:** ![medium] Les tailles Webfont ne dépassent pas 300kb (toutes les variantes incluses)

 * 📖 [Font Bytes - Page Weight](https://httparchive.org/reports/page-weight#bytesFont)
 
- [ ] **Empêche le Flash de Texte Invisible:** ![medium] Évitez le texte transparent jusqu'à ce que Webfont soit chargé

 * 📖 [`font-display` for the Masses](https://css-tricks.com/font-display-masses/)
 * 📖 [CSS font-display: The Future of Font Rendering on the Web](https://www.sitepoint.com/css-font-display-future-font-rendering-web/)

**[⬆ Retour au sommaire](#table-of-contents)**

## Images

![images]

 * 📖 [Image Bytes in 2018](https://httparchive.org/reports/page-weight#bytesImg)

* [ ] **Optimisation des images:** ![high] Vos images sont optimisées, compressées sans impact direct pour l'utilisateur final.

    *Pourquoi:*
    > Les images optimisées se chargent plus rapidement dans votre navigateur et consomment moins de données.

    *Comment:*
    > ⁃ Essayez d'utiliser les effets CSS3 quand c'est possible (au lieu d'une petite image)
    ⁃ Lorsque cela est possible, utilisez des polices au lieu du texte codé dans vos images
    ⁃ Utilisez SVG
    ⁃Utilisez un outil et spécifiez une compression de niveau inférieure à 85.

    * 📖 [Image Optimization | Web Fundamentals | Google Developers](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization)
    * 🛠 [TinyJPG – Compress JPEG images intelligently](https://tinyjpg.com/)
    * 🛠 [Kraken.io - Online Image Optimizer](https://kraken.io/web-interface)
    * 🛠 [Compressor.io - optimize and compress JPEG photos and PNG images](https://compressor.io/compress)
    * 🛠 [Cloudinary - Image Analysis Tool](https://webspeedtest.cloudinary.com)


* [ ] **Format d'images:** ![high] Choisissez votre format d'image de manière appropriée.

    *Pourquoi:*
    > Pour vous assurer que vos images ne ralentissent pas votre site Web, choisissez le format qui s'adapte au besoin que vous en faîtes

    *Comment:*
    > ⁃ Utilisez [Lighthouse](https://developers.google.com/web/tools/lighthouse/) pour identifier quelles images peuvent éventuellement utiliser **les formats next-gen** (comme JPEG 2000m JPEG XR ou WebP)
    ⁃ Comparez les différents formats, parfois l'utilisation de PNG8 est mieux que PNG16, parfois ce n'est pas le cas.

    * 📖 [Serve Images in Next-Gen Formats  |  Tools for Web Developers  |  Google Developers](https://developers.google.com/web/tools/lighthouse/audits/webp)
    * 📖 [What Is the Right Image Format for Your Website? — SitePoint](https://www.sitepoint.com/what-is-the-right-image-format-for-your-website/)
     * 📖 [PNG8 - The Clear Winner — SitePoint](https://www.sitepoint.com/png8-the-clear-winner/)
     * 📖 [8-bit vs 16-bit - What Color Depth You Should Use And Why It Matters - DIY Photography](https://www.diyphotography.net/8-bit-vs-16-bit-color-depth-use-matters/)

- [ ] **UtiliseZ l'image vectorielle vs bitmap:** ![medium] Préférez utiliser une image vectorielle plutôt que des images bitmap (si possible).

    *Pourquoi:*
    > Les images vectorielles (SVG) ont tendance à être plus petites que les images et les SVG sont sensibles et s'adaptent parfaitement. Ces images peuvent être animées et modifiées par CSS.

* [ ] **Dimensions des images:** ![medium] Définissez les attributs `width` et` height` sur l'élément `<img>` si la taille finale de l'image rendue est connue.

    *Pourquoi:*
    > Si la hauteur et la largeur sont définies, l'espace requis pour l'image est réservé lorsque la page est chargée. Toutefois, sans ces attributs, le navigateur ne connaît pas la taille de l'image et ne peut pas lui réserver l'espace approprié. L'effet sera que la mise en page changera pendant le chargement (pendant le chargement des images).

* [ ] **Évitez d'utiliser des images Base64:** ![medium] Vous pourriez éventuellement convertir des images minuscules en base64 mais ce n'est pas la meilleure pratique.

    * 📖 [Base64 Encoding & Performance, Part 1 and 2 by Harry Roberts](https://csswizardry.com/2017/02/base64-encoding-and-performance/)
    * 📖 [A closer look at Base64 image performance – The Page Not Found Blog](http://www.andygup.net/a-closer-look-at-base64-image-performance/)
    * 📖 [When to base64 encode images (and when not to) | David Calhoun](https://www.davidbcalhoun.com/2011/when-to-base64-encode-images-and-when-not-to/)
   * 📖 [Base64 encoding images for faster pages | Performance and seo factors](https://varvy.com/pagespeed/base64-images.html)

* [ ] **Lazy loading:** ![medium] Images sont lazyloaded (Un noscript fallback est toujours fourni).

    *Pourquoi:*
    > Cela améliorera le temps de réponse de la page en cours et évitera de charger des images inutiles dont l'utilisateur n'a pas besoin.

    *Comment:*
    > ⁃ Utilisez [Lighthouse](https://developers.google.com/web/tools/lighthouse/) pour identifier le nombre d'images **hors écran**.
    ⁃ Utilisez un plugin JavaScript comme pour lazyload vos images.

    * 🛠 [verlok/lazyload: Github](https://github.com/verlok/lazyload)
    * 🛠 [aFarkas/lazysizes: Github](https://github.com/aFarkas/lazysizes/)
    * 📖 [Lazy Loading Images and Video  |  Web Fundamentals  |  Google Developers](https://developers.google.com/web/fundamentals/performance/lazy-loading-guidance/images-and-video/)
    * 📖 [5 Brilliant Ways to Lazy Load Images For Faster Page Loads - Dynamic Drive Blog](http://blog.dynamicdrive.com/5-brilliant-ways-to-lazy-load-images-for-faster-page-loads/)

* [ ] **Responsive images:** ![medium] Assurez-vous de diffuser des images proches de votre taille d'affichage.

    *Pourquoi:*
    > Les petits appareils n'ont pas besoin d'images plus grandes que leur fenêtre d'affichage. Il est recommandé d'avoir plusieurs versions d'une image sur différentes tailles.

    *Comment:*
    > ⁃ Créez différentes tailles d'image pour les appareils que vous souhaitez cibler.
    ⁃ Utilisez `srcset` et` picture` pour fournir plusieurs variantes de chaque image.

     * 📖 [Responsive images - Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)

**[⬆ Retour au sommaire](#table-of-contents)**

## JavaScript

![javascript]

- [ ] **JS Minification:** ![high] Tous les fichiers JavaScript sont minifiés, les commentaires, les espaces blancs et les nouvelles lignes sont supprimés des fichiers de production *(toujours valide si vous utilisez HTTP / 2)*.

    *Pourquoi:*
    > La suppression de tous les espaces, commentaires et ruptures inutiles réduira la taille de vos fichiers JavaScript et accélérera le chargement des pages de votre site et, de toute évidence, allégera le téléchargement pour votre utilisateur.

    *Comment:*
    > ⁃ Utilisez les outils suggérés ci-dessous pour réduire automatiquement vos fichiers avant ou pendant votre build ou votre déploiement.

    * 📖 [uglify-js - npm](https://www.npmjs.com/package/uglify-js)
    * 📖 [Short read: How is HTTP/2 different? Should we still minify and concatenate?](https://scaleyourcode.com/blog/article/28)

* [ ] **Pas de JavaScript à l'intérieur:** ![medium] * (Valable uniquement pour le site Web) * Évitez d'avoir plusieurs codes JavaScript intégrés au milieu de votre corps. Regroupe votre code JavaScript dans des fichiers externes ou éventuellement dans le `<head>` ou à la fin de votre page (avant `</ body>`).

    *Pourquoi:*
    > Placer du code incorporé JavaScript directement dans votre `<body>` peut ralentir votre page car elle se charge pendant la construction du DOM. La meilleure option est d'utiliser des fichiers externes avec `async` ou` defer` pour éviter de bloquer le DOM. Une autre option consiste à placer des scripts dans votre `<head>`. La plupart du temps, le code d'analyse ou le petit script qui doit être chargé avant que le DOM arrive au traitement principal.

    *Comment:*
    > ⁃ Assurez-vous que tous vos fichiers sont chargés en utilisant `async` ou` defer` et décidez sagement du code que vous devrez injecter dans votre `<head>`.

     * 📖 [11 Tips to Optimize JavaScript and Improve Website Loading Speeds](https://www.upwork.com/hiring/development/11-tips-to-optimize-javascript-and-improve-website-loading-speeds/)

* [ ] **JavaScript non bloquant:** ![high] Les fichiers JavaScript sont chargés de manière asynchrone en utilisant `async` ou différés en utilisant l'attribut` defer`.

    ```html
    <!-- Defer Attribute -->
    <script defer src="foo.js">

    <!-- Async Attribute -->
    <script async src="foo.js">
    ```

    *Pourquoi:*
    > JavaScript bloque l'analyse normale du document HTML, donc quand l'analyseur atteint une balise `<script>` (en particulier dans le `<head>`), il arrête de l'extraire et de l'exécuter. Ajouter `async` ou` defer` est fortement recommandé si vos scripts sont placés en haut de votre page mais moins précieux si vous êtes juste avant votre balise `</ body>`. Mais il est recommandé de toujours utiliser ces attributs pour éviter tout problème de performance.

    *Comment:*
    > ⁃ Ajoutez `async` (si le script ne repose pas sur d'autres scripts) ou` defer` (si le script s'appuie sur un script asynchrone ou sur lequel il s'appuie) comme attribut de votre balise de script.
    ⁃ Si vous avez de petits scripts, utilisez peut-être un script en ligne placé au-dessus des scripts asynchrones.

    * 📖 [Remove Render-Blocking JavaScript](https://developers.google.com/speed/docs/insights/BlockingJS)

* [ ] **Bibliothèques JS optimisées et mises à jour:** ![medium] Toutes les bibliothèques JavaScript utilisées dans votre projet sont nécessaires (préférez le Javascript de Vanilla pour des fonctionnalités simples), mises à jour à leur dernière version et ne surchargez pas votre JavaScript avec des méthodes inutiles.

    *Pourquoi:*
    > La plupart du temps, les nouvelles versions viennent avec l'optimisation et la correction de sécurité. Vous devriez utiliser le code le plus optimisé pour accélérer votre projet et vous assurer que vous ne ralentirez pas votre site ou votre application sans plugin obsolète.

    *Comment:*
    > ⁃ Si votre projet utilise des paquets NPM, [npm-check](https://www.npmjs.com/package/npm-check) est une bibliothèque assez intéressante pour mettre à jour vos bibliothèques.

    * 📖 [You may not need jQuery](http://youmightnotneedjquery.com/)
    * 📖 [Vanilla JavaScript for building powerful web applications](https://plainjs.com/)

- [ ] **Vérifier la limite de taille des dépendances:** ![low] Assurez-vous d'utiliser judicieusement les bibliothèques externes, la plupart du temps, vous pouvez utiliser une bibliothèque plus légère pour une même fonctionnalité.

    *Pourquoi:*
    > Vous pourriez être tenté d'utiliser l'un des 745 000 paquets que vous pouvez trouver sur [npm](https://www.npmjs.com/), mais vous devez choisir le meilleur package pour vos besoins. Par exemple, MomentJS est une bibliothèque impressionnante mais avec beaucoup de méthodes que vous n'utiliserez jamais, c'est pourquoi Day.js a été créé. C'est juste 2kB vs 16.4kB gz pour Moment.

    *Comment:*
    > ⁃ Comparez et choisissez toujours la bibliothèque la meilleure et la plus légère pour vos besoins. Vous pouvez également utiliser des outils tels que [npm trends](http://www.npmtrends.com/) pour comparer les téléchargements de packages NPM ou [Bundlephobia](https://bundlephobia.com/) pour connaître la taille de vos dépendances.

    * 🛠 [ai/size-limit: Prevent JS libraries bloat. If you accidentally add a massive dependency, Size Limit will throw an error.](https://github.com/ai/size-limit)
    * 📖 [webpack-bundle-analyzer - npm](https://www.npmjs.com/package/webpack-bundle-analyzer)
    * 📖 [Size Limit: Make the Web lighter — Martian Chronicles, Evil Martians’ team blog](https://evilmartians.com/chronicles/size-limit-make-the-web-lighter)

- [ ] **Profilage JavaScript:** ![medium] Vérifiez les problèmes de performance dans vos fichiers JavaScript (et CSS aussi).

    *Pourquoi:*
    > La complexité JavaScript peut ralentir les performances d'exécution. Identifier ces problèmes possibles est essentiel pour offrir la meilleure expérience utilisateur.

    *Comment:*
    > ⁃ Utilisez l'outil Timeline de Chrome pour évaluer les événements de scripts et trouver celui qui peut prendre trop de temps.

     * 📖 [Speed Up JavaScript Execution  |  Tools for Web Developers  |  Google Developers](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution)
    * 📖 [JavaScript Profiling With The Chrome Developer Tools — Smashing Magazine](https://www.smashingmagazine.com/2012/06/javascript-profiling-chrome-developer-tools/)
    * 📖 [How to Record Heap Snapshots  |  Tools for Web Developers  |  Google Developers](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots)
    * 📖 [Chapter 22 - Profiling the Frontend - Blackfire](https://blackfire.io/docs/book/22-frontend-profiling)

**[⬆ Retour au sommaire](#table-of-contents)**

## Serveur

![server-side]

- [ ] **Poids de la page <1500 Kb (idéalement <500 KB):** ![high] Réduisez autant que possible la taille de votre page et de vos ressources.

    *Pourquoi:*
    > Idéalement, vous devriez essayer de cibler <500 KB, mais l'état des sites Web montre que la médiane des Kilobytes est d'environ 1500 KB (même sur mobile). En fonction de vos utilisateurs cibles, de vos connexions, de vos appareils, il est important de réduire autant que possible le nombre total de kilooctets pour avoir la meilleure expérience utilisateur possible.

    *Comment:*
    > ⁃ Toutes les règles de Front-End Performance Checklist vous aideront à réduire autant que possible vos ressources et votre code.

    * 📖 [Page Weight](https://httparchive.org/reports/page-weight#bytesTotal)
    * 🛠 [What Does My Site Cost?](https://whatdoesmysitecost.com/)
    * 🛠 [web - Measure full page size in Chrome DevTools - Stack Overflow](https://stackoverflow.com/questions/38239980/measure-full-page-size-in-chrome-devtools)

- [ ] **Temps de chargement de la page <3 secondes:** ![high] Réduisez autant que possible vos temps de chargement de la page pour livrer rapidement votre contenu à vos utilisateurs.

    *Pourquoi:*
    > Plus votre site Web ou votre application est rapide, moins vous avez de probabilité de rebondir, en d'autres termes vous avez moins de chances de perdre votre utilisateur ou futur client. Suffisamment de recherches sur le sujet prouvent ce point.
    
    *Comment:*
    >  ⁃ Utilisez des outils en ligne comme [Page Speed Insight](https://developers.google.com/speed/pagespeed/insights/) ou [WebPageTest](https://www.webpagetest.org/) pour analyser ce qui pourrait vous ralentir et utiliser le Front-End Performance Checklist pour améliorer vos temps de chargement.

    * 🛠 [Compare your mobile site speed](https://www.thinkwithgoogle.com/feature/mobile/)
    * 🛠 [Test Your Mobile Website Speed and Performance - Think With Google](https://testmysite.thinkwithgoogle.com/?_ga=1.155316027.1489996091.1482187369)
    * 📖 [Average Page Load Times for 2018 - How does yours compare? - MachMetrics Speed Blog](https://www.machmetrics.com/speed-blog/average-page-load-times-websites-2018/)

- [ ] **Temps au premier octet <1,3 seconde:** ![high] Réduisez autant que vous le pouvez le temps que votre navigateur attend avant de recevoir des données.

    * 📖 [What is Waiting (TTFB) in DevTools, and what to do about it](https://scaleyourcode.com/blog/article/27)
    * 📖 [Monitoring your servers with free tools is easy](https://scaleyourcode.com/blog/article/7)
    * 🛠 [Global latency testing tool](https://latency.apex.sh)

* [ ] **Taille du cookie:** ![medium] Si vous utilisez des cookies, assurez-vous que chaque cookie ne dépasse pas 4096 bytes et que votre nom de domaine ne contient pas plus de 20 cookies.

    *Pourquoi:*
    > les cookies sont échangés dans les en-têtes HTTP entre les serveurs Web et les navigateurs. Il est important de garder la taille des cookies aussi faible que possible afin de minimiser l'impact sur le temps de réponse de l'utilisateur.

    *Comment:*
    > ⁃ Éliminer les cookies inutiles

    * 📖 [Cookie specification: RFC 6265](https://tools.ietf.org/html/rfc6265)
    * 📖 [Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
    * 🛠 [Browser Cookie Limits](http://browsercookielimits.squawky.net/)
    * 📖 [Website Performance: Cookies Don't Taste So Good - Monitis Blog](http://www.monitis.com/blog/website-performance-cookies-dont-taste-so-good/)
    * 📖 [Google's Web Performance Best Practices #3: Minimize Request Overhead - GlobalDots Blog](https://www.globaldots.com/googles-web-performance-best-practices-3-minimize-request-overhead/)

- [ ] **Minimiez le nombre de requête HTTP:** ![high] Assurez-vous toujours que chaque requête vers un fichier est essentiel pour votre site ou application.

- [ ] **Utilisez un CDN pour délivrer vos assets:** ![medium] Utilisez un CDN pour délivrer plus rapidement votre contenu à travers le monde.

 * 📖 [10 Tips to Optimize CDN Performance - CDN Planet](https://www.cdnplanet.com/blog/10-tips-optimize-cdn-performance/)
 * 📖 [HTTP Caching  |  Web Fundamentals  |  Google Developers](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching)

- [ ] **Servez des fichiers en utilisant le même protocol:** ![high] Evitez d'utiliser des fichiers provenant de sources utilisant HTTP alors que votre site tourne en HTTPS.

- [ ] **Servez des fichiers existants:** ![high] Evitez de servir des fichiers qui n'existent pas (404).

- [ ] **Ajouter les headers HTTP de cache correctement:** ![high] Configurez les headers HTTP pour éviter des aller-retours inutiles entre le serveur et le navigateur.

- [ ] **Compression GZIP compression est activé:** ![high]

 * 📖 [Check GZIP compression](https://checkgzipcompression.com/)

**[⬆ Retour au sommaire](#table-of-contents)**

---
## Performances et Frameworks JS

### Vue

### React

 * 📖 [Optimizing Performance - React](https://reactjs.org/docs/optimizing-performance.html)
 * 📖 [React image manipulation | Cloudinary](https://cloudinary.com/documentation/react_image_manipulation)
 * 📖 [Debugging React performance with React 16 and Chrome Devtools.](https://building.calibreapp.com/debugging-react-performance-with-react-16-and-chrome-devtools-c90698a522ad)

---

## Traductions

La Front-End Performance Checklist se veut également d'être décliné dans d'autres langues! N'hésitez pas à envoyer votre contribution!

* 🇵🇹 Portugais: [fernandofawkes/Front-End-Performance-Checklist](https://github.com/fernandofawkes/Front-End-Performance-Checklist)
* 🇨🇳 Chinois: [JohnsenZhou/Front-End-Performance-Checklist](https://github.com/JohnsenZhou/Front-End-Performance-Checklist)
* 🇫🇷 Français: [WilliamDASILVA/Front-End-Performance-Checklist](https://github.com/WilliamDASILVA/Front-End-Performance-Checklist)

## Contribuer

**Ouvrir une issue ou une pull request pour suggérer des changements ou ajouts.**

## Aide

Si vosu avez une question ou une suggestion, n'hésitez pas à utiliser Gitter, Twitter ou Facebook:

* [Chat on Gitter](https://gitter.im/Front-End-Checklist/Lobby?utm_source=share-link&utm_medium=link&utm_campaign=share-link)
* [Facebook](https://www.facebook.com/frontendchecklist/)
* [Twitter](https://twitter.com/thedaviddias)

## Auteur

**Fait avec ❤️ par [David Dias](https://github.com/thedaviddias) chez [@influitive](https://influitive.com/) 🇨🇦**

**Traduit par [William DA SILVA](https://github.com/WilliamDASILVA) 🇫🇷**

## Contributeurs

Ce projet existe grâce à toute les personnes qui ont contribués. [[Contribute]](.github/CONTRIBUTING.md).

## License

[MIT](LICENCE.md)

Toute les icônes sont fournies par [Icons8](https://icons8.com/)

**[⬆ Retour au sommaire](#table-of-contents)**

[logo]: images/logo-front-end-performance-checklist.jpg
[html]: images/html.png
[css]: images/css.png
[fonts]: images/fonts.png
[images]: images/images.png
[javascript]: images/javascript.png
[server-side]: images/server-side.png

[low]: https://front-end-checklist.now.sh/low.svg
[medium]: https://front-end-checklist.now.sh/medium.svg
[high]: https://front-end-checklist.now.sh/high.svg
