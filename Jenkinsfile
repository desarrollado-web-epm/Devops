pipeline {
    agent any

    environment {
     
    }

    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/your_username/your_repository.git'
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
