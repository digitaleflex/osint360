# OSINT 360° — Conférence

Site de l'événement **OSINT 360°** : conférence en direct sur TikTok LIVE, samedi 14 novembre 2026 à 20 h (UTC+1).

Site statique (HTML/CSS/JS, aucune dépendance, aucun build).

## Structure

```
index.html                    page unique (styles et scripts inclus)
assets/logo.webp              logo du hero
assets/favicon.webp           icône d'onglet
assets/apple-touch-icon.png   icône écran d'accueil iOS
assets/osint360-banniere.webp bannière utilisée pour l'aperçu de partage (og:image)
vercel.json                   cache des assets + en-têtes de sécurité
```

## Configuration

En haut de `index.html`, bloc `CONFIGURATION` :

- `WHATSAPP_GROUP_URL` — lien d'invitation du groupe WhatsApp
- `EVENT_DATE` — date/heure du direct (ISO 8601 avec fuseau)
- `EVENT_DURATION_MIN` — durée estimée (agenda + passage « en direct » → « terminé »)

Si le domaine final n'est pas `osint360.vercel.app`, mettre à jour l'URL absolue de `og:image`.

## Déploiement Vercel

Importer le dépôt dans Vercel → Framework preset **Other** → aucun build command, output directory `.` → Deploy.

## Test en local

```bash
npx serve .
```
