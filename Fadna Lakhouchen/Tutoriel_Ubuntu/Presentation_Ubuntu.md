---
marp: true
theme: default
paginate: true
style: |
  :root {
    --color-ubuntu-orange: #E95420;
    --color-ubuntu-aubergine: #2C001E;
    --color-white: #FFFFFF;
    --color-light-grey: #F4F5F6;
  }
  
  section {
    background-color: var(--color-light-grey);
    font-family: 'Segoe UI', system-ui, sans-serif;
    color: #333333;
    font-size: 30px;
  }
  
  /* Slide de titre */
  section.title-slide {
    background-color: var(--color-ubuntu-aubergine);
    color: var(--color-white);
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  
  section.title-slide img {
    margin-bottom: 25px;
  }
  
  section.title-slide h1 {
    color: var(--color-ubuntu-orange);
    font-size: 3.5em;
    margin-bottom: 0.1em;
    border-bottom: none;
  }
  
  section.title-slide h2 {
    color: var(--color-white);
    font-weight: 300;
    font-size: 1.5em;
    margin-top: 0;
  }
  
  .authors {
    margin-top: 50px;
    font-size: 0.9em;
    color: #DDDDDD;
    font-style: italic;
    background: rgba(0,0,0,0.2);
    padding: 15px 30px;
    border-radius: 12px;
  }
  
  .authors span {
    color: var(--color-ubuntu-orange);
    font-weight: bold;
    font-style: normal;
  }
  
  /* Slides normaux */
  h1 {
    color: var(--color-ubuntu-aubergine);
    border-bottom: 4px solid var(--color-ubuntu-orange);
    padding-bottom: 15px;
    font-size: 1.8em;
  }
  
  h2 { color: var(--color-ubuntu-orange); }
  strong { color: var(--color-ubuntu-orange); }
  
  code {
    background-color: #EAEAEA;
    color: var(--color-ubuntu-aubergine);
    padding: 4px 8px;
    border-radius: 6px;
    font-weight: bold;
  }
  
  blockquote {
    background: rgba(233, 84, 32, 0.1);
    border-left: 10px solid var(--color-ubuntu-orange);
    margin: 1.5em 0;
    padding: 1em;
    font-style: italic;
    border-radius: 0 8px 8px 0;
  }
  
  ul li { margin-bottom: 15px; }
  
  .grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 40px;
    margin-top: 20px;
  }
  
  .pros, .cons {
    background: white;
    padding: 20px;
    border-radius: 12px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
  }
  
  .pros h3 { color: #27ae60; margin-top: 0; border-bottom: 2px solid #27ae60; padding-bottom: 10px; }
  .cons h3 { color: #c0392b; margin-top: 0; border-bottom: 2px solid #c0392b; padding-bottom: 10px; }
  
  .grid ul { padding-left: 20px; font-size: 0.9em; }
  .grid li { margin-bottom: 10px; }
  
  /* ===== SCHÉMAS ANIMÉS CSS ===== */
  
  @keyframes bounceArrow {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(10px); color: var(--color-ubuntu-orange); }
  }
  
  @keyframes pulseBox {
    0% { transform: scale(1); box-shadow: 0 0 0 0 rgba(233, 84, 32, 0.4); }
    50% { transform: scale(1.02); box-shadow: 0 0 15px 5px rgba(233, 84, 32, 0.2); }
    100% { transform: scale(1); box-shadow: 0 0 0 0 rgba(233, 84, 32, 0); }
  }
  
  @keyframes floatLeftRight {
    0%, 100% { transform: translateX(0); }
    50% { transform: translateX(5px); }
  }

  .schema-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 10px;
  }
  
  .schema-box {
    background: var(--color-ubuntu-aubergine);
    color: white;
    padding: 12px 40px;
    border-radius: 8px;
    width: 65%;
    text-align: center;
    font-weight: bold;
    box-shadow: 0 4px 6px rgba(0,0,0,0.2);
    border: 2px solid transparent;
  }
  
  .schema-box.core {
    background: var(--color-ubuntu-orange);
    animation: pulseBox 2s infinite;
    font-size: 1.1em;
  }
  
  .schema-arrow {
    font-size: 1.8em;
    margin: 5px 0;
    animation: bounceArrow 1.5s infinite;
  }
  
  /* Schema Tree */
  .tree-schema {
    display: flex;
    align-items: center;
    margin-top: 30px;
  }
  
  .root-node {
    background: var(--color-ubuntu-aubergine);
    color: white;
    padding: 20px;
    border-radius: 50%;
    font-weight: bold;
    font-size: 1.5em;
    width: 80px;
    height: 80px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-right: 40px;
    animation: pulseBox 3s infinite;
  }
  
  .branches {
    display: flex;
    flex-direction: column;
    gap: 15px;
    position: relative;
  }
  
  .branches::before {
    content: '';
    position: absolute;
    left: -25px;
    top: 20px;
    bottom: 20px;
    width: 4px;
    background: var(--color-ubuntu-orange);
  }
  
  .branch {
    background: white;
    padding: 10px 20px;
    border-radius: 6px;
    border-left: 5px solid var(--color-ubuntu-orange);
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    position: relative;
    animation: floatLeftRight 3s infinite ease-in-out;
  }
  
  .branch::before {
    content: '';
    position: absolute;
    left: -25px;
    top: 50%;
    width: 20px;
    height: 4px;
    background: var(--color-ubuntu-orange);
    transform: translateY(-50%);
  }
  
  .branch:nth-child(2) { animation-delay: 0.5s; }
  .branch:nth-child(3) { animation-delay: 1s; }
  .branch:nth-child(4) { animation-delay: 1.5s; }

---

<!-- _class: title-slide -->

<img src="https://upload.wikimedia.org/wikipedia/commons/a/ab/Logo-ubuntu_cof-orange-hex.svg" width="160" alt="Ubuntu Logo">

# Tutoriel Ubuntu
## Découverte et Architecture du Système

<div class="authors">
  Réalisé par :<br>
  <span>Fadna Lakhouchen</span> 
</div>

---

# 1. Qu'est-ce que Ubuntu ? 🐧

- **Système d'exploitation** basé sur **Linux** (distribution Debian).
- Totalement **open-source** et **gratuit**.
- Utilisé partout : Ordinateurs personnels, Entreprises, Serveurs, Cloud.
- Développé et sponsorisé par l'entreprise **Canonical**.

> *"Ubuntu"* est un mot africain signifiant *"Je suis ce que je suis grâce à ce que nous sommes tous"*. Cela reflète l'esprit de communauté !

---

# 2. L'Architecture  🏗️

Le système est construit en plusieurs couches :

<div class="schema-container">
  <div class="schema-box">💻 Le Matériel (Processeur, RAM, Disque)</div>
  <div class="schema-arrow">⬇️</div>
  <div class="schema-box core">🧠 Le Noyau Linux (Kernel : Le traducteur)</div>
  <div class="schema-arrow">⬇️</div>
  <div class="schema-box">⌨️ Le Shell (Interface Ligne de Commande)</div>
  <div class="schema-arrow">⬇️</div>
  <div class="schema-box">🖱️ L'Interface Graphique (GUI / GNOME)</div>
  <div class="schema-arrow">⬇️</div>
  <div class="schema-box">📱 Les Applications (Firefox, VS Code...)</div>
</div>

---

# 3. Le Système de Fichiers 📂

Fini le `C:\` ou `D:\` de Windows ! Sur Linux, tout part de la **Racine** appelée **`/`** (Root).

<div class="tree-schema">
  <div class="root-node">/</div>
  <div class="branches">
    <div class="branch"><strong>/home</strong> : Vos fichiers personnels (Documents...)</div>
    <div class="branch"><strong>/etc</strong> : Les fichiers de configuration système</div>
    <div class="branch"><strong>/var</strong> : Les fichiers variables (logs, BDD)</div>
    <div class="branch"><strong>/bin</strong> : Les commandes exécutables (Terminal)</div>
  </div>
</div>

---

# 4. Gestion des Logiciels (APT) 📦

Sur Ubuntu, pas besoin de télécharger des fichiers `.exe`. On passe par un **Gestionnaire de paquets** appelé **APT**. 

- Mettre à jour la liste des logiciels :
  `sudo apt update`

- Installer un nouveau logiciel :
  `sudo apt install nom_du_logiciel`

*(La commande `sudo` vous donne temporairement les droits d'Administrateur).*

---

# 5. Les Versions (Cycle de Vie) 🔄

Une nouvelle version sort tous les 6 mois (Avril et Octobre).

- **LTS (Long Term Support)** : 
  Sortent tous les 2 ans (ex: 22.04, 24.04). Elles sont extrêmement stables et ont des mises à jour de sécurité garanties pendant **5 ans**. *(C'est ce qu'on utilise en entreprise)*.
  
- **Versions normales** : 
  Supportées pendant 9 mois seulement. Idéales pour tester les dernières nouveautés.

---

# 6. Les Différentes Saveurs (Flavors) 🎨

- **Ubuntu Desktop** : Pour votre PC personnel (avec interface graphique).
- **Ubuntu Server** : Pour les serveurs. *Pas d'interface graphique*, 100% terminal pour économiser la RAM et le processeur !
- **Kubuntu / Xubuntu / Lubuntu** : Le même moteur Ubuntu, mais avec des interfaces graphiques différentes (plus légères pour les vieux PC ou avec un design différent).

---

# 7. Avantages et Inconvénients ⚖️

<div class="grid">
  <div class="pros">
    <h3>✅ Avantages</h3>
    <ul>
      <li><strong>Sécurité</strong> : Très peu de virus, pas besoin d'antivirus.</li>
      <li><strong>Performances</strong> : Fluide, même sur de vieilles machines.</li>
      <li><strong>Gratuit & Open Source</strong>.</li>
      <li><strong>Paradis des devs</strong> : Idéal pour Docker, Git, Python, etc.</li>
    </ul>
  </div>
  
  <div class="cons">
    <h3>❌ Inconvénients</h3>
    <ul>
      <li><strong>Logiciels Pros</strong> : Pas de suite Adobe ni de Microsoft Office (faut utiliser des alternatives).</li>
      <li><strong>Jeux Vidéo</strong> : Moins de jeux natifs (bien que ça s'améliore).</li>
      <li><strong>Apprentissage</strong> : Demande un petit effort d'adaptation.</li>
    </ul>
  </div>
</div>

---

# 8. Ce qu'il faut absolument savoir ! 💡

- 🔠 **Sensibilité à la casse (Case Sensitive)** : Sur Linux, `Fichier.txt` et `fichier.txt` sont **deux fichiers différents** ! Fais attention aux majuscules !
- 🔑 **La puissance de `sudo`** : La sécurité est reine. Si tu essaies de modifier le système sans le mot magique `sudo`, tu auras une erreur *"Permission denied"*.
- 🤝 **La Communauté est ton amie** : Tu as un bug ou une erreur ? Copie-la sur Google ! La communauté Ubuntu est gigantesque, la solution existe toujours sur un forum.
- 👨‍💻 **N'aie pas peur du Terminal !** Au début ça fait peur, mais avec le temps tu te rendras compte que c'est beaucoup plus rapide que la souris.

---

<!-- _class: title-slide -->

## Merci pour votre attention !

