# Fading-Echo-Modding -FR

<img width="1670" height="936" alt="image" src="https://github.com/user-attachments/assets/c774dbea-9f85-4399-b413-7e6268afa03b" />


# Guide Complet : Modifier les Textes de Localisation dans Fading Echo Demo

## Prérequis
- FModel installé
- Outil UnrealPak téléchargé
- Un éditeur .locres (choisissez-en un parmi les options ci-dessous)

## Étape 1 : Extraire le Fichier de Localisation

1. Ouvrez FModel
2. Naviguez vers : `UE_YGRO/Content/Localization/Game/fr/Game.locres`
3. Faites un clic droit sur `Game.locres` et extrayez-le sur votre ordinateur

## Étape 2 : Modifier le Fichier de Localisation

Choisissez l'un de ces éditeurs pour modifier le fichier .locres :

**Option A - Unreal Locres Editor (GUI - Recommandé) :**
- Télécharger : https://github.com/snoozeds/UnrealLocresEditor

**Option B - LocresStudio :**
- Télécharger : https://github.com/AcTePuKc/LocresStudio

**Option C - UE4-locres-Online-Editor :**
- Accéder : https://github.com/klimaleksus/UE4-locres-Online-Editor

**Option D - UEExtractor (Ligne de commande) :**
- Télécharger : https://github.com/SolicenTEAM/UEExtractor

Ouvrez votre fichier `Game.locres` extrait dans l'éditeur, trouvez le texte que vous voulez modifier, changez-le et sauvegardez le fichier.

## Étape 3 : Créer la Structure de Dossiers du Mod

Créez un dossier avec cette structure exacte (le nom du dossier doit se terminer par `_P`) :

```
CustomLocres_P/
└── UE_YGRO/
    └── Content/
        └── Localization/
            └── Game/
                └── fr/
                    └── Game.locres (votre fichier modifié)
```

Placez votre fichier `Game.locres` modifié dans le dossier `fr`.

## Étape 4 : Télécharger UnrealPak

Téléchargez l'outil UnrealPak autonome :
- Télécharger : https://github.com/Dmgvol/UE_Modding/raw/main/Tools/UnrealPak.zip

Extrayez-le dans un dossier. Vous devriez voir :
- `UnrealPak-With-compression.bat`
- `UnrealPak.exe`
- D'autres fichiers de support

## Étape 5 : Créer le Fichier .pak

**Méthode A - Utilisation du Fichier Batch (Le plus simple) :**
- Glissez-déposez votre dossier `CustomLocres_P` sur `UnrealPak-With-compression.bat`
- Cela créera automatiquement `CustomLocres_P.pak`

**Méthode B - Utilisation de la Ligne de Commande :**
1. Ouvrez l'Invite de Commandes dans le dossier UnrealPak
2. Créez un fichier filelist.txt avec le chemin vers votre dossier de mod
3. Exécutez :
```
UnrealPak.exe "C:\chemin\vers\CustomLocres_P.pak" -create=filelist.txt -compress
```

## Étape 6 : Installer le Mod

1. Naviguez vers le dossier Paks du jeu :
```
Steam\steamapps\common\Fading Echo Demo\UE_YGRO\Content\Paks
```

2. Copiez votre fichier `CustomLocres_P.pak` dans ce dossier

## Étape 7 : Créer les Fichiers IoStore (Requis pour les jeux UE5 avec .ucas/.utoc)

Puisque votre jeu utilise le format IoStore (vous avez des fichiers `.ucas` et `.utoc`) :

1. Dans le dossier Paks, localisez `global.ucas` et `global.utoc`
2. Copiez `global.ucas` et renommez la copie en `CustomLocres_P.ucas`
3. Copiez `global.utoc` et renommez la copie en `CustomLocres_P.utoc`

Votre dossier Paks devrait maintenant contenir :
- global.ucas
- global.utoc
- UE_YGRO-Windows.pak
- UE_YGRO-Windows.ucas
- UE_YGRO-Windows.utoc
- CustomLocres_P.pak
- CustomLocres_P.ucas
- CustomLocres_P.utoc

## Étape 8 : Tester le Jeu

Lancez Fading Echo Demo et vérifiez que votre texte modifié apparaît.

## Dépannage

Si les changements n'apparaissent pas :
- Vérifiez que la structure des dossiers correspond exactement
- Assurez-vous que le nom du dossier se termine par `_P`
- Vérifiez que le fichier .locres est dans le bon dossier de langue (`fr` pour le français)
- Le texte pourrait être dans un autre fichier .locres (comme `Engine.locres`)
- Le texte pourrait être codé en dur dans un widget ou un blueprint

## Ressources Supplémentaires

- Documentation de Localisation Unreal Engine : https://docs.unrealengine.com/
- FModel GitHub : https://github.com/4sval/FModel
- Communauté de Modding UE : https://www.nexusmods.com/
- Collection d'Outils de Modding UE : https://github.com/Dmgvol/UE_Modding

## Crédits

- Outil UnrealPak : https://github.com/Dmgvol/UE_Modding
- Guides et tutoriels de la communauté de modding Unreal Engine

---

Ce guide a été testé sur la démo Fading Echo.  
Notez que la procédure peut varier pour d'autres modifications autres que celles-ci.  

Ce guide a été entièrement rédigé par une intelligence artificielle.
