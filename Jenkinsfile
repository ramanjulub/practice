pipeline {
    agent any
    environment {
        DOCKER_IMAGE = "ramanjulu421/nginx-test:latest"
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ramanjulub/practice.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $DOCKER_IMAGE .'
            }
        }
        stage('Push to Registry') {
            steps {
                sh 'docker push $DOCKER_IMAGE'
            }
        }
        stage('Deploy to Minikube') {
            steps {
                sshagent(['vm2-ssh-cred']) {
                    sh '''
                    scp deployment.yaml service.yaml azureuser@135.235.218.198:/home/azureuser/k8s-manifests/
                    ssh azureuser@135.235.218.198 "kubectl apply -f ~/k8s-manifests/deployment.yaml && kubectl apply -f ~/k8s-manifests/service.yaml"
                    '''
                }
            }
        }
    }
}
