## WebApp no Cluster EKS

### Instâncias

**JENKINS SERVER**

Configurações:
- t2.medium
- EBS - 15GiB - gp2

Security Group
- Inbound Rules

   Type: Custom TCP
   Port Range: 8080
   Source: 0.0.0.0/0

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
sudo systemctl enable jenkins
sudo systemctl start jenkins
```

Para verificar o status do Jenkins
```
sudo systemctl status jenkins
```


#### Link para o vídeo do projeto

https://www.youtube.com/watch?v=e42hIYkvxoQ
