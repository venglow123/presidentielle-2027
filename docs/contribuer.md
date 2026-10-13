# Contribuer

Ce wiki est ouvert à toutes et à tous. Voici comment participer.

## Modifier une page

1. Ouvrez la page à modifier sur le site.
2. Cliquez sur le bouton ✏️ en haut de la page : vous êtes redirigé vers l'éditeur GitHub.
3. Modifiez le contenu, puis proposez les changements (« Propose changes »).
4. GitHub crée une Pull Request ; elle sera relue avant fusion.

## Ajouter un sujet

1. Créez un fichier Markdown dans `docs/sujets/`, par exemple `docs/sujets/mon-sujet.md`.
2. Partez de la page [exemple](sujets/exemple.md) : sections **Contexte** et **Sources**.
3. Ajoutez la page dans la section `nav` de `mkdocs.yml` :

    ```yaml
    nav:
      - Sujets:
          - sujets/index.md
          - Mon sujet: sujets/mon-sujet.md
    ```

4. Ajoutez un lien vers la page dans `docs/sujets/index.md`.
5. Ouvrez une Pull Request.

## Bonnes pratiques

- **Citez vos sources** : chaque affirmation factuelle doit renvoyer à une source vérifiable.
- **Restez neutre** : décrivez, ne jugez pas ; présentez les positions de manière équilibrée.
- **Un sujet par page** : privilégiez des pages courtes et ciblées.
- Rédigez en français, avec un style clair.

## Prévisualisation locale

```bash
python -m venv .venv
pip install -r requirements.txt
mkdocs serve
```

Ouvrez ensuite <http://127.0.0.1:8000>. Avant de proposer vos changements, vérifiez qu'aucun avertissement n'apparaît avec `mkdocs build --strict`.
