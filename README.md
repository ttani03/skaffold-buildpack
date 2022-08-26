# skaffold-buildpacks

skaffold で buildpacks を使ってイメージをビルドし、minikube 上に展開する

## 環境

- Intel Mac, macOS Monterey 12.5.1
- minikube v1.26.1 (ドライバは VMware Fusion)
- Docker Engine 20.10.17 (minikube内)
- skaffold v1.39.2

## 使い方

リポジトリをクローン

```
git clone git@github.com:ttani03/skaffold-buildpack.git
cd skaffold-buildpack
```

minikube を起動

```
minikube start --driver=vmware
```

minikube 内の Docker を使うよう、環境変数を設定

```
eval $(minikube docker-env) 
```

skaffold でイメージをビルドして、minikube 上に展開

```
skaffold run --port-forward
```

表示された URL にアクセス ※ `/hello` にアクセスする必要あり
