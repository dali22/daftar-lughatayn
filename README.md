# دفتر لغتين — version Android

Application de révision anglais/français (programme de 12 semaines), empaquetée dans une WebView Android.
Tout fonctionne hors ligne ; les données restent dans le téléphone (pense à la sauvegarde dans l'onglet « البرنامج »).

## Option A — Android Studio (le plus simple)
1. Décompresse le dossier `LughatayApp`.
2. Android Studio → *File › Open* → choisis le dossier. Laisse la synchronisation Gradle se terminer
   (il télécharge Gradle 8.7, le plugin Android et le SDK 34 si besoin).
3. *Build › Build App Bundle(s) / APK(s) › Build APK(s)*.
4. L'APK est dans `app/build/outputs/apk/debug/app-debug.apk`. Copie-le sur le téléphone et installe-le
   (autorise « installer des applications inconnues » pour ton gestionnaire de fichiers).

Si Android Studio propose de mettre à jour le plugin Android (AGP), tu peux accepter.

## Option B — sans rien installer (GitHub Actions)
1. Crée un dépôt GitHub privé et pousse ce dossier.
2. L'onglet *Actions* lance « Build APK » automatiquement.
3. Quand c'est vert, télécharge l'artefact `daftar-lughatayn-apk` (un .zip contenant l'APK).

## Ce que la version Android ajoute
- Polices intégrées (fonctionne sans internet).
- Prononciation via le moteur « synthèse vocale » d'Android. Installe les voix anglaise et française dans
  *Paramètres › Accessibilité/Système › Synthèse vocale* si le son ne marche pas.
- Vibration à la fin des minuteurs, écran maintenu allumé pendant un minuteur.
- Liens externes ouverts dans le navigateur ; bouton retour du téléphone géré.
- Sauvegarde/restauration par copier-coller (onglet « البرنامج »).

## Modifier le contenu
Toute l'application est dans `app/src/main/assets/index.html` (cartes, sujets, programme).
