# examen_action

Repo minimal pour l'exercice CI/CD GitHub Actions.

## Objectif
- Construire automatiquement une image Docker
- Push l'image sur Docker Hub à chaque push GitHub

## Secrets GitHub requis
Dans GitHub → Settings → Secrets and variables → Actions, ajouter:
- `DOCKERHUB_USERNAME`
- `DOCKERHUB_TOKEN` (un access token Docker Hub)

## Image publiée
- `${DOCKERHUB_USERNAME}/${REPO_NAME}:latest`
- `${DOCKERHUB_USERNAME}/${REPO_NAME}:sha-...`

## Test local
Depuis la racine du repo:
- `docker build -t examen_action .`
- `docker run --rm -p 3000:3000 examen_action`
- ouvrir http://localhost:3000
