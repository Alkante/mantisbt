# Mantis community dev

## Lancement
```bash
# Login on Alkante docker registry
docker login docker.alkante.com

# Put UID and GID in env file
echo -e "LOCAL_USER_ID=$(id -u)\nLOCAL_GROUP_ID=$(id -g)" > docker-compose.env;

# Build dev image
docker-compose build

# Run containers
docker-compose up

# Run composer
docker exec -ti -u www-data -w /var/www/html/mantisbt mantis_web composer install
```
Got to : http://localhost:2121/mantisbt/admin/install.php (administrator/root)


## Mise à jour du fork
```bash
git remote set-url origin git@github.com:mantisbt/mantisbt.git
git fetch
git rebase
git remote set-url origin git@github.com:Alkante/mantisbt.git
git fetch
git push
```

## Set git info commit
```bash
git config user.name "John Doe"
git config user.email johndoe@example.com
```
