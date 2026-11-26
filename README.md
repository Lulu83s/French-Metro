# 🚇 French Metro

**Simulateur de métro VAL** — prends les commandes d'une rame **VAL 206** sur la ligne M2 du métro de Lille : stations, signalisation, météo, trafic, piétons, trams IA, multijoueur et compatibilité avec un **manipulateur USB**.

> Jeu non officiel, sans lien avec l'exploitant du réseau.
> Fait avec [Godot Engine](https://godotengine.org) 4.7.

---

## ✨ Fonctionnalités

- Conduite réaliste : traction, freinage, neutre, freinage d'urgence, **VACMA**, portes, pantographe, annonces en station
- Arrêts précis au repère de quai, voyageurs qui montent et descendent
- Cycle jour / nuit, **pluie**, **neige**, lampadaires et éclairage dynamique
- Rames IA, circulation routière, piétons, carrefours et giratoires
- Système d'**XP**, de **missions** et de **lignes à débloquer**
- **Multijoueur** : parties publiques, privées, ou entre amis (même Wi-Fi ou Internet)
- Tutoriel intégré
- Prise en charge du **manipulateur USB** (ou du clavier) ; **commandes tactiles** sur Android
- Réglages graphiques complets (de « Rapide » à « Beau ») pour s'adapter à ta machine

---

## 📥 Téléchargement

Rends-toi dans l'onglet **[Releases](https://github.com/Lulu83s/French-Metro/releases)** du dépôt et télécharge le fichier correspondant à ton appareil :

| Plateforme | Fichier | Remarque |
|---|---|---|
| 🪟 Windows (PC) | `VoieLibre.exe` | 64 bits, un seul fichier |
| 🤖 Android | `VoieLibre.apk` | Appareil **arm64** (tous les téléphones récents) |
| 🍎 macOS | voir [la section Mac](#-macos) | Lancement depuis Godot, ou export à faire |
| 🐧 Linux | `VoieLibre.x86_64` | Bonus, 64 bits |

---

## 🪟 Installation sur PC (Windows)

**Configuration conseillée :** Windows 10 ou 11 (64 bits), carte graphique compatible **Vulkan** (pilotes à jour). Le jeu génère le décor au lancement : plus la machine est récente, mieux c'est.

1. Télécharge `VoieLibre.exe` depuis les [Releases](https://github.com/Lulu83s/French-Metro/releases).
2. Place-le dans un dossier de ton choix (par exemple `C:\Jeux\French Metro\`).
3. Double-clique dessus pour lancer le jeu.
4. Si Windows affiche **« Windows a protégé votre PC »** (SmartScreen) : clique sur **Informations complémentaires**, puis **Exécuter quand même**. Ce message apparaît pour toutes les applications non signées.

**Bon à savoir**
- Aucune installation : le jeu tient dans un seul `.exe`.
- Sur PC, le jeu peut **se mettre à jour automatiquement** au lancement quand une nouvelle version est disponible.
- Tes réglages et ta progression (XP, lignes débloquées) sont dans `%APPDATA%\Godot\app_userdata\French Metro\`.
- Pour désinstaller : supprime le `.exe` (et ce dossier de sauvegarde si tu veux tout effacer).

---

## 🤖 Installation sur Android

**Configuration conseillée :** téléphone ou tablette **récent** (processeur arm64), orientation **paysage**. Le jeu est lourd : démarre en qualité **« Basse »** (c'est le réglage par défaut sur mobile).

1. Télécharge `VoieLibre.apk` depuis les [Releases](https://github.com/Lulu83s/French-Metro/releases) directement sur ton téléphone.
2. Ouvre le fichier téléchargé (depuis la notification ou l'application **Fichiers**).
3. Android te demande d'autoriser l'installation depuis cette source :
   - appuie sur **Paramètres**, puis active **Autoriser depuis cette source** (le navigateur ou l'application Fichiers que tu utilises) ;
   - reviens en arrière et appuie sur **Installer**.
4. Si **Play Protect** affiche un avertissement, choisis **Installer quand même** (l'application n'est pas publiée sur le Play Store).
5. Lance **French Metro** depuis ton écran d'accueil.

**Commandes tactiles**
- **Levier** à gauche : pose ou glisse le doigt sur un cran (T4 … N … F1 … FM, FU)
- Gros bouton **VACMA** (à maintenir), bouton **FU** (urgence) et bouton **N** (neutre)
- Boutons : Portes, Caméra, Cabine, Klaxon, Gong, Annonce, Sable, Essuie-glaces, SAE, Pause
- Un doigt sur la vue : regarder autour de soi ; deux doigts : zoom
- Le bouton **Retour** d'Android ouvre la pause

**Bon à savoir**
- Sur Android, **il n'y a pas de mise à jour automatique** : pour mettre à jour, réinstalle simplement le nouvel APK par-dessus l'ancien (tu gardes ta progression).
- L'accès Internet est nécessaire pour le multijoueur.
- La version Android est encore **en phase de test** : si le jeu lag, passe en qualité « Basse » dans **Paramètres > Graphismes**.

---

## 🍎 macOS

> ⚠️ Aucun export macOS n'est encore publié dans les Releases. Deux solutions :

### Option A : lancer le jeu depuis Godot (la plus simple)

1. Télécharge **Godot 4.7.2** (version standard, pas .NET) sur [godotengine.org/download](https://godotengine.org/download/macos/) et glisse l'application dans **Applications**.
2. Récupère le projet : **Code > Download ZIP** sur la page GitHub (puis décompresse), ou `git clone https://github.com/Lulu83s/French-Metro.git`.
3. Ouvre Godot, clique sur **Importer**, choisis le fichier `project.godot` du dossier du jeu, puis **Importer et modifier**.
4. Attends la fin de l'importation (la première fois, c'est long), puis appuie sur **▶ (F5)** pour lancer le jeu.
5. Si macOS bloque Godot au premier démarrage : **clic droit sur l'application > Ouvrir > Ouvrir**.

### Option B : application `.app` / `.dmg` (si une version macOS est publiée)

1. Télécharge le fichier macOS depuis les [Releases](https://github.com/Lulu83s/French-Metro/releases) et décompresse-le.
2. Glisse **French Metro** dans **Applications**.
3. L'application n'étant pas signée par Apple, **ne double-clique pas** la première fois : fais **clic droit > Ouvrir**, puis confirme. Autre méthode : **Réglages Système > Confidentialité et sécurité**, puis **Ouvrir quand même**.
4. Si le message « l'application est endommagée » apparaît, ouvre le Terminal et tape :
   ```bash
   xattr -dr com.apple.quarantine "/Applications/French Metro.app"
   ```

---

## 🐧 Linux (bonus)

```bash
chmod +x VoieLibre.x86_64
./VoieLibre.x86_64
```

Ou utilise le script `VoieLibre.sh` fourni, placé dans le même dossier que l'exécutable.

---

## 🎮 Commandes clavier

| Touche | Action | Touche | Action |
|---|---|---|---|
| `D` | Traction | `H` | Klaxon |
| `Q` | Frein | `B` | Gong |
| `N` | Neutre | `X` | Sable |
| `F` | Urgence | `E` | Essuie-glaces |
| `Espace` | VACMA (à maintenir) | `P` | Pantographe |
| `O` | Portes | `I` | Écran SAE |
| `C` | Caméra | `V` | Annonce |
| `R` | Changer de cabine | | |

**Manipulateur USB :** branche-le **avant** de lancer le jeu. Le lobby affiche *« Commandes : manipulateur USB »* quand il est reconnu, avec un bouton pour **recalibrer le neutre**.

---

## 🌐 Multijoueur

Depuis l'accueil, ouvre **Multijoueur** :

- Choisis ton **pseudo**
- **Rejoins** une partie publique de la liste (bouton *Actualiser*)
- Ou **crée** une partie publique / privée
- Ou **héberge une partie entre amis** : ils se connectent directement à toi (même Wi-Fi, ou via Internet). Fonctionne aussi sur téléphone.

---

## ⚙️ Réglages

Accueil > **Options** (ou **Paramètres** dans le lobby et le menu pause) :

- **Graphismes** : préréglage Rapide / Équilibré / Beau / Personnalisé, résolution 3D, ombres, distance d'affichage, pluie et neige…
- **Affichage** : limite de FPS, VSync, plein écran, luminosité
- **Son** : volume général, **musique des menus** (activable / désactivable), annonces voyageurs
- **Jeu** : VACMA, tutoriel avant de conduire

Les réglages s'appliquent en direct et sont sauvegardés automatiquement.

---

## 🛠️ Dépannage

| Problème | Solution |
|---|---|
| Le jeu lag | Paramètres > Graphismes > préréglage **Rapide**, et baisse la distance d'affichage |
| Écran noir ou plantage au lancement (PC) | Mets à jour les pilotes de ta carte graphique (Vulkan requis) |
| Démarrage long | Normal : le décor est généré au lancement de la partie |
| Le manipulateur USB n'est pas détecté | Branche-le avant de lancer le jeu, puis relance |
| Pas de musique dans les menus | Vérifie **Paramètres > Son > Musique des menus** et le volume |
| Multijoueur indisponible | Vérifie ta connexion Internet, puis clique sur *Actualiser* ; sinon joue en solo ou héberge entre amis |

Un autre souci ? Ouvre une [issue](https://github.com/Lulu83s/French-Metro/issues) en indiquant ton appareil, ton système et ce qui s'est passé.

---

## 👨‍💻 Pour les développeurs

### Lancer depuis les sources

1. Installe **Godot 4.7.2** (version standard).
2. Clone le dépôt : `git clone https://github.com/Lulu83s/French-Metro.git`
3. Importe `project.godot` dans Godot, puis lance avec **F5**. La scène principale est `res://scenes/accueil.tscn`.

### Exporter le jeu

Installe d'abord les **modèles d'export** : *Éditeur > Gérer les modèles d'export*. Puis *Projet > Exporter* :

| Plateforme | Preset | Sortie |
|---|---|---|
| Windows | `Windows Desktop` (déjà configuré) | `VoieLibre.exe` |
| Linux | `Linux` (déjà configuré) | `VoieLibre.x86_64` |
| Android | `Android` (déjà configuré, arm64) | `VoieLibre.apk` |
| macOS | À ajouter : *Ajouter… > macOS*, architecture **universal** | `.app` / `.zip` |

**Android :** il faut le SDK Android et un JDK, à configurer dans *Éditeur > Paramètres de l'éditeur > Export > Android* (Godot indique les versions attendues). Le preset autorise Internet et active le plein écran immersif. Voir aussi `LISEZMOI_ANDROID.md`.

**macOS :** sans compte développeur Apple, l'application exportée n'est pas signée (voir les astuces de lancement plus haut).

### Structure du projet

```
autoload/    Services globaux (réglages, multijoueur, musique, tactile, manipulateur…)
scenes/      Scènes principales (accueil, lobby, jeu)
scripts/     Code du jeu (tram, génération du décor, trafic, interface…)
lignes/      Les lignes de métro
modeles/     Modèles 3D (.glb)
sons/        Sons et musique
images/      Images de l'interface
```

---

## 🙏 Crédits

- Conception et développement : **French Metro** ([@Lulu83s](https://github.com/Lulu83s))
- Moteur : [Godot Engine](https://godotengine.org)
- Inspiration : réseau de métro de Lille

---

⭐ Si le projet te plaît, n'hésite pas à lui mettre une étoile sur GitHub !
