pipeline {

    agent any

    stages {
        stage('Print') {
            steps {
                git 'https://github.com/sdevops5427/roboshop-cart-v1.git'
                aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 012751250483.dkr.ecr.us-east-1.amazonaws.com
                docker build -t 012751250483.dkr.ecr.us-east-1.amazonaws.com/cart .
                docker push 012751250483.dkr.ecr.us-east-1.amazonaws.com/cart
            }
        }
    }
}