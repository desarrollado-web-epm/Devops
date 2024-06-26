pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/desarrollado-web-epm/Devops.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('nginx_image:latest')
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
