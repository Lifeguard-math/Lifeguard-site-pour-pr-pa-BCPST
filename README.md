[lifeguard (2).html](https://github.com/user-attachments/files/33788112/lifeguard.2.html)
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Lifeguard — Maths BCPST</title>
<style>
:root{
  --navy:#0b2540; --coral:#ff6b4a; --coral-d:#e6553a;
  --bg:#f7f4ec; --card:#ffffff; --text:#16324a; --muted:#5c7189; --border:#e3ddd0; --radius:14px;
  box-sizing:border-box; padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
}
*{box-sizing:inherit;}
@media (prefers-color-scheme: dark){
  :root:not([data-theme="light"]){--bg:#0b1622;--card:#12233a;--text:#e8eef4;--muted:#93a6bb;--border:#1f3348;}
}
:root[data-theme="dark"]{--bg:#0b1622;--card:#12233a;--text:#e8eef4;--muted:#93a6bb;--border:#1f3348;}
html{scroll-padding-top:env(safe-area-inset-top,0px);}
body{margin:0;background:var(--bg);color:var(--text);font-family:system-ui,-apple-system,"Segoe UI",Roboto,Arial,sans-serif;line-height:1.5;}
.hidden{display:none!important;}
header.topbar{position:sticky;top:0;z-index:20;background:var(--navy);color:#fff;padding:calc(10px + env(safe-area-inset-top,0px)) 16px 10px;}
.topbar-inner{max-width:1100px;margin:0 auto;display:flex;align-items:center;gap:16px;flex-wrap:wrap;}
.logo{font-weight:800;font-size:1.3rem;display:flex;align-items:center;gap:8px;white-space:nowrap;}
.logo small{font-weight:400;font-size:.7rem;opacity:.75;display:block;}
nav.tabs{display:flex;gap:6px;overflow-x:auto;flex:1;}
.nav-btn{background:transparent;border:none;color:#cfe0f0;padding:8px 14px;border-radius:999px;font-size:.92rem;cursor:pointer;white-space:nowrap;}
.nav-btn.active,.nav-btn:hover{background:rgba(255,255,255,.14);color:#fff;}
.btn-primary{background:var(--coral);color:#fff;border:none;padding:9px 16px;border-radius:999px;font-weight:700;cursor:pointer;font-size:.9rem;}
.btn-primary:hover{background:var(--coral-d);}
.btn-primary.subscribed{background:#2f9e6b;}
main{max-width:1100px;margin:0 auto;padding:28px 16px 60px;}
.tab{display:none;}
.tab.active{display:block;animation:fade .25s ease;}
@keyframes fade{from{opacity:0;transform:translateY(4px);}to{opacity:1;transform:none;}}
.hero{padding:20px 0 10px;}
.hero h1{font-size:clamp(1.6rem,4vw,2.5rem);margin:0 0 10px;}
.hero p.lead{color:var(--muted);max-width:640px;font-size:1.05rem;}
.feature-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px;margin:26px 0;}
.card{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:18px;}
.feature-grid .card b{display:block;margin-bottom:6px;font-size:1.05rem;}
.pricing-strip{display:flex;align-items:center;justify-content:space-between;gap:16px;flex-wrap:wrap;background:var(--navy);color:#fff;border-radius:var(--radius);padding:22px;}
.pricing-strip .price{font-size:2rem;font-weight:800;}
.pricing-strip .price span{font-size:.9rem;font-weight:400;opacity:.8;}
.subnav{display:flex;gap:8px;margin:18px 0;}
.subnav button{padding:8px 16px;border-radius:999px;border:1px solid var(--border);background:var(--card);color:var(--text);cursor:pointer;}
.subnav button.active{background:var(--navy);color:#fff;border-color:var(--navy);}
h2{font-size:1.5rem;}
.domaine{margin:22px 0 10px;color:var(--coral-d);text-transform:uppercase;font-size:.78rem;letter-spacing:.08em;}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:12px;}
details.chapitre{padding:0;overflow:hidden;}
details.chapitre summary{list-style:none;cursor:pointer;padding:14px 16px;display:flex;justify-content:space-between;align-items:center;gap:8px;font-weight:600;}
details.chapitre summary::-webkit-details-marker{display:none;}
.niveaux{padding:0 16px 14px;display:flex;flex-direction:column;gap:6px;border-top:1px solid var(--border);}
.niveau{display:flex;justify-content:space-between;font-size:.86rem;color:var(--muted);padding-top:8px;}
.annales-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:12px;}
.annale-head{display:flex;justify-content:space-between;font-weight:700;margin-bottom:10px;}
.annale-actions{display:flex;gap:8px;flex-wrap:wrap;}
.annale-actions button{flex:1;background:var(--bg);border:1px solid var(--border);border-radius:8px;padding:8px 6px;cursor:pointer;font-size:.8rem;color:var(--text);}
.filters{display:flex;gap:8px;margin:16px 0;flex-wrap:wrap;}
.filters button{padding:7px 14px;border-radius:999px;border:1px solid var(--border);background:var(--card);cursor:pointer;color:var(--text);}
.filters button.active{background:var(--coral);color:#fff;border-color:var(--coral);}
.menu-wrap{position:relative;}
.menu-btn{background:transparent;border:none;color:#fff;font-size:1.3rem;cursor:pointer;padding:2px 8px;line-height:1;}
.dropdown{position:absolute;right:0;top:calc(100% + 8px);background:var(--card);border:1px solid var(--border);border-radius:10px;overflow:hidden;min-width:210px;box-shadow:0 8px 24px rgba(0,0,0,.2);}
.dropdown button{display:block;width:100%;text-align:left;background:none;border:none;padding:12px 16px;color:var(--text);cursor:pointer;font-size:.9rem;}
.dropdown button:hover{background:var(--bg);}
.kholle-list label{display:flex;gap:8px;align-items:center;font-weight:400!important;padding:10px 12px;border:1px solid var(--border);border-radius:8px;background:var(--card);font-size:.88rem;}
#ia-setup{display:flex;flex-direction:column;gap:14px;}
#prepia label{display:flex;flex-direction:column;gap:6px;font-size:.85rem;color:var(--muted);flex:1;min-width:160px;}
select,textarea,input[type=email],input[type=password],input[type=text]{padding:9px;border-radius:8px;border:1px solid var(--border);background:var(--bg);color:var(--text);font-family:inherit;font-size:.95rem;width:100%;}
textarea{width:100%;min-height:150px;margin:14px 0;resize:vertical;}
.ia-top{display:flex;justify-content:space-between;font-weight:700;margin-bottom:10px;color:var(--coral-d);}
.enonce{white-space:pre-wrap;background:var(--bg);border-radius:8px;padding:14px;font-size:.95rem;}
.overlay{position:fixed;inset:0;background:rgba(11,37,64,.6);display:flex;align-items:center;justify-content:center;z-index:50;padding:16px;}
.modal{background:var(--card);border-radius:var(--radius);padding:26px;max-width:380px;position:relative;text-align:center;}
.modal .close{position:absolute;top:10px;right:14px;background:none;border:none;font-size:1.1rem;cursor:pointer;color:var(--muted);}
.modal .price{font-size:2.2rem;font-weight:800;margin:12px 0;color:var(--coral-d);}
.modal .price span{font-size:.9rem;color:var(--muted);font-weight:400;}
.toast{position:fixed;bottom:calc(18px + env(safe-area-inset-bottom,0px));left:50%;transform:translateX(-50%) translateY(10px);background:var(--navy);color:#fff;padding:10px 18px;border-radius:999px;opacity:0;transition:.3s;z-index:60;font-size:.86rem;max-width:90vw;text-align:center;}
.toast.show{opacity:1;transform:translateX(-50%) translateY(0);}
footer{text-align:center;padding:30px 16px calc(30px + env(safe-area-inset-bottom,0px));color:var(--muted);font-size:.8rem;}
@media(max-width:600px){.logo small{display:none;}}
</style>
</head>
<body>
<header class="topbar"><div class="topbar-inner">
  <div class="logo">🛟 Lifeguard<small>Maths BCPST</small></div>
  <nav class="tabs">
    <button class="nav-btn" data-tab="conseils" onclick="showTab('conseils')">Conseils</button>
    <button class="nav-btn active" data-tab="accueil" onclick="showTab('accueil')">Accueil</button>
    <button class="nav-btn" data-tab="chapitres" onclick="showTab('chapitres')">Chapitres</button>
    <button class="nav-btn" data-tab="annales" onclick="showTab('annales')">Annales</button>
    <button class="nav-btn" data-tab="prepia" onclick="showTab('prepia')">PrepIA</button>
    <button class="nav-btn" data-tab="kholles" onclick="showTab('kholles')">Khôlles</button>
  </nav>
  <button id="sub-btn" class="btn-primary" onclick="openPaywall()">S'abonner – 10€/an</button>
  <div id="compte-badge" class="hidden" style="color:#fff;font-weight:600;font-size:.9rem;white-space:nowrap">👤 <span id="compte-nom"></span></div>
  <div class="menu-wrap">
    <button class="menu-btn" onclick="toggleMenu()" aria-label="Menu">☰</button>
    <div id="menu-dropdown" class="dropdown hidden">
      <button onclick="closeMenu();openCompte()">Compte</button>
      <button onclick="closeMenu();openPaywall()">Abonnement</button>
      <button onclick="closeMenu();toast('Support : support@lifeguard-maths.fr (démo)')">Contacter le support</button>
      <button id="menu-admin" class="hidden" onclick="closeMenu();showTab('admin')">Administration</button>
    </div>
  </div>
</div></header>

<main>
  <section id="conseils" class="tab">
    <h2>Conseils</h2>
    <div class="subnav">
      <button id="cg1" class="active" onclick="setConseilView('generaux')">Conseils généraux</button>
      <button id="cg2" onclick="setConseilView('chapitre')">Conseils par chapitre</button>
    </div>
    <div id="conseils-generaux" class="feature-grid"></div>
    <div id="conseils-chapitre" class="hidden">
      <div class="card" style="border-style:dashed;text-align:center;color:var(--muted);margin-bottom:14px">🚧 Génération par IA — arrive bientôt. Les chapitres déjà complétés par l'équipe s'affichent normalement.</div>
      <div id="conseils-chapitre-list"></div>
    </div>
  </section>

  <section id="accueil" class="tab active">
    <div class="hero">
      <h1>Progresser en maths BCPST, sans jamais couler.</h1>
      <p class="lead">Lifeguard rassemble les chapitres officiels de 1ère et 2ème années, cinq ans d'annales Agro-Véto, G2E et ENS, et PrepIA pour s'entraîner en conditions de concours avec une correction générée par IA.</p>
      <button class="btn-primary" onclick="showTab('chapitres')">Voir les chapitres</button>
    </div>
    <div class="feature-grid">
      <div class="card"><b>📘 Chapitres 1A / 2A</b>Le programme officiel BCPST découpé en chapitres, exercices classés par niveau.</div>
      <div class="card"><b>🗂️ Annales</b>5 dernières années des concours Agro-Véto, G2E et ENS : sujets et corrigés.</div>
      <div class="card"><b>🤖 PrepIA</b>Un exercice, un temps limité, une correction et une analyse générées par IA.</div>
    </div>
    <div class="pricing-strip">
      <div><div class="price">10€ <span>/ an</span></div><div>Accès illimité à tout Lifeguard</div></div>
      <button class="btn-primary" onclick="openPaywall()">Je m'abonne</button>
    </div>
  </section>

  <section id="chapitres" class="tab">
    <h2>Chapitres</h2>
    <p style="color:var(--muted)">Découpage conforme au programme officiel de mathématiques BCPST.</p>
    <div class="subnav">
      <button id="y1" class="active" onclick="setYear(1)">1ère année</button>
      <button id="y2" onclick="setYear(2)">2ème année</button>
    </div>
    <div id="chapitres-list"></div>
  </section>

  <section id="annales" class="tab">
    <h2>Annales</h2>
    <p style="color:var(--muted)">Sujets et corrigés des 5 dernières sessions (2022–2026).</p>
    <div class="filters" id="filters"></div>
    <div class="annales-grid" id="annales-list"></div>
  </section>

  <section id="prepia" class="tab">
    <h2>PrepIA</h2>
    <p style="color:var(--muted)">Un exercice, un temps limité, une correction générée et analysée par IA. Inclus dans l'abonnement Lifeguard.</p>
    <div class="card" style="border-style:dashed;text-align:center;color:var(--muted);margin-bottom:14px">🚧 Génération et correction par IA — arrive bientôt. L'interface ci-dessous est consultable dès maintenant.</div>
    <div class="card" id="ia-setup">
      <div class="subnav">
        <button id="pm1" class="active" onclick="setPrepMode('chapitre')">Exercice ciblé</button>
        <button id="pm2" onclick="setPrepMode('kholle')">Programme de khôlle</button>
        <button id="pm3" onclick="setPrepMode('upload')">Mon programme (photo)</button>
      </div>
      <div id="pm-chapitre"><label>Chapitre <select id="ia-ch"></select></label></div>
      <div id="pm-kholle" class="hidden">
        <p style="color:var(--muted);margin:4px 0">Sélectionnez 2 à 3 chapitres à travailler pendant la session.</p>
        <div id="ia-kholle-list" class="grid kholle-list"></div>
      </div>
      <div id="pm-upload" class="hidden">
        <p style="color:var(--muted);margin:4px 0">Envoyez une photo (JPG/PNG) de votre programme de révision personnalisé ; l'IA l'analysera pour cibler l'exercice.</p>
        <input type="file" id="ia-file" accept="image/*" onchange="handleFileUpload(event)">
        <div id="ia-file-status" style="color:var(--muted);font-size:.85rem;margin-top:6px"></div>
      </div>
      <div style="display:flex;gap:16px;flex-wrap:wrap;align-items:end">
        <label>Durée <select id="ia-duree"><option value="600">10 min</option><option value="1200" selected>20 min</option><option value="1800">30 min</option><option value="3600">1h (examen blanc)</option></select></label>
        <button class="btn-primary" onclick="demarrerPrepIA()">Commencer</button>
      </div>
    </div>
    <div class="card hidden" id="ia-session">
      <div class="ia-top"><span id="ia-timer"></span><span id="ia-chapitre-label"></span></div>
      <div id="ia-enonce" class="enonce"></div>
      <textarea id="ia-reponse" placeholder="Rédigez votre réponse ici…"></textarea>
      <button class="btn-primary" onclick="envoyerPrepIA()">Envoyer pour correction</button>
    </div>
    <div class="card hidden" id="ia-resultat">
      <h3 style="margin-top:0">Correction IA</h3>
      <div id="ia-correction" class="enonce"></div>
      <button class="btn-primary" style="margin-top:12px" onclick="resetPrepIA()">Nouvel exercice</button>
    </div>
  </section>

  <section id="kholles" class="tab">
    <h2>Se préparer aux khôlles</h2>
    <p style="color:var(--muted)">Questions de cours courtes, triées par chapitre, avec leur correction — cliquez sur un chapitre pour les afficher.</p>
    <div class="card" style="border-style:dashed;text-align:center;color:var(--muted);margin-bottom:14px">🚧 Génération par IA — arrive bientôt. Les chapitres déjà complétés par l'équipe s'affichent normalement.</div>
    <div id="kholle-questions-list"></div>
  </section>

  <section id="inscription" class="tab">
    <div class="card" style="max-width:420px;margin:20px auto">
      <h2 style="margin-top:0">Créer mon compte</h2>
      <div style="display:flex;flex-direction:column;gap:10px">
        <label style="display:flex;flex-direction:column;gap:4px">Nom<input type="text" id="inscr-nom"></label>
        <label style="display:flex;flex-direction:column;gap:4px">Prénom<input type="text" id="inscr-prenom"></label>
        <label style="display:flex;flex-direction:column;gap:4px">E-mail<input type="email" id="inscr-email"></label>
        <label style="display:flex;flex-direction:column;gap:4px">Mot de passe<input type="password" id="inscr-pass"></label>
        <label style="display:flex;flex-direction:column;gap:4px">Comment avez-vous découvert Lifeguard ?
          <select id="inscr-decouverte"><option>Bouche-à-oreille</option><option>Réseaux sociaux</option><option>Professeur / lycée</option><option>Moteur de recherche</option><option>Autre</option></select>
        </label>
      </div>
      <button class="btn-primary" style="width:100%;margin-top:16px" onclick="creerCompte()">Créer mon compte</button>
      <button style="width:100%;margin-top:8px;background:none;border:none;color:var(--muted);cursor:pointer" onclick="showTab('accueil')">Annuler</button>
    </div>
  </section>

  <section id="admin" class="tab">
    <h2>Administration</h2>
    <p style="color:var(--muted)">Visible et modifiable uniquement par les comptes ayant les droits d'édition sur cet artifact ; les visiteurs voient le contenu mis à jour.</p>
    <div class="subnav">
      <button id="ad1" class="active" onclick="setAdminView('conseils')">Conseils généraux</button>
      <button id="ad2" onclick="setAdminView('exos')">Exercices par chapitre</button>
      <button id="ad3" onclick="setAdminView('conseilsch')">Conseils par chapitre</button>
      <button id="ad4" onclick="setAdminView('kholle')">Khôlles</button>
      <button id="ad5" onclick="setAdminView('annales')">Annales</button>
    </div>
    <div id="admin-conseils">
      <div id="admin-conseils-list" style="display:flex;flex-direction:column;gap:10px;margin:14px 0"></div>
      <button style="margin-bottom:10px;border:1px solid var(--border);background:var(--card);border-radius:8px;padding:8px 14px;cursor:pointer;color:var(--text)" onclick="ajouterConseilAdmin()">+ Ajouter un conseil</button><br>
      <button class="btn-primary" onclick="enregistrerConseils()">Enregistrer les conseils</button>
    </div>
    <div id="admin-exos" class="hidden">
      <label>Chapitre <select id="admin-ch" onchange="chargerAdminExos()"></select></label>
      <div id="admin-exos-list" style="display:flex;flex-direction:column;gap:10px;margin:14px 0"></div>
      <button style="margin-bottom:10px;border:1px solid var(--border);background:var(--card);border-radius:8px;padding:8px 14px;cursor:pointer;color:var(--text)" onclick="ajouterExoAdmin()">+ Ajouter un exercice</button><br>
      <button class="btn-primary" onclick="enregistrerExos()">Enregistrer les exercices</button>
    </div>
    <div id="admin-conseilsch" class="hidden">
      <label>Chapitre <select id="admin-ch-conseil" onchange="chargerAdminConseilCh()"></select></label>
      <textarea id="admin-conseil-texte" style="min-height:100px;margin-top:10px" placeholder="Conseil méthodologique pour ce chapitre…"></textarea>
      <button class="btn-primary" style="margin-top:10px" onclick="enregistrerConseilCh()">Enregistrer</button>
    </div>
    <div id="admin-kholle" class="hidden">
      <label>Chapitre <select id="admin-ch-kholle" onchange="chargerAdminKholle()"></select></label>
      <div id="admin-kholle-list" style="display:flex;flex-direction:column;gap:10px;margin:14px 0"></div>
      <button style="margin-bottom:10px;border:1px solid var(--border);background:var(--card);border-radius:8px;padding:8px 14px;cursor:pointer;color:var(--text)" onclick="ajouterQuestionKholle()">+ Ajouter une question</button><br>
      <button class="btn-primary" onclick="enregistrerKholle()">Enregistrer les questions</button>
    </div>
    <div id="admin-annales" class="hidden">
      <div style="display:flex;gap:12px;flex-wrap:wrap">
        <label>Concours <select id="admin-concours"><option>Agro-Véto</option><option>G2E</option><option>ENS</option></select></label>
        <label>Année <select id="admin-annee"></select></label>
      </div>
      <div style="display:flex;flex-direction:column;gap:10px;margin-top:12px;max-width:420px">
        <label style="display:flex;flex-direction:column;gap:4px">Lien du sujet (URL)<input type="text" id="admin-sujet-url" placeholder="https://..."></label>
        <label style="display:flex;flex-direction:column;gap:4px">Lien du corrigé (URL)<input type="text" id="admin-corrige-url" placeholder="https://..."></label>
      </div>
      <button class="btn-primary" style="margin-top:10px" onclick="enregistrerAnnale()">Enregistrer</button>
    </div>
  </section>
</main>

<footer>Lifeguard — Prototype de démonstration. Aucun paiement réel n'est effectué. © 2026</footer>

<div id="modal" class="overlay hidden">
  <div class="modal">
    <button class="close" onclick="closeModal()">✕</button>
    <h3>🛟 Débloquez tout Lifeguard</h3>
    <p style="color:var(--muted)">Conseils, chapitres 1A/2A, annales Agro-Véto/G2E/ENS, PrepIA et préparation aux khôlles, pendant 1 an.</p>
    <div class="price" id="prix-affiche">10€ <span>/ an</span></div>
    <div style="display:flex;gap:8px;margin:10px 0">
      <input type="text" id="promo-code" placeholder="Code promo" style="text-transform:uppercase">
      <button onclick="appliquerPromo()" style="padding:9px 14px;border-radius:8px;border:1px solid var(--border);background:var(--bg);color:var(--text);cursor:pointer;white-space:nowrap">Appliquer</button>
    </div>
    <div id="promo-msg" style="font-size:.8rem;min-height:1.2em;margin-bottom:6px"></div>
    <button class="btn-primary" onclick="subscribe()">S'abonner (démo)</button>
  </div>
</div>

<div id="modal-compte" class="overlay hidden">
  <div class="modal">
    <button class="close" onclick="closeCompte()">✕</button>
    <h3>🛟 Mon compte</h3>
    <p style="color:var(--muted)">Connectez-vous pour retrouver votre progression Lifeguard.</p>
    <div style="text-align:left;display:flex;flex-direction:column;gap:10px;margin:14px 0">
      <label style="display:flex;flex-direction:column;gap:4px">E-mail<input type="email" id="login-email" placeholder="vous@exemple.fr"></label>
      <label style="display:flex;flex-direction:column;gap:4px">Mot de passe<input type="password" id="login-pass" placeholder="••••••••"></label>
    </div>
    <button class="btn-primary" style="width:100%" onclick="seConnecter()">Se connecter</button>
    <div class="pricing-strip" style="margin-top:18px;flex-direction:column;align-items:stretch;text-align:center;gap:10px;padding:16px">
      <div>Pas encore de compte ?</div>
      <button class="btn-primary" onclick="ouvrirInscription()">Créer mon compte</button>
    </div>
  </div>
</div>

<script>
let subscribed=false, currentYear=1, filtreConcours="Tous", timerInterval=null, timeLeft=0, prepMode="chapitre", uploadedImageBase64=null, uploadedImageType=null;
const CONSEILS_GENERAUX=[
["Planifier ses révisions","Consacrez un créneau fixe chaque semaine à chaque matière, en priorisant les chapitres les plus récents avant une khôlle."],
["Rédiger comme au concours","Justifiez chaque étape et citez les théorèmes utilisés : la rigueur de rédaction compte autant que le résultat."],
["Refaire ses erreurs","Après un devoir corrigé, retravaillez seul les exercices ratés une semaine plus tard pour vérifier l'acquis."],
["Alterner les niveaux","Ne visez pas systématiquement les exercices les plus durs : consolidez d'abord les exercices de découverte."],
["Préparer sa khôlle","Relisez le cours, les définitions et les démonstrations exigibles avant de foncer sur les exercices d'annales."],
["Gérer son temps le jour J","En concours, ne restez pas bloqué sur une question : passez à la suivante et revenez-y si le temps le permet."]
];
let compteConnecte=null, remise=0, estAdmin=false, adminConseilsData=[], adminExosData=[], adminChCourant=null, adminConseilChCourant=null, adminKholleChCourant=null, adminKholleData=[];
const CODES_PROMO={"BIENVENUE10":2,"KHOLLE5":0.5,"LIFEGUARD":3};
const CH={
1:[["Outils","Logique, ensembles et raisonnement"],["Outils","Nombres réels et trigonométrie"],["Outils","Nombres complexes"],["Outils","Dénombrement"],["Analyse","Suites réelles usuelles"],["Analyse","Fonctions usuelles : limites et continuité"],["Analyse","Dérivation des fonctions réelles"],["Analyse","Calcul intégral sur un segment"],["Analyse","Développements limités"],["Analyse","Équations différentielles linéaires"],["Analyse","Fonctions de deux variables réelles"],["Algèbre","Systèmes linéaires et calcul matriciel"],["Algèbre","Polynômes réels"],["Algèbre","Espaces vectoriels Kⁿ et applications linéaires"],["Géométrie","Géométrie du plan et de l'espace"],["Probabilités","Probabilités sur un univers fini"],["Probabilités","Variables aléatoires discrètes"],["Probabilités","Statistique descriptive"]],
2:[["Analyse","Séries numériques"],["Analyse","Intégrales généralisées"],["Analyse","Équations différentielles scalaires"],["Algèbre","Polynômes : compléments"],["Algèbre","Espaces vectoriels généraux"],["Algèbre","Applications linéaires et matrices"],["Algèbre","Réduction : valeurs propres et diagonalisation"],["Géométrie","Produit scalaire dans Rⁿ et projection orthogonale"],["Probabilités","Variables aléatoires discrètes : compléments et couples"],["Probabilités","Variables aléatoires à densité"],["Probabilités","Théorèmes limites"],["Probabilités","Statistique inférentielle"]]
};
const NIVEAUX=["Découverte","Entraînement","Approfondissement"];
const CONCOURS=["Agro-Véto","G2E","ENS"];
const ANNEES=[2026,2025,2024,2023,2022];
const IA_ACTIF=false;

function showTab(id){
  document.querySelectorAll(".tab").forEach(s=>s.classList.remove("active"));
  document.getElementById(id).classList.add("active");
  document.querySelectorAll(".nav-btn").forEach(b=>b.classList.toggle("active", b.dataset.tab===id));
  window.scrollTo(0,0);
}
function setYear(y){
  currentYear=y;
  document.getElementById("y1").classList.toggle("active",y===1);
  document.getElementById("y2").classList.toggle("active",y===2);
  renderChapitres();
}
function renderChapitres(){
  const list=CH[currentYear];
  const domaines=[...new Set(list.map(c=>c[0]))];
  let html="";
  domaines.forEach(d=>{
    html+=`<h3 class="domaine">${d}</h3><div class="grid">`;
    list.forEach((c,i)=>{
      if(c[0]!==d) return;
      const counts=NIVEAUX.map((n,k)=>4+((i+k)%4));
      const rows=NIVEAUX.map((n,k)=>`<div class="niveau"><span>${n}</span><b>${counts[k]} exercices</b></div>`).join("");
      html+=`<details class="card chapitre" ontoggle="chargerExosChapitre(event,${currentYear},${i})"><summary onclick="return gate(event)"><span>${c[1]}</span>${subscribed?"":"🔒"}</summary><div class="niveaux" id="exos-${currentYear}-${i}">${rows}</div></details>`;
    });
    html+="</div>";
  });
  document.getElementById("chapitres-list").innerHTML=html;
}
function gate(e){
  if(!subscribed){e.preventDefault();openPaywall();return false;}
  return true;
}
function setConseilView(v){
  document.getElementById("cg1").classList.toggle("active",v==="generaux");
  document.getElementById("cg2").classList.toggle("active",v==="chapitre");
  document.getElementById("conseils-generaux").classList.toggle("hidden",v!=="generaux");
  document.getElementById("conseils-chapitre").classList.toggle("hidden",v!=="chapitre");
}
function renderConseilsGeneraux(){
  document.getElementById("conseils-generaux").innerHTML=CONSEILS_GENERAUX.map(c=>`<details class="card chapitre"><summary onclick="return gate(event)"><span>${c[0]}</span>${subscribed?"":"🔒"}</summary><div class="niveaux">${c[1]}</div></details>`).join("");
}
function renderAiChapterList(containerId,type){
  let html="";
  [1,2].forEach(annee=>{
    html+=`<h3 class="domaine">${annee===1?"1ère":"2ème"} année</h3><div class="grid">`;
    CH[annee].forEach((c,idx)=>{
      const hint=type==="conseil"?"un conseil ciblé":"des questions de cours";
      html+=`<details class="card chapitre" ontoggle="handleAiToggle(event,'${type}',${annee},${idx})"><summary onclick="return gate(event)"><span>${c[1]}</span>${subscribed?"":"🔒"}</summary><div class="niveaux" id="${type}-${annee}-${idx}">Cliquez pour afficher ${hint}.</div></details>`;
    });
    html+="</div>";
  });
  document.getElementById(containerId).innerHTML=html;
}
async function handleAiToggle(e,type,annee,idx){
  if(!e.target.open) return;
  const nom=CH[annee][idx][1];
  const box=document.getElementById(`${type}-${annee}-${idx}`);
  if(box.dataset.loaded) return;
  box.dataset.loaded="1";
  const coll=type==="conseil"?"conseils_chapitre":"questions_cours";
  try{
    const db=await getDb();
    if(db){
      const snap=await db.collection(coll).doc(`${annee}-${idx}`).get();
      if(snap&&snap.exists){
        const d=snap.data();
        if(d&&d.texte){box.textContent=d.texte;return;}
        if(d&&d.items&&d.items.length){box.innerHTML=d.items.map(q=>`<p style="margin:6px 0"><b>Q :</b> ${q.question}<br><b>R :</b> ${q.reponse}</p>`).join("");return;}
      }
    }
  }catch(err){}
  if(!IA_ACTIF){box.textContent="🚧 Contenu généré par IA — arrive bientôt.";return;}
  box.textContent="Génération…";
  const prompts={
    conseil:`Tu es professeur de mathématiques en BCPST. Donne 3 conseils méthodologiques courts (à puces) pour réussir le chapitre "${nom}" (erreur classique à éviter, méthode clé, priorité de révision). Moins de 80 mots.`,
    kholle:`Tu es professeur de mathématiques en BCPST. Rédige 2 questions de cours courtes type khôlle sur le chapitre "${nom}", chacune suivie immédiatement de sa réponse concise. Moins de 100 mots au total.`
  };
  const offline={
    conseil:`(Aperçu hors-ligne) Conseils méthodologiques pour « ${nom} » générés par l'IA à la connexion.`,
    kholle:`(Aperçu hors-ligne) Questions de cours sur « ${nom} » générées par l'IA à la connexion.`
  };
  try{
    const sample=await getSample();
    if(!sample){box.textContent=offline[type];return;}
    const r=await sample(prompts[type],{modelTier:"quick"});
    box.textContent=r.text.trim();
  }catch(err){box.textContent="Contenu indisponible pour le moment.";}
}
async function chargerExosChapitre(e,annee,idx){
  if(!e.target.open) return;
  const box=document.getElementById(`exos-${annee}-${idx}`);
  if(box.dataset.loaded) return;
  box.dataset.loaded="1";
  try{
    const db=await getDb(); if(!db) return;
    const snap=await db.collection("exercices").doc(`${annee}-${idx}`).get();
    if(snap&&snap.exists){
      const d=snap.data();
      if(d&&d.items&&d.items.length){
        box.innerHTML=d.items.map(ex=>`<details style="border-top:1px solid var(--border);padding-top:8px;margin-top:8px"><summary style="cursor:pointer;font-weight:600;font-size:.86rem;list-style:none">${ex.niveau||""} — ${ex.titre||"Exercice"}</summary><div style="margin-top:6px;font-size:.85rem;white-space:pre-wrap">${ex.enonce||""}${ex.corrige?`<p style="color:var(--coral-d);margin-top:6px"><b>Corrigé :</b> ${ex.corrige}</p>`:""}</div></details>`).join("");
      }
    }
  }catch(err){}
}
async function chargerConseilsPersistes(){
  try{
    const db=await getDb(); if(!db) return;
    const snap=await db.collection("content").doc("conseils-generaux").get();
    if(snap&&snap.exists){
      const d=snap.data();
      if(d&&d.items&&d.items.length){CONSEILS_GENERAUX.length=0;CONSEILS_GENERAUX.push(...d.items);renderConseilsGeneraux();}
    }
  }catch(err){}
}
function setAdminView(v){
  const vues=["conseils","exos","conseilsch","kholle","annales"];
  vues.forEach((k,i)=>{
    document.getElementById("ad"+(i+1)).classList.toggle("active",k===v);
    document.getElementById("admin-"+k).classList.toggle("hidden",k!==v);
  });
}
function populateChapterSelect(id){
  const sel=document.getElementById(id);
  let html="";
  [1,2].forEach(an=>{
    html+=`<optgroup label="${an===1?"1ère":"2ème"} année">`;
    CH[an].forEach((c,idx)=>html+=`<option value="${an}|${idx}">${c[1]}</option>`);
    html+="</optgroup>";
  });
  sel.innerHTML=html;
}
function populateAdminAnneeSelect(){
  document.getElementById("admin-annee").innerHTML=ANNEES.map(a=>`<option>${a}</option>`).join("");
}
async function chargerAdminConseilCh(){
  const [an,idx]=document.getElementById("admin-ch-conseil").value.split("|");
  adminConseilChCourant={an,idx};
  document.getElementById("admin-conseil-texte").value="";
  try{
    const db=await getDb();
    if(db){const snap=await db.collection("conseils_chapitre").doc(`${an}-${idx}`).get();if(snap&&snap.exists){const d=snap.data();if(d&&d.texte)document.getElementById("admin-conseil-texte").value=d.texte;}}
  }catch(e){}
}
async function enregistrerConseilCh(){
  const texte=document.getElementById("admin-conseil-texte").value.trim();
  try{
    const db=await getDb();
    if(!db){toast("Enregistrement indisponible dans cet aperçu.");return;}
    await db.collection("conseils_chapitre").doc(`${adminConseilChCourant.an}-${adminConseilChCourant.idx}`).set({texte});
    toast("Conseil enregistré ✓ — visible par tous les visiteurs.");
  }catch(e){toast("Échec de l'enregistrement (droits d'édition requis).");}
}
async function chargerAdminKholle(){
  const [an,idx]=document.getElementById("admin-ch-kholle").value.split("|");
  adminKholleChCourant={an,idx}; adminKholleData=[];
  try{
    const db=await getDb();
    if(db){const snap=await db.collection("questions_cours").doc(`${an}-${idx}`).get();if(snap&&snap.exists){const d=snap.data();if(d&&d.items)adminKholleData=d.items;}}
  }catch(e){}
  renderAdminKholle();
}
function renderAdminKholle(){
  document.getElementById("admin-kholle-list").innerHTML=adminKholleData.map((q,i)=>`<div class="card"><input type="text" value="${(q.question||"").replace(/"/g,"&quot;")}" oninput="adminKholleData[${i}].question=this.value" placeholder="Question"><textarea style="min-height:50px;margin-top:8px" oninput="adminKholleData[${i}].reponse=this.value" placeholder="Réponse">${q.reponse||""}</textarea><button style="margin-top:8px;color:var(--coral-d);background:none;border:none;cursor:pointer" onclick="adminKholleData.splice(${i},1);renderAdminKholle()">Supprimer</button></div>`).join("");
}
function ajouterQuestionKholle(){adminKholleData.push({question:"",reponse:""});renderAdminKholle();}
async function enregistrerKholle(){
  try{
    const db=await getDb();
    if(!db){toast("Enregistrement indisponible dans cet aperçu.");return;}
    await db.collection("questions_cours").doc(`${adminKholleChCourant.an}-${adminKholleChCourant.idx}`).set({items:adminKholleData});
    toast("Questions enregistrées ✓ — visibles par tous les visiteurs.");
  }catch(e){toast("Échec de l'enregistrement (droits d'édition requis).");}
}
async function enregistrerAnnale(){
  const concours=document.getElementById("admin-concours").value;
  const annee=document.getElementById("admin-annee").value;
  const sujetUrl=document.getElementById("admin-sujet-url").value.trim();
  const corrigeUrl=document.getElementById("admin-corrige-url").value.trim();
  try{
    const db=await getDb();
    if(!db){toast("Enregistrement indisponible dans cet aperçu.");return;}
    await db.collection("annales").doc(`${concours}-${annee}`).set({sujetUrl,corrigeUrl});
    toast("Annale enregistrée ✓ — visible par tous les visiteurs.");
  }catch(e){toast("Échec de l'enregistrement (droits d'édition requis).");}
}
function renderAdminConseils(){
  document.getElementById("admin-conseils-list").innerHTML=adminConseilsData.map((c,i)=>`<div class="card"><input type="text" value="${(c[0]||"").replace(/"/g,"&quot;")}" oninput="adminConseilsData[${i}][0]=this.value" placeholder="Titre"><textarea style="min-height:60px;margin-top:8px" oninput="adminConseilsData[${i}][1]=this.value" placeholder="Texte">${c[1]||""}</textarea><button style="margin-top:8px;color:var(--coral-d);background:none;border:none;cursor:pointer" onclick="adminConseilsData.splice(${i},1);renderAdminConseils()">Supprimer</button></div>`).join("");
}
function ajouterConseilAdmin(){adminConseilsData.push(["Nouveau conseil",""]);renderAdminConseils();}
async function enregistrerConseils(){
  try{
    const db=await getDb();
    if(!db){toast("Enregistrement indisponible dans cet aperçu.");return;}
    await db.collection("content").doc("conseils-generaux").set({items:adminConseilsData});
    CONSEILS_GENERAUX.length=0;CONSEILS_GENERAUX.push(...adminConseilsData);
    renderConseilsGeneraux();
    toast("Conseils enregistrés ✓ — visibles par tous les visiteurs.");
  }catch(e){toast("Échec de l'enregistrement (droits d'édition requis).");}
}
function populateAdminChSelect(){
  const sel=document.getElementById("admin-ch");
  let html="";
  [1,2].forEach(an=>{
    html+=`<optgroup label="${an===1?"1ère":"2ème"} année">`;
    CH[an].forEach((c,idx)=>html+=`<option value="${an}|${idx}">${c[1]}</option>`);
    html+="</optgroup>";
  });
  sel.innerHTML=html;
  chargerAdminExos();
}
async function chargerAdminExos(){
  const [an,idx]=document.getElementById("admin-ch").value.split("|");
  adminChCourant={an,idx};
  adminExosData=[];
  try{
    const db=await getDb();
    if(db){
      const snap=await db.collection("exercices").doc(`${an}-${idx}`).get();
      if(snap&&snap.exists){const d=snap.data();if(d&&d.items)adminExosData=d.items;}
    }
  }catch(e){}
  renderAdminExos();
}
function renderAdminExos(){
  document.getElementById("admin-exos-list").innerHTML=adminExosData.map((ex,i)=>`<div class="card"><input type="text" value="${(ex.titre||"").replace(/"/g,"&quot;")}" oninput="adminExosData[${i}].titre=this.value" placeholder="Titre de l'exercice"><select style="margin-top:8px" onchange="adminExosData[${i}].niveau=this.value">${NIVEAUX.map(n=>`<option ${ex.niveau===n?"selected":""}>${n}</option>`).join("")}</select><textarea style="min-height:70px;margin-top:8px" oninput="adminExosData[${i}].enonce=this.value" placeholder="Énoncé">${ex.enonce||""}</textarea><textarea style="min-height:70px;margin-top:8px" oninput="adminExosData[${i}].corrige=this.value" placeholder="Corrigé">${ex.corrige||""}</textarea><button style="margin-top:8px;color:var(--coral-d);background:none;border:none;cursor:pointer" onclick="adminExosData.splice(${i},1);renderAdminExos()">Supprimer</button></div>`).join("");
}
function ajouterExoAdmin(){adminExosData.push({titre:"Nouvel exercice",niveau:NIVEAUX[0],enonce:"",corrige:""});renderAdminExos();}
async function enregistrerExos(){
  try{
    const db=await getDb();
    if(!db){toast("Enregistrement indisponible dans cet aperçu.");return;}
    await db.collection("exercices").doc(`${adminChCourant.an}-${adminChCourant.idx}`).set({items:adminExosData});
    toast("Exercices enregistrés ✓ — rouvrez le chapitre côté public pour les voir.");
  }catch(e){toast("Échec de l'enregistrement (droits d'édition requis).");}
}
async function initAdmin(){
  try{
    const user=await getUser();
    if(user&&user.canEdit&&user.canEdit()){
      estAdmin=true;
      document.getElementById("menu-admin").classList.remove("hidden");
      await chargerConseilsPersistes();
      adminConseilsData=CONSEILS_GENERAUX.map(c=>[c[0],c[1]]);
      renderAdminConseils();
      populateAdminChSelect();
      populateChapterSelect("admin-ch-conseil");chargerAdminConseilCh();
      populateChapterSelect("admin-ch-kholle");chargerAdminKholle();
      populateAdminAnneeSelect();
    }
  }catch(e){}
}
function setPrepMode(m){
  prepMode=m;
  const map={chapitre:"pm1",kholle:"pm2",upload:"pm3"};
  Object.keys(map).forEach(k=>{
    document.getElementById(map[k]).classList.toggle("active",k===m);
    document.getElementById("pm-"+k).classList.toggle("hidden",k!==m);
  });
}
function renderKholleChecklist(){
  let html="";
  [1,2].forEach(annee=>CH[annee].forEach((c,idx)=>{
    html+=`<label><input type="checkbox" value="${annee}|${idx}" onchange="limitKholle()"> ${c[1]}</label>`;
  }));
  document.getElementById("ia-kholle-list").innerHTML=html;
}
function limitKholle(){
  const boxes=[...document.querySelectorAll("#ia-kholle-list input")];
  const n=boxes.filter(i=>i.checked).length;
  boxes.forEach(i=>{i.disabled=n>=3&&!i.checked;});
}
function handleFileUpload(e){
  const f=e.target.files[0];
  const status=document.getElementById("ia-file-status");
  uploadedImageBase64=null;uploadedImageType=null;
  if(!f) return;
  if(!f.type.startsWith("image/")){status.textContent="Cette démo n'analyse que les photos (JPG/PNG). Pour un PDF, envoyez une capture d'écran de la page.";return;}
  const reader=new FileReader();
  reader.onload=()=>{uploadedImageBase64=reader.result.split(",")[1];uploadedImageType=f.type;status.textContent=`✓ ${f.name} prêt à être analysé par l'IA.`;};
  reader.readAsDataURL(f);
}
function toggleMenu(){document.getElementById("menu-dropdown").classList.toggle("hidden");}
function closeMenu(){document.getElementById("menu-dropdown").classList.add("hidden");}
document.addEventListener("click",e=>{if(!e.target.closest(".menu-wrap"))closeMenu();});
function renderFilters(){
  const all=["Tous",...CONCOURS];
  document.getElementById("filters").innerHTML=all.map(c=>`<button class="${c===filtreConcours?"active":""}" onclick="setFiltre('${c}')">${c}</button>`).join("");
}
function setFiltre(c){filtreConcours=c;renderFilters();renderAnnales();}
function renderAnnales(){
  const cs=filtreConcours==="Tous"?CONCOURS:[filtreConcours];
  let html="";
  cs.forEach(c=>{ANNEES.forEach(a=>{
    html+=`<div class="card annale"><div class="annale-head"><span>${c}</span><span>${a}</span></div><div class="annale-actions"><button onclick="telecharger('${c}',${a},'Sujet')">📄 Sujet ${subscribed?"":"🔒"}</button><button onclick="telecharger('${c}',${a},'Corrigé')">✅ Corrigé ${subscribed?"":"🔒"}</button></div></div>`;
  });});
  document.getElementById("annales-list").innerHTML=html;
}
async function telecharger(c,a,type){
  if(!subscribed){openPaywall();return;}
  try{
    const db=await getDb();
    if(db){
      const snap=await db.collection("annales").doc(`${c}-${a}`).get();
      if(snap&&snap.exists){
        const d=snap.data();
        const url=type==="Sujet"?d.sujetUrl:d.corrigeUrl;
        if(url){window.open(url,"_blank");return;}
      }
    }
  }catch(e){}
  toast(`${type} — ${c} ${a} : pas encore de lien enregistré.`);
}
function openPaywall(){document.getElementById("modal").classList.remove("hidden");}
function closeModal(){document.getElementById("modal").classList.add("hidden");}
function appliquerPromo(){
  const code=document.getElementById("promo-code").value.trim().toUpperCase();
  const msg=document.getElementById("promo-msg");
  const prix=document.getElementById("prix-affiche");
  if(CODES_PROMO[code]!==undefined){
    remise=CODES_PROMO[code];
    prix.innerHTML=`<span style="text-decoration:line-through;opacity:.5;font-size:1.1rem">10€</span> ${(10-remise).toFixed(2).replace(".00","")}€ <span>/ an</span>`;
    msg.style.color="var(--coral-d)";msg.textContent=`Code appliqué : -${remise}€ 🎉`;
  }else{
    remise=0;
    prix.innerHTML="10€ <span>/ an</span>";
    msg.style.color="var(--coral-d)";msg.textContent="Code promo invalide.";
  }
}
async function getDb(){try{return window.claude?await window.claude.use("db"):null;}catch(e){return null;}}
async function getUser(){try{return window.claude?await window.claude.use("user"):null;}catch(e){return null;}}
function connecterUI(d){
  compteConnecte=d;
  document.getElementById("compte-nom").textContent=`${d.prenom} ${d.nom}`;
  document.getElementById("compte-badge").classList.remove("hidden");
}
async function chargerCompte(){
  try{
    const user=await getUser();if(!user)return;
    const db=await getDb();if(!db)return;
    const snap=await db.doc(`data/users/${user.id()}/profile`).get();
    if(snap&&snap.exists){const d=snap.data();if(d&&d.email)connecterUI(d);}
  }catch(e){}
}
function openCompte(){
  if(compteConnecte){toast(`Connecté(e) en tant que ${compteConnecte.prenom} ${compteConnecte.nom}`);return;}
  document.getElementById("modal-compte").classList.remove("hidden");
}
function closeCompte(){document.getElementById("modal-compte").classList.add("hidden");}
function ouvrirInscription(){closeCompte();showTab("inscription");}
async function seConnecter(){
  const email=document.getElementById("login-email").value.trim().toLowerCase();
  const pass=document.getElementById("login-pass").value;
  if(!email||!pass){toast("Merci de renseigner votre e-mail et votre mot de passe.");return;}
  try{
    const user=await getUser();const db=await getDb();
    if(user&&db){
      const snap=await db.doc(`data/users/${user.id()}/profile`).get();
      if(snap&&snap.exists){
        const d=snap.data();
        if(d&&d.email&&d.email.toLowerCase()===email){connecterUI(d);closeCompte();toast(`Connecté(e) — bon retour ${d.prenom} 🛟`);return;}
      }
    }
  }catch(e){}
  toast("Aucun compte retrouvé pour cet e-mail sur cet appareil. Créez votre compte.");
}
async function creerCompte(){
  const nom=document.getElementById("inscr-nom").value.trim();
  const prenom=document.getElementById("inscr-prenom").value.trim();
  const email=document.getElementById("inscr-email").value.trim();
  const pass=document.getElementById("inscr-pass").value;
  const decouverte=document.getElementById("inscr-decouverte").value;
  if(!nom||!prenom||!email||!pass){toast("Merci de remplir tous les champs.");return;}
  const profil={nom,prenom,email,decouverte,creeLe:new Date().toISOString()};
  try{
    const user=await getUser();const db=await getDb();
    if(user&&db){await db.doc(`data/users/${user.id()}/profile`).set(profil);}
  }catch(e){}
  connecterUI(profil);
  toast(`Compte créé — bienvenue ${prenom} 🛟`);
  showTab("accueil");
}
function subscribe(){
  subscribed=true;closeModal();
  const b=document.getElementById("sub-btn");
  b.textContent="✓ Abonné (1 an)";b.classList.add("subscribed");b.onclick=null;
  renderChapitres();renderAnnales();renderConseilsGeneraux();renderAiChapterList("conseils-chapitre-list","conseil");renderAiChapterList("kholle-questions-list","kholle");
  toast(remise>0?`Abonnement activé avec -${remise}€ (démo) — bienvenue à bord 🛟`:"Abonnement activé (démo) — bienvenue à bord 🛟");
}
function toast(msg){
  const t=document.createElement("div");t.className="toast";t.textContent=msg;
  document.body.appendChild(t);
  requestAnimationFrame(()=>t.classList.add("show"));
  setTimeout(()=>{t.classList.remove("show");setTimeout(()=>t.remove(),300);},2600);
}
function populateChSelect(){
  const sel=document.getElementById("ia-ch");
  let html="";
  [1,2].forEach(an=>{
    html+=`<optgroup label="${an===1?"1ère":"2ème"} année">`;
    CH[an].forEach(c=>html+=`<option value="${an}|${c[1]}">${c[1]}</option>`);
    html+="</optgroup>";
  });
  sel.innerHTML=html;
}
async function demarrerPrepIA(){
  if(!subscribed){openPaywall();return;}
  let nom="";
  if(prepMode==="chapitre"){
    nom=document.getElementById("ia-ch").value.split("|")[1];
  }else if(prepMode==="kholle"){
    const sel=[...document.querySelectorAll("#ia-kholle-list input:checked")].map(i=>{const [a,idx]=i.value.split("|");return CH[a][idx][1];});
    if(sel.length<2){toast("Sélectionnez au moins 2 chapitres pour le programme de khôlle.");return;}
    nom=sel.join(", ");
  }else{
    nom=uploadedImageBase64?"le programme personnalisé envoyé en photo":"des révisions générales BCPST (aucune photo fournie)";
  }
  document.getElementById("ia-setup").classList.add("hidden");
  document.getElementById("ia-session").classList.remove("hidden");
  document.getElementById("ia-resultat").classList.add("hidden");
  document.getElementById("ia-chapitre-label").textContent=nom;
  document.getElementById("ia-enonce").textContent="Génération de l'exercice…";
  document.getElementById("ia-reponse").value="";
  window._iaChapitre=nom;
  startTimer(parseInt(document.getElementById("ia-duree").value,10));
  const enonce=await genererExercice(nom, prepMode==="upload"?uploadedImageBase64:null, prepMode==="upload"?uploadedImageType:null);
  document.getElementById("ia-enonce").textContent=enonce;
  window._iaEnonce=enonce;
}
function startTimer(sec){
  timeLeft=sec;updateTimerDisplay();clearInterval(timerInterval);
  timerInterval=setInterval(()=>{
    timeLeft--;updateTimerDisplay();
    if(timeLeft<=0){clearInterval(timerInterval);envoyerPrepIA();}
  },1000);
}
function updateTimerDisplay(){
  const m=Math.floor(timeLeft/60), s=timeLeft%60;
  document.getElementById("ia-timer").textContent=`⏱ ${m}:${String(s).padStart(2,"0")}`;
}
async function getSample(){
  try{ return window.claude ? await window.claude.use("sample") : null; }catch(e){ return null; }
}
async function genererExercice(nom,imgB64,imgType){
  if(!IA_ACTIF) return "🚧 La génération d'exercices par IA arrive bientôt. En attendant, explorez librement l'interface.";
  try{
    const sample=await getSample();
    if(!sample) return `(Aperçu hors-ligne) Un exercice type sur « ${nom} » apparaîtrait ici, généré par l'IA.`;
    let prompt, opts={modelTier:"quick"};
    if(imgB64){
      prompt="Tu es professeur de mathématiques en classe préparatoire BCPST. Voici en photo le programme de révision personnalisé de l'élève. Identifie les chapitres visés puis rédige un unique exercice de niveau concours (8 à 12 lignes) qui les combine, sans corrigé ni préambule.";
      opts.images=[{data:imgB64,media_type:imgType}];
    }else{
      prompt=`Tu es professeur de mathématiques en classe préparatoire BCPST. Rédige un unique exercice de niveau concours (8 à 12 lignes), sans corrigé ni préambule, portant sur : ${nom}.`;
    }
    const res=await sample(prompt,opts);
    return res.text.trim();
  }catch(e){return "Exercice indisponible pour le moment (photo trop lourde ou programme non détecté). Réessayez ou choisissez un chapitre manuellement.";}
}
async function envoyerPrepIA(){
  clearInterval(timerInterval);
  const reponse=document.getElementById("ia-reponse").value.trim();
  document.getElementById("ia-session").classList.add("hidden");
  document.getElementById("ia-resultat").classList.remove("hidden");
  const box=document.getElementById("ia-correction");
  box.textContent="Analyse de votre copie par l'IA…";
  box.textContent=await corrigerReponse(window._iaChapitre,window._iaEnonce,reponse||"(Aucune réponse rédigée avant la fin du temps imparti.)");
}
async function corrigerReponse(nom,enonce,reponse){
  if(!IA_ACTIF) return "🚧 La correction par IA arrive bientôt. Votre réponse a bien été reçue et sera analysée dès l'activation de cette fonctionnalité.";
  try{
    const sample=await getSample();
    if(!sample) return "La correction par IA nécessite d'être connecté sur claude.ai. Exemple : structure correcte, mais justifiez mieux les hypothèses du théorème utilisé. Note indicative : 12/20.";
    const prompt=`Tu es correcteur de concours pour la filière BCPST. Chapitre : ${nom}.\nÉnoncé : ${enonce}\nRéponse de l'étudiant : ${reponse}\nRédige une correction bienveillante et rigoureuse en français (150 mots maximum) : appréciation générale, points corrects, erreurs ou points à travailler, puis une note indicative sur 20.`;
    const r=await sample(prompt,{modelTier:"default"});
    return r.text.trim();
  }catch(e){return "La correction n'a pas pu être générée pour le moment. Réessayez dans un instant.";}
}
function resetPrepIA(){
  document.getElementById("ia-resultat").classList.add("hidden");
  document.getElementById("ia-setup").classList.remove("hidden");
}
populateChSelect();renderChapitres();renderFilters();renderAnnales();renderConseilsGeneraux();renderAiChapterList("conseils-chapitre-list","conseil");renderAiChapterList("kholle-questions-list","kholle");renderKholleChecklist();chargerCompte();chargerConseilsPersistes();initAdmin();
</script>
</body>
</html>
