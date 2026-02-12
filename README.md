# fix-webmethods-readme

Collection de fichiers readme des correctifs (fixes) IBM webMethods, organisés par version et par code trigramme de composant.

Ce dépôt est utilisé comme source de données par l'application [IBM Fixes](https://ibmfixes.ismael.best) pour afficher le contenu des readmes de correctifs. Il s'agit d'un projet personnel, non affilié à IBM.

## Structure du dépôt

```
fix-webmethods-readme/
├── 105/          # webMethods 10.5
├── 107/          # webMethods 10.7
├── 111/          # webMethods 10.11
├── 1011/         # webMethods 10.11 (alt)
├── 1015/         # webMethods 10.15
└── README.md
```

Chaque répertoire de version contient des sous-répertoires nommés par trigramme de composant (ex: `CHE`, `WEL`, `TPS`, `ESB`...), qui contiennent les fichiers `.txt` readme des correctifs correspondants.

## Versions disponibles

| Version | Composants | Fichiers readme |
|---------|-----------|-----------------|
| 10.5    | 100       | 236             |
| 10.7    | 99        | 227             |
| 10.11   | 81        | 258             |
| 10.11   | 102       | 260             |
| 10.15   | 104       | 347             |

## Alimentation

Les fichiers readme sont extraits via IBM Software Update Manager (SUM), puis triés automatiquement par trigramme grâce à l'outil `TriFichiersParTrigramme`.