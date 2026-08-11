# Comandos básicos de Git y GitHub

## Ramas

### Ver ramas
git branch

### Crear una nueva rama

git branch nueva-funcionalidad

### Crear una nueva rama y cambiar
git switch -c nombre-rama

### Cambiar de rama
git switch nombre-rama

### Guardar cambios
git add .
git commit -m "mensaje"

### Subir rama
git push -u origin nombre-rama

### Fusionar
git switch main
git pull
git merge nombre-rama
git push

# Borrar rama
git branch -d nombre-rama
git push origin --delete nombre-rama

## Comprobar que un fichero está en una rama
git ls-tree -r nombre-rama --name-only | grep fichero
