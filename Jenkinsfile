pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Add deployment steps here
                // e.g., deploy to a staging environment
            }
        }
    }

    post {
        success {
            // Add notification or further actions on success
            echo 'Build and deployment successful!'
        }
        failure {
            // Add notification or further actions on failure
            echo 'Build or deployment failed!'
        }
    }
}
