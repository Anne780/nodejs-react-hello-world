pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Manually clone the repository
                git 'https://github.com/Anne780/nodejs-react-hello-world.git'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
    }

    post {
        success {
            echo 'Pipeline successful!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}
