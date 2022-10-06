Deploying minikub on Windows
    https://kubernetes.io/docs/tasks/tools/install-minikube/
    
2. Commands
    #Check to see if virtualization is supported
    systeminfo

    #Install Virtualbox (info at chocolatey.org)
    choco install virtualbox

    #Install Minikube with Chocolatey
    choco install minikube

    #Start Minikube
    minikube start

3. Try docker
    docker ps
    
    You may see an error, to fix that
    minikube docker-env
    
    Now take the last commnad displayed by above command @FOR ..., that will fix the issue
    

Deploying minikube on Mac
    https://kubernetes.io/docs/tasks/tools/install-minikube/

2. Commands
    #Check to see if virtualization is supported
    sysctl -a | grep -E --color 'machdep.cpu.features|VMX'

    #Install Virtualbox with Brew (info at brew.sh)
    brew cask install virtualbox

    #Install Minikube with Brew
    brew cask install minikube

    #Install Kubectl
    brew install kubernetes-cli

    #Install the Docker Client
    brew install docker

    #Start Minikube
    minikube start

    #Configure the Docker Client
    minikube docker-env