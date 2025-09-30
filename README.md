# Automatisation : Événements gratuits Montpellier

Ce dépôt génère automatiquement un calendrier des événements gratuits à Montpellier et dans un rayon de 20 km.

## Contenu

- `agenda_montpellier_auto.py` : script Python qui interroge l’API OpenDataSoft, filtre les événements gratuits et exporte CSV/XLSX colorés.
- `requirements.txt` : dépendances Python.
- `.github/workflows/auto_agenda.yml` : workflow GitHub Actions qui s’exécute chaque jour.

## Utilisation

1. Créez un dépôt GitHub et copiez-y tous les fichiers de cette archive.
2. Activez **Actions** dans GitHub.
3. Chaque jour à 03h30 UTC, le script génère les fichiers :
   - `evenements_montpellier_auto.xlsx`
   - `INTRA_montpellier_gratuits.csv`
   - `OUTSIDE_20km_gratuits.csv`
4. Les fichiers sont disponibles comme artifacts téléchargeables dans l’onglet **Actions**.

## Personnalisation

- La détection de la gratuité repose sur les mots-clés "gratuit" ou "entrée libre".
- Les couleurs sont appliquées par mots-clés (concert, théâtre, enfant, cinéma, reste).
- Pour changer l’heure ou fréquence d’exécution, modifiez la ligne `cron` dans `.github/workflows/auto_agenda.yml`.
