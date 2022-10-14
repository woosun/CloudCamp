#brew 설치되어있어야함
#minikube설치
brew install minikube
curl -Lo minikube https://github.com/kubernetes/minikube/releases/download/v1.25.1/minikube-darwin-arm64 \\n  && chmod +x minikube\n
sudo install minikube /usr/local/bin/minikube
minikube version
#도커 설치되어있어야함
minikube start --driver=docker
minikube delete
#버전 다운그레이드
minikube start --kubernetes-version=v1.22.5
minikube dashboard
