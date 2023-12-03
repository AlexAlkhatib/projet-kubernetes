# Mini-projet 4KUBE : Fleetman

## Contenu de ce dépôt

Le répertoire `docker/` contient le fichier `compose.yaml` original.

Le répertoire `kubernetes/` contient les manifestes kubernetes.

Le fichier `Montage cluster Kubernetes.pdf` contient le document détaillant la procédure utilisée pour créer un cluster.

## Mise en route du déploiement Kubernetes

Pré-requis : Docker Desktop avec l'option Kubernetes activée, kubectl.

- Lancer Docker Desktop
- `kubectl apply -f kubernetes/`
- Dans un navigateur, se rendre à l'adresse `localhost:80`
- L'application s'affiche

Si l'application ne s'affiche pas, l'adresse est peut-être incorrects :
- `kubectl get services` : Chercher le service `fleetman-webapp` de type `LoadBalancer`. Prendre en note la valeur `EXTERNAL-IP`. Naviguer vers cette adresse, toujours avec le port 80.
