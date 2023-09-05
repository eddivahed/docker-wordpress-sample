pipeline {
    agent any 

    stages {
        stage('Checkout') {
            steps {
                // This step checks out the code from the repository
                checkout scm
            }
        }

        // stage('Build Docker Image') {
        //     steps {
        //         // Build the Docker image using docker-compose
        //         sh 'docker-compose build'
        //     }
        // }

        stage('Run Docker Containers') {
            steps {
                // Start the containers using docker-compose
                sh 'docker-compose up -d'
            }
        }
    }

    post {
        always {
            // Clean up the workspace after the pipeline run
            cleanWs()
        }
    }
}
