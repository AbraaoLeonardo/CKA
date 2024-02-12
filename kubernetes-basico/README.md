## Projeto final do curso de kubernetes
### Conceitos abordados utilizados nesse projeto.
1. Pod
2. ReplicaSet
3. Deployment
4. Service.
5. Namespace

## Como executar esse projeto?
Primeiro precisaremos criar nosso cluster kubernetes. Para esse projeto iremos usar o minikube.
### Instalação
#### Linux
#### Minikube

```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```
#### Git
Use a documentação do git para instalar a versão de sua distro. <a href="https://git-scm.com/download/linux">site oficial</a>

#### kubectl

```
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin
```


### MacOs

```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-amd64
sudo install minikube-darwin-amd64 /usr/local/bin/minikube
```

#### Git

```
brew install git
```

#### Kubectl
```
brew install kubectl
kubectl version --client 
```


### Windows.
Não é recomendado a utilização do minikube no ambiente windows. Por isso, recomendo a instalação de uma máquina virtual com o sistema virtual windows.
1. Instale o virtual box. <a href="https://www.virtualbox.org/wiki/Downloads">site oficial</a>
2. Baixe uma distro. Devido a simplicidade do ubuntu, recomendo a sua utilização, porém fique a vontade em utilizar a que tenha mais fácilidade. <a href="https://ubuntu.com/download/desktop">site oficial</a>
3. Após a instalação, abra o terminal e execute.

```
sudo apt install && \
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-amd64 && \
sudo install minikube-darwin-amd64 /usr/local/bin/minikube
```

#### Instalando o git

```
apt-get install git
```

#### Instalando o kubectl
```
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin
```


## Executando o projeto.
No terminal, execute os seguintes comandos.
```
git clone https://github.com/AbraaoLeonardo/CKA.git # Baixar o código fonte
cd CKA/kubernetes-basico # Acessar a pasta do projeto
minikube start # Iniciar o cluster kubernetes
kubectl apply -k . # Executando todos os serviços com o kustomize
minikube service jupyter-svc -n jupyter --url # Pegando o endpoint para acessar a aplicação
``` 
