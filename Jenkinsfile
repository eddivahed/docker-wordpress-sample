pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker-compose build'
            }
        }

        stage('Run Docker Containers') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
