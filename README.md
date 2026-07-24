# nol.dotenv

Chargement de fichiers .env en pur [Nolc](https://noliae-nolc.s3.gra.io.cloud.ovh.net/nolc-latest-linux-x86_64.tar.gz), sans dépendance.

## Installation

```toml
[dependances]
"nol-dotenv" = { git = "https://github.com/Noliae-France/nol-dotenv" }
```

## API
`dotenv_charge(chemin)`, `dotenv_parse(contenu)`, `dotenv_lire(env, cle)`, `dotenv_ou(env, cle, defaut)`. Ignore lignes vides et commentaires `#`, retire les guillemets. Fichier absent = map vide.

```nol
let env = dotenv_charge(".env")
let hote = dotenv_ou(env, "HOST", "localhost")
```

## Licence

MIT © 2026 Bastien LANGUEDOC.
