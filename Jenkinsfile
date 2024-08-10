pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'github-pat', url: 'https://github.com/your-username/simple-web-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('simple-web-app')
                }
            }
        }
    }
}

