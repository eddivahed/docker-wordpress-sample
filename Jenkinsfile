pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build and Up Docker Compose') {
            steps {
                dockerComposeBuildAndUp()
            }
        }

        stage('Run Docker Containers') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
