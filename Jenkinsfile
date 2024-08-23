pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'mvn clean install' // Example build command for a Maven project
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'mvn test' // Example test command for a Maven project
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
            sh 'mvn clean' // Clean up after the build
        }
        success {
            echo 'Build was successful!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
