pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the GitHub repository
                git url: 'https://github.com/k8s-gurus/register-app', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                // Assuming this is a Node.js project, we run npm install
                echo 'Running Build Stage...'
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                // Run tests, assuming a Node.js test environment
                echo 'Running Test Stage...'
                sh 'npm test'
            }
        }

        stage('Package') {
            steps {
                // Package the application, if necessary
                echo 'Running Package Stage...'
                sh 'npm run build'
            }
        }
    }

    post {
        always {
            // Post actions like cleanup or notifications
            echo 'Cleaning up workspace...'
            cleanWs()
        }
        success {
