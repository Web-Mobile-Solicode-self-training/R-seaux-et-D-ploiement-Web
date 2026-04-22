---
marp: true
theme: default
_class: lead
_paginate: false
paginate: true
backgroundColor: #ffffff
style: |
  @import url('https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;600;700&display=swap');
  section {
    font-family: 'Outfit', sans-serif;
    font-size: 24px;
    color: #2d3436;
    line-height: 1.6;
    padding: 60px 80px;
    background: linear-gradient(135deg, #ffffff 0%, #f1f2f6 100%);
  }
  footer { width: 100%; text-align: right; font-size: 14px; color: #a4b0be; font-weight: 300; }
  .logo-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: absolute;
    top: 30px;   
    left: 50px;
    right: 50px;
  }
  .logo-header img { height: 110px; filter: drop-shadow(0 4px 6px rgba(0,0,0,0.1)); transition: transform 0.3s ease; }
  .logo-header img:hover { transform: scale(1.05); }
  
  h1 { color: #0984e3; font-size: 3em; margin-top: 80px; text-align: left; font-weight: 700; letter-spacing: -1px; }
  h2 { color: #0984e3; font-size: 2.2em; border-bottom: 3px solid #74b9ff; margin-bottom: 35px; font-weight: 600; padding-bottom: 10px; }
  h3 { text-align: left; color: #636e72; margin-top: 0; font-weight: 400; font-size: 1.4em; }
  h4 { color: #0984e3; margin-bottom: 15px; font-weight: 600; }

  .highlight { color: #0984e3; font-weight: 600; }

  .sommaire-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 25px;
    margin-top: 30px;
  }
  .sommaire-item {
    display: flex;
    align-items: center;
    background: #ffffff;
    border-radius: 15px;
    padding: 20px;
    box-shadow: 0 10px 20px rgba(0,0,0,0.05);
    border-left: 6px solid #0984e3;
    transition: all 0.3s ease;
  }
  .sommaire-item:hover { transform: translateX(10px); box-shadow: 0 15px 30px rgba(9, 132, 227, 0.1); }
  .sommaire-num {
    background: #0984e3; color: white; width: 40px; height: 40px;
    display: flex; justify-content: center; align-items: center;
    border-radius: 10px; font-weight: bold; margin-right: 20px; flex-shrink: 0; font-size: 1.1em;
  }
  .sommaire-text { font-weight: 500; font-size: 1.1em; color: #2d3436; }

  .img-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
    margin-top: 20px;
  }
  .img-premium {
    width: 90%;
    max-height: 420px;
    object-fit: contain;
    border-radius: 20px;
    box-shadow: 0 20px 40px rgba(0,0,0,0.12);
    border: 1px solid rgba(255,255,255,0.5);
  }

  .glass-card {
    background: rgba(255, 255, 255, 0.8);
    backdrop-filter: blur(10px);
    padding: 35px;
    border-radius: 20px;
    border: 1px solid rgba(255,255,255,0.4);
    box-shadow: 0 15px 35px rgba(0,0,0,0.08);
    margin-top: 20px;
    width: 100%;
  }
  
  .tech-card {
    background: #ffffff;
    padding: 25px;
    border-radius: 20px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.04);
    border-top: 6px solid #0984e3;
    height: 100%;
  }
  .tech-card ul { padding-left: 20px; margin: 0; }
  .tech-card li { margin-bottom: 12px; list-style-type: '→ '; }

  .equipment-showcase {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 20px;
    align-items: stretch;
  }
  .device-card {
    background: white;
    border-radius: 20px;
    padding: 20px;
    box-shadow: 0 15px 30px rgba(0,0,0,0.08);
    text-align: center;
    border-bottom: 5px solid #0984e3;
  }
---

<div class="logo-header">
  <img src="images/ofppt-logo.png" alt="OFPPT">
  <img src="images/logo-solicode.png" alt="Solicode">
</div>

# **Infrastructure Réseau**

### Fondamentaux du LAN & Équipements

**Module :** Réseaux Informatiques  
**Filière :** Développement Digital  
**Formateur :** M. [Nom du Formateur]

---

## Sommaire

<div class="sommaire-grid">
  <div class="sommaire-item"><div class="sommaire-num">1</div><div class="sommaire-text">Qu'est-ce qu'un LAN ?</div></div>
  <div class="sommaire-item"><div class="sommaire-num">2</div><div class="sommaire-text">Topologies Réseau</div></div>
  <div class="sommaire-item"><div class="sommaire-num">3</div><div class="sommaire-text">Les Supports de Transmission</div></div>
  <div class="sommaire-item"><div class="sommaire-num">4</div><div class="sommaire-text">Équipements d'Interconnexion</div></div>
  <div class="sommaire-item"><div class="sommaire-num">5</div><div class="sommaire-text">Focus : Switch vs Hub</div></div>
  <div class="sommaire-item"><div class="sommaire-num">6</div><div class="sommaire-text">Adressage IP (Survol)</div></div>
  <div class="sommaire-item"><div class="sommaire-num">7</div><div class="sommaire-text">Bonnes Pratiques</div></div>
</div>

---

## 1. Qu'est-ce qu'un LAN ?

<div class="glass-card">
  <p style="font-size: 1.4em; font-weight: 600; color: #0984e3;">Local Area Network</p>
  <p>Un <strong>réseau local</strong> est un groupe d'ordinateurs et de périphériques connectés entre eux dans une zone géographique limitée (bureau, maison, école).</p>
  
  <div style="display: flex; justify-content: space-around; margin-top: 40px;">
    <div style="text-align: center;">
      <div style="background: #dfe6e9; padding: 20px; border-radius: 20px; width: 150px; height: 100px; display: flex; flex-direction: column; justify-content: center;">
        <span style="font-weight: bold; font-size: 1.5em;">🏠</span>
        <span>Domestique</span>
      </div>
    </div>
    <div style="text-align: center;">
      <div style="background: #74b9ff; padding: 20px; border-radius: 20px; width: 150px; height: 100px; display: flex; flex-direction: column; justify-content: center; color: white;">
        <span style="font-weight: bold; font-size: 1.5em;">🏢</span>
        <span>Entreprise</span>
      </div>
    </div>
    <div style="text-align: center;">
      <div style="background: #0984e3; padding: 20px; border-radius: 20px; width: 150px; height: 100px; display: flex; flex-direction: column; justify-content: center; color: white;">
        <span style="font-weight: bold; font-size: 1.5em;">🎓</span>
        <span>Éducatif</span>
      </div>
    </div>
  </div>
  <p style="margin-top: 30px; font-style: italic; color: #636e72;">Objectif : Partage de ressources (Fichiers, Imprimantes, Connexion Internet).</p>
</div>

---

## 2. Topologies Réseau Courantes

<div class="equipment-showcase">
  <div class="device-card">
    <h4 style="margin-top: 0;">⭐ Étoile</h4>
    <div style="font-size: 3em; margin: 20px 0;">✴️</div>
    <p style="font-size: 0.9em;">Tous les appareils connectés à un équipement central (Switch).</p>
    <p style="color: #00b894; font-weight: bold;">La plus fiable et la plus utilisée.</p>
  </div>
  <div class="device-card">
    <h4 style="margin-top: 0;">🔄 Bus</h4>
    <div style="font-size: 3em; margin: 20px 0;">➖➖➖</div>
    <p style="font-size: 0.9em;">Un seul câble partagé par tous.</p>
    <p style="color: #d63031;">Obsolète</p>
  </div>
  <div class="device-card">
    <h4 style="margin-top: 0;">🔁 Anneau</h4>
    <div style="font-size: 3em; margin: 20px 0;">⭕</div>
    <p style="font-size: 0.9em;">Données circulent dans une boucle fermée.</p>
    <p style="color: #e17055;">Rare aujourd'hui</p>
  </div>
</div>

<div class="img-container" style="margin-top: 10px;">
  <div class="glass-card" style="text-align: center;">
    <p><span class="highlight">Topologie Physique</span> (Câblage) ≠ <span class="highlight">Topologie Logique</span> (Flux de données)</p>
  </div>
</div>

---

## 3. Supports de Transmission

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 30px;">
  <div class="tech-card" style="border-top-color: #6c5ce7;">
    <h4>🔌 Cuivre (Paire Torsadée)</h4>
    <ul>
      <li><strong>Catégorie 5e / 6 / 6a</strong></li>
      <li>Connecteur <strong>RJ45</strong></li>
      <li>Portée max : 100 mètres</li>
      <li>Coût faible, installation facile</li>
    </ul>
    <div style="margin-top: 20px; background: #f1f2f6; padding: 10px; border-radius: 10px; text-align: center;">
      <span style="font-weight: bold;">Blindé (STP) vs Non Blindé (UTP)</span>
    </div>
  </div>
  
  <div class="tech-card" style="border-top-color: #00b894;">
    <h4>✨ Fibre Optique</h4>
    <ul>
      <li>Transport par <strong>Lumière (Laser/LED)</strong></li>
      <li>Insensible aux interférences électromagnétiques</li>
      <li>Très longue portée (km)</li>
      <li><strong>Monomode</strong> (Longue distance) / <strong>Multimode</strong> (Bâtiment)</li>
    </ul>
  </div>
</div>

---

## 4. Équipements d'Interconnexion

<div class="equipment-showcase" style="grid-template-columns: 1fr 1fr;">
  <div class="device-card">
    <h4>🔄 Switch</h4>
    <p style="color: #0984e3; font-weight: 600;">L'intelligent du réseau</p>
    <p style="font-size: 0.9em;">Analyse l'adresse MAC de destination et envoie la trame <strong>uniquement</strong> au port concerné.</p>
    <p style="font-size: 0.8em; margin-top: 15px; background: #f1f2f6; padding: 5px; border-radius: 10px;">Full-Duplex → Communication simultanée</p>
  </div>
  <div class="device-card">
    <h4>📡 Hub</h4>
    <p style="color: #d63031; font-weight: 600;">Le répéteur primitif</p>
    <p style="font-size: 0.9em;">Répète les données reçues sur <strong>tous</strong> les autres ports. Crée des collisions.</p>
    <p style="font-size: 0.8em; margin-top: 15px; background: #f1f2f6; padding: 5px; border-radius: 10px;">Half-Duplex → Un seul parle à la fois</p>
  </div>
</div>

<div style="margin-top: 20px; display: flex;">
  <div class="tech-card" style="width: 100%;">
    <h4>🚀 Routeur</h4>
    <p>La passerelle entre différents réseaux (Ex: Relie votre LAN à Internet). Il travaille avec les <strong>Adresses IP</strong>, pas seulement les MAC.</p>
  </div>
</div>

---

## 5. Focus : Pourquoi le Switch a remplacé le Hub

<div class="maquette-showcase" style="grid-template-columns: 1.2fr 1fr; gap: 20px;">
  <div>
    <div class="img-container">
      <!-- Placeholder for network diagram illustration -->
      <div style="background: #2d3436; padding: 20px; border-radius: 20px; color: white; width: 100%; text-align: center;">
        <p style="color: #74b9ff;">🖥️ [A] ➡️ SWITCH ➡️ [B]</p>
        <p style="font-size: 0.7em; color: #dfe6e9;">Le switch crée un chemin dédié entre A et B. <br>Pendant ce temps, C et D peuvent aussi communiquer entre eux sans attendre.</p>
        <hr style="border-color: #636e72;">
        <p style="color: #ff7675;">🖥️ [A] ➡️ HUB ➡️ [B] [C] [D]</p>
        <p style="font-size: 0.7em; color: #dfe6e9;">Le hub envoie à tout le monde. Bande passante gaspillée.</p>
      </div>
    </div>
  </div>
  <div class="glass-card">
    <h4 style="margin-top: 0;">Avantage Switch</h4>
    <ul>
      <li><strong>Sécurité :</strong> Pas de "sniffing" facile des données des autres ports.</li>
      <li><strong>Performance :</strong> Micro-segmentation (Domaine de collision séparé par port).</li>
      <li><strong>Bande Passante :</strong> Chaque port a sa vitesse dédiée (100 Mbps / 1 Gbps).</li>
    </ul>
  </div>
</div>

---

## 6. Adressage IP dans le LAN

<div class="glass-card">
  <h4>Le Protocole TCP/IP (Survol Essentiel)</h4>
  <p>Pour qu'un PC A trouve un PC B dans le LAN, il faut une <strong>Adresse IP</strong> et un <strong>Masque de Sous-Réseau</strong>.</p>
  
  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 30px; margin-top: 30px;">
    <div style="background: #f1f2f6; padding: 20px; border-radius: 15px;">
      <p style="font-weight: bold; color: #0984e3;">Exemple typique :</p>
      <code style="font-size: 1.5em; background: none;">192.168.1.10</code>
      <p>Masque : <code>255.255.255.0</code></p>
      <p>Passerelle (Routeur) : <code>192.168.1.1</code></p>
    </div>
    <div style="padding: 20px;">
      <p><span class="highlight">DHCP</span> : Service qui attribue ces adresses automatiquement.</p>
      <p><span class="highlight">DNS</span> : Traduit "google.com" en IP.</p>
    </div>
  </div>
</div>

---

## 7. Bonnes Pratiques en Salle Serveur

<div class="equipment-showcase" style="grid-template-columns: 1fr 1fr;">
  <div class="device-card">
    <h4>📦 Câblage Structuré</h4>
    <ul style="text-align: left;">
      <li>Utiliser des baies de brassage (Racks 19").</li>
      <li>Panneaux de brassage (Patch Panels).</li>
      <li>Guides de câbles pour la ventilation.</li>
      <li>Étiquetage <strong>OBLIGATOIRE</strong>.</li>
    </ul>
    <div style="font-size: 3em;">🔌🗂️</div>
  </div>
  <div class="device-card">
    <h4>⚠️ Sécurité Physique</h4>
    <ul style="text-align: left;">
      <li>Salle technique fermée à clé.</li>
      <li>Contrôle de la température et de l'humidité.</li>
      <li>Onduleur (UPS) pour éviter les coupures brutales.</li>
    </ul>
    <div style="font-size: 3em;">🌡️🔋</div>
  </div>
</div>

---

## Conclusion : Le LAN pour un Développeur

<div class="glass-card" style="text-align: center;">
  <h3 style="color: #0984e3; font-weight: 700; margin-bottom: 20px;">Pourquoi comprendre le LAN ?</h3>
  <p style="font-size: 1.2em;">En développement digital, vous créez des applications qui <strong>vivent sur le réseau</strong>.</p>
  <div style="display: flex; justify-content: center; gap: 40px; margin: 40px 0;">
    <div>
      <span style="background: #0984e3; color: white; padding: 10px 20px; border-radius: 30px;">API Locales</span>
    </div>
    <div>
      <span style="background: #00b894; color: white; padding: 10px 20px; border-radius: 30px;">Docker Networking</span>
    </div>
    <div>
      <span style="background: #6c5ce7; color: white; padding: 10px 20px; border-radius: 30px;">Débogage</span>
    </div>
  </div>
  <p>Une bonne maîtrise des bases réseau (IP, Ports, Switch) fait la différence entre un bon développeur et un excellent architecte logiciel.</p>
</div>

---

## Merci pour votre attention !

<div class="img-container">
   <h3 style="color: #0984e3; font-weight: 700;">Des questions sur le matériel ou la configuration ?</h3>
   <p style="color: #636e72;">Module Réseaux | Développement Digital</p>
</div>