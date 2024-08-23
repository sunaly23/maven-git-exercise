pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                bat 'mvn clean install' // Example build command for a Maven project on Windows
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
                bat 'mvn test' // Example test command for a Maven project on Windows
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Deployment commands go here
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
            bat 'mvn clean' // Clean up after the build on Windows
        }
        success {
            echo 'Build was successful!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
