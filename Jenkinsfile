pipeline {
    agent any  // This tells Jenkins to run the pipeline on any available agent

    stages {
        stage('Build') {
            steps {
                // Install dependencies
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                // Run tests using pytest
                sh 'pytest'
            }
        }

        stage('Deploy') {
            steps {
                // Simulate deployment, in practice you could push the code to a server or containerize it.
                echo 'Deploying the application...'
            }
        }
    }

    post {
        success {
            echo 'Build completed successfully!'
        }

        failure {
            echo 'Build failed!'
        }
    }
}
