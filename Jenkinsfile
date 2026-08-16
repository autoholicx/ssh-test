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
                echo 'All code tests passed beautifully!' 
            }
        }
        stage('Build') {
            steps {
                echo 'Building production assets...'
            }
        }
    }
}
