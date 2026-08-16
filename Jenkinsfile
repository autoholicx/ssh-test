pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Pulling code from GitHub...'
            }
        }
        stage('Test') {
            steps {
                echo 'Running project automated tests...'
                // You can add testing commands here like: sh 'npm test' or sh 'pytest'
            }
        }
        stage('Build') {
            steps {
                echo 'Building production assets...'
            }
        }
    }
}
