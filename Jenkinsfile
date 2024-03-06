pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
               git branch: 'main',
               url: 'https://github.com/aprajwalc/PES1UG21CS418_Jenkins.git'
            }
        }
        stage('Build') {
            steps {
                build 'PES1UG21CS418-1'
                sh 'g++ mainfile.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
