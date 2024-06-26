pipeline {
    agent any

    environment {
     
    }

    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/desarrollado-web-epm/Devops.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("$DOCKERHUB_REPO:latest")
                }
            }
        }
        
    }
    post {
        always {
            cleanWs()
        }
    }
}
