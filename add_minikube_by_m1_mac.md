#brew 설치되어있어야함</br>
#minikube설치</br>
brew install minikube</br>
curl -Lo minikube https://github.com/kubernetes/minikube/releases/download/v1.25.1/minikube-darwin-arm64 \\n  && chmod +x minikube\n</br>
sudo install minikube /usr/local/bin/minikube</br>
minikube version</br>
#도커 설치되어있어야함</br>
minikube start --driver=docker</br>
minikube delete</br>
#버전 다운그레이드</br>
minikube start --kubernetes-version=v1.22.5</br>
minikube dashboard</br>
