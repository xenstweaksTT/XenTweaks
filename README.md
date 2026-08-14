# Xen Utility — mises à jour

Dépôt **public**. Les PC lisent `xen-update.json` au lancement.

## 1. Créer le dépôt GitHub

1. github.com → **New repository**
2. Nom : `xen-utility-updates`
3. **Public**
4. Upload les fichiers de **ce dossier** (sauf le dossier `release/`)

## 2. Publier l’installeur (Release)

1. GitHub → **Releases** → **Create a new release**
2. Tag : `v2.0.0`
3. Joindre le fichier : `release/SetupXenUtility.exe`
4. Publier

## 3. Corriger les URLs

Dans `xen-update.json`, remplace `TON-COMPTE` et `TON-REPO` par ton vrai compte et le nom du repo.

Exemple d’URL du JSON (bouton **Raw** sur GitHub) :

`https://raw.githubusercontent.com/TON-COMPTE/TON-REPO/main/xen-update.json`

Colle cette URL dans l’app, fichier `opti_product.json` :

```json
"updateManifestUrl": "https://raw.githubusercontent.com/TON-COMPTE/TON-REPO/main/xen-update.json"
```

## 4. Prochaine version (ex. 2.0.1)

1. Passe `"version"` à `2.0.1` dans `xen-update.json`
2. Mets le nouveau `SetupXenUtility.exe` dans une Release `v2.0.1`
3. Mets à jour le champ `"url"` vers ce fichier
4. Commit / push `xen-update.json`

Les PC voient **Mettre à jour** au prochain lancement.
