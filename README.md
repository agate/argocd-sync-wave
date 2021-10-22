# argocd-sync-wave

ArgoCD sync wave demo

## Prepare

### create a namespace for this demo

`kubectl create namespace argocd-sync-wave`

### setup your argocd

1. Make sure your kubectl is working properly.
2. Follow this doc to install argocd to your kubernetes cluster.
   https://argo-cd.readthedocs.io/en/stable/getting_started/

## See how sync wave work in a one folder application

1. `kubectl apply -f ./onedir/versions/1.yaml`
2. open your argocd web page and view how wave -1, 0, 1 resources get synced.
3. `kubectl apply -f ./onedir/versions/2.yaml`
4. open your argocd web page and view how wave -1, 0, 1 resources get synced.

## See how sync wave work in the nested folder applications

1. `kubectl apply -f ./subdir/versions/1.yaml`
2. open your argocd web page and view how wave -1, 0, 1 resources get synced.
3. `kubectl apply -f ./subdir/versions/2.yaml`
4. open your argocd web page and view how wave -1, 0, 1 resources get synced.
