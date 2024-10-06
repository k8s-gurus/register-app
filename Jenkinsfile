pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from the GitHub repository
                git url: 'https://github.com/k8s-gurus/register-app', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                // Replace with your actual build commands, e.g., npm install, Maven build, etc.
                echo 'Building the project...'
                sh 'echo Build step (replace with your actual build commands)'
            }
        }

        stage('Test') {
            steps {
                // Replace with your actual test commands, e.g., npm test, pytest, etc.
                echo 'Running tests...'
                sh 'echo Test step (replace with your actual test commands)'
            }
        }

        stage('Deploy') {
            steps {
                // Replace with your actual deploy commands if needed
                echo 'Deploying the application...'
                sh 'echo Deploy step (replace with your actual deploy commands)'
            }
        }
    }

    post {
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
