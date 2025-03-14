pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Shin-9x/lgm8.git'
            }
        }

        stage('Rebuild Services') {
            steps {
                sh 'docker compose -f infrastructure/docker-compose.yml build'
                sh 'docker compose -f infrastructure/docker-compose.yml up -d'
            }
        }
    }
}
