pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from the GitHub repository
                git url: 'https://github.com/k8s-gurus/register-app', branch: 'main'
            }
        }

        stage('Test') {
            steps {
                // Simulating a test step
                echo 'Running tests...'
                // This is a simple shell command to test the pipeline.
                sh 'echo "Tests passed!"'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
