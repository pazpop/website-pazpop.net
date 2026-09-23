# pazpop.net

Site personnel de pazpop, déployé automatiquement sur l'hébergeur via FTP.

## Structure

```
www/            Racine du site servie par l'hébergeur
  index.html
  favicon.ico
  img/
.github/
  workflows/
    deploy.yml  CI/CD : déploiement FTP à chaque push sur main
```

## Déploiement

Un push sur `main` déclenche le workflow GitHub Actions [deploy.yml](.github/workflows/deploy.yml),
qui synchronise le contenu de `www/` vers `public_html/` sur le serveur FTP.

Secrets requis (Settings → Secrets and variables → Actions) :

- `FTP_SERVER`
- `FTP_USERNAME`
- `FTP_PASSWORD`

## Licence

MIT — voir [LICENSE](LICENSE).
