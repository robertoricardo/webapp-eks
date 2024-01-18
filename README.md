## WebApp no Cluster EKS

### Instâncias

**JENKINS SERVER**

Configurações:
- t2.large
- EBS - 15GiB - gp2


Atualizando o sistema
```
sudo apt update && sudo apt upgrade
```
Instalação do Jenkins

- Para instalar o Jenkins é necessário a instalação do JAVA
  ```
  sudo apt update
  sudo apt install fontconfig openjdk-17-jre
  java -version
  openjdk version "17.0.8" 2023-07-18
  OpenJDK Runtime Environment (build 17.0.8+7-Debian-1deb12u1)
  OpenJDK 64-Bit Server VM (build 17.0.8+7-Debian-1deb12u1, mixed mode, sharing)
  ```
- Instalação do Jenkins
  ```
  sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
  echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
  sudo apt-get update
  sudo apt-get install jenkins
  ```
#### Link para o vídeo do projeto

https://www.youtube.com/watch?v=e42hIYkvxoQ
