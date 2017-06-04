## 準備
```sh
brew cask install minikube
brew install kubernetes-helm
helm init
helm repo update
```

## start kubernetes
```sh
minikube start
eval $(minikube docker-env)
```

## help
- charts list
  - helm search
- show parameter
  - helm inspect stable/mysql

```config.yaml
mysqlUser: user1
mysqlPassword: password1
```

- start
```sh
helm install -f config.yaml stable/mysql
```

- ls
  - `helm ls`
- rm
  - helm delete <name>
- status
  - helm stats <name>
