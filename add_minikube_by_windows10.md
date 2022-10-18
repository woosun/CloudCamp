1. 파워쉘에서 실행 </br>
</br>
New-Item -Path 'c:\' -Name 'minikube' -ItemType Directory -Force</br>
Invoke-WebRequest -OutFile 'c:\minikube\minikube.exe' -Uri 'https://github.com/kubernetes/minikube/releases/latest/download/minikube-windows-amd64.exe' -UseBasicParsing</br>
</br>
</br>
2. 파워쉘 관리자권한에서 실행</br>
</br>
$oldPath = [Environment]::GetEnvironmentVariable('Path', [EnvironmentVariableTarget]::Machine)</br>
if ($oldPath.Split(';') -inotcontains 'C:\minikube'){ `</br>
  [Environment]::SetEnvironmentVariable('Path', $('{0};C:\minikube' -f $oldPath), [EnvironmentVariableTarget]::Machine) `</br>
}</br>
</br>
3.WSL 활성화 및 Ubuntu 설치 참고하여 설치하자 +도커설치</br>
</br>
https://goddaehee.tistory.com/313</br>
 </br>
 </br>

minikube start --driver=docker</br>
minikube delete</br>
minikube start --kubernetes-version=v1.22.5</br>
minikube dashboard</br>
</br>
끝</br>
</br>
 </br>
종료시</br>
</br>
파워쉘에서 명령어입력</br>
</br>
minikube stop</br>
</br>
종료되면 도커 데스크탑 종료</br>
시작시</br>
</br>
도커 데스크탑 실행</br>
</br>
파워쉘에서 명령어입력</br>
</br>
minikube start --kubernetes-version=v1.22.5</br>
minikube dashboard</br>
